<template>
  <div>
    <div class="Carousel">
      <div v-for="item in renderElems(currentIndex)" :key="items.indexOf(item)">
        <div class="Rectangle" style="touch-action: pan-x">
          <h3>{{ item.header }}</h3>
          <p>{{ item.text }}</p>
        </div>
      </div>
    </div>
    <div class="Buttons">
      <div class="Left" v-on:click="moveLeft">
        <svg height="87" viewBox="0 0 84 87" width="84" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <filter id="a" filterUnits="objectBoundingBox" height="150%" width="150%" x="-25%" y="-25%">
              <feGaussianBlur in="SourceGraphic" stdDeviation="5"/>
            </filter>
            <linearGradient id="b" x1="100%" x2="0%" y1="100%" y2="0%">
              <stop offset="0%" stop-color="#DD6F40"/>
              <stop offset="100%" stop-color="#F79369"/>
            </linearGradient>
          </defs>
          <g fill="none" fill-rule="evenodd">
            <path d="M5 15h60v60H5z" fill="#D05826" fill-opacity=".5" filter="url(#a)" transform="translate(7)"/>
            <path d="M0 0h70v70H0z" fill="url(#b)" transform="translate(7)"/>
            <path d="M30 47h24V23H30z"/>
            <path
                d="M41.365 32.61l1.584-1.542c.956-.93.956-2.44 0-3.37a2.496 2.496 0 0 0-3.462 0l-5.77 5.617a2.339 2.339 0 0 0 0 3.37l5.77 5.617c.956.93 2.506.93 3.462 0 .956-.93.956-2.44 0-3.37l-1.584-1.542h7.245a2.39 2.39 0 0 0 0-4.78h-7.245z"
                fill="#1E1E1E"/>
          </g>
        </svg>
      </div>
      <div class="Right" v-on:click="moveRight">
        <svg height="87" viewBox="0 0 84 87" width="84" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <filter id="a" filterUnits="objectBoundingBox" height="150%" width="150%" x="-25%" y="-25%">
              <feGaussianBlur in="SourceGraphic" stdDeviation="5"/>
            </filter>
            <linearGradient id="b" x1="100%" x2="0%" y1="100%" y2="0%">
              <stop offset="0%" stop-color="#DD6F40"/>
              <stop offset="100%" stop-color="#F79369"/>
            </linearGradient>
          </defs>
          <g fill="none" fill-rule="evenodd">
            <path d="M5 15h60v60H5z" fill="#D05826" fill-opacity=".5" filter="url(#a)" transform="translate(7)"/>
            <path d="M0 0h70v70H0z" fill="url(#b)" transform="translate(7)"/>
            <path d="M54 47H30V23h24z"/>
            <path
                d="M42.635 32.61l-1.584-1.542a2.339 2.339 0 0 1 0-3.37 2.496 2.496 0 0 1 3.462 0l5.77 5.617c.956.93.956 2.44 0 3.37l-5.77 5.617c-.956.93-2.506.93-3.462 0a2.339 2.339 0 0 1 0-3.37l1.584-1.542H35.39a2.39 2.39 0 0 1 0-4.78h7.245z"
                fill="#1E1E1E"/>
          </g>
        </svg>
      </div>
      <div v-for="n in items.length" :key="n" class="Dots">
        <span v-if="currentIndex!==n-1" class="dot" v-on:click="move(n)"/>
        <span v-else class="activeDot"/>
      </div>
    </div>
  </div>
</template>

<script>
import VueScreenSize from 'vue-screen-size'

export default {
  name: "Carousel",
  mixins: [VueScreenSize.VueScreenSizeMixin],
  data() {
    return {
      currentIndex: 0,
      items: [
        {
          header: "Overwhelming and inaccurate paperwork",
          text: "Most documents, such as orders, invoices, contracts, etc. are stored in folders on endless shelves. They are never easy to find. Moreover, due to human factor, crucial mistakes take place that cost your company much time to solve, but also drain your budget."
        },
        {
          header: "Manual order management based on phone calls and emails",
          text: "Do your clients call you just to find out that the necessary product is currently out of stock? You waste resources by not providing them with actual information about your available inventory online"
        },
        {
          header: "Inefficient truck load",
          text: "Without dynamic truck load scheduling, your company misses up to 50% of the potential loading capability"
        },
        {
          header: "2Manual order management based on phone calls and emails",
          text: "Do your clients call you just to find out that the necessary product is currently out of stock? You waste resources by not providing them with actual information about your available inventory online"
        },
        {
          header: "2Inefficient truck load",
          text: "Without dynamic truck load scheduling, your company misses up to 50% of the potential loading capability"
        }
      ]
    }
  },
  methods: {
    renderElems() {
      return this.items.filter((item, index) => {
        return index < (this.$vssWidth / 500).toFixed(0)
      })
    },
    moveRight() {
      if (this.currentIndex === this.items.length - 1) {
        this.currentIndex = 0
      } else {
        this.currentIndex++
      }
      const shifted = this.items.shift()
      this.items.push(shifted)
    },
    moveLeft() {
      if (this.currentIndex === 0) {
        this.currentIndex = this.items.length - 1
      } else {
        this.currentIndex--
      }
      this.items.reverse()
      const shifted = this.items.shift()
      this.items.push(shifted)
      this.items.reverse()
    },
    logger(data) {
      console.log(data)
    },
    move(step) {
      if (this.currentIndex < step - 1) {
        for (let i = Math.min(this.currentIndex, step - 1); i < Math.max(this.currentIndex, step - 1); i++) {
          this.moveRight()
        }
        return 0
      }
      if (this.currentIndex > step - 1) {
        for (let i = Math.max(this.currentIndex, step - 1); i > Math.min(this.currentIndex, step - 1); i--) {
          this.moveLeft()
        }
        return 0
      }
    }
  }
}
</script>

<style scoped>
.dot {
  height: 15px;
  margin-left: 25px;
  width: 15px;
  background-color: #bbb;
  border-radius: 50%;
  display: inline-block;
}

.activeDot {
  height: 15px;
  margin-left: 25px;
  width: 15px;
  background-color: #1e1e1e;
  border-radius: 50%;
  display: inline-block;
}

.Left {
  opacity: 0.5;
}

.Right {
  opacity: 0.5;
}

.Left:hover {
  opacity: 1;
}

.Right:hover {
  opacity: 1;
}

.Carousel {
  display: flex;
  margin-left: 252px;
}

.Buttons {
  display: flex;
  margin-top: 20px;
  margin-left: 252px;
}


.Rectangle {
  width: 420px;
  height: auto;
  max-height: 390px;
  margin: 100px 11px 0 0;
  padding: 67px 37px 168px 38px;
  object-fit: contain;
  box-shadow: 0 10px 30px 0 rgba(8, 61, 119, 0.25);
  background-color: rgba(8, 61, 119, 1);
}

.Carousel > div:last-child {
  overflow: hidden;
}

.Rectangle > h3 {
  text-align: left;
  width: 345px;
  height: 50px;
  margin: 0 0 22px;
  font-family: OpenSans;
  font-size: 21px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.19;
  letter-spacing: -0.53px;
  color: white;
}

.Rectangle > p {
  text-align: left;
  width: 345px;
  height: 115px;
  margin: 22px 0 0;
  font-family: OpenSans;
  font-size: 17px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: -0.43px;
  color: white;
}

@media screen and (max-width: 1025px) {
  .Carousel {
    margin-left: 112px;
  }

  .Buttons {
    margin-top: 20px;
    margin-left: 112px;
  }

  .Rectangle {
    margin-top: 20px;
    width: 280px;
    height: auto;
    max-height: 290px;
    padding: 67px 37px 118px 38px;
  }

  .Rectangle > h3 {
    width: 245px;
    height: 50px;
    font-size: 17px;
    margin: 0 0 22px;
    line-height: 1.19;
    letter-spacing: -0.53px;
  }

  .Rectangle > p {
    font-size: 14px;
    width: 245px;
    height: 115px;
    margin: 22px 0 0;
    letter-spacing: -0.43px;
  }
}

@media screen and (max-width: 500px) {
  .dot {
    height: 10px;
    margin-left: 15px;
    width: 10px;
  }

  .activeDot {
    height: 10px;
    margin-left: 15px;
    width: 10px;
  }

  .Carousel {
    margin-left: 12px;
  }

  .Buttons {
    margin-top: 10px;
    margin-left: 12px;
  }


  .Rectangle {
    position: relative;
    margin-top: 20px;
    width: 240px;
    height: auto;
    max-height: 290px;
    padding: 67px 37px 118px 38px;
  }


  .Rectangle > h3 {
    width: 245px;
    height: 50px;
    font-size: 17px;
    margin: 0 0 22px;
    line-height: 1.19;
    letter-spacing: -0.53px;
  }

  .Rectangle > p {
    font-size: 14px;
    width: 245px;
    height: 115px;
    margin: 22px 0 0;
    letter-spacing: -0.43px;
  }
}
</style>

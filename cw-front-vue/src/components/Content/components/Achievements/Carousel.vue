<template>
  <div>
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
      <div v-for="n in items.length" :key="n" class="Dots">
        <span v-if="currentIndex!==n-1" class="dot"></span>
        <span v-if="currentIndex===n-1" class="activeDot"></span>
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
    </div>
    <div class="Carousel">
      <article v-for="item in renderElems(currentIndex)" :key="items.indexOf(item)">
        <div class="ImageField">
          <div class="Image">
            <img :key="item.index" :src="item.photo"/>
          </div>
          <div class="ImageHeader">
            <p>{{ item.photoDescription }}</p>
          </div>
        </div>
        <div class="TextField">
          <h3>{{ item.header }}</h3>
          <pre>{{ item.text }}</pre>
        </div>
      </article>
    </div>

  </div>
</template>

<script>
import VueScreenSize from 'vue-screen-size'

const image_1 = require('../../assets/carousel-image-1.png');
const image_2 = require('../../assets/carousel-image-2.png');
const image_3 = require('../../assets/carousel-image-3.png');

export default {
  name: "Carousel",
  mixins: [VueScreenSize.VueScreenSizeMixin],
  data() {
    return {
      currentIndex: 0,
      items: [
        {
          photo: image_1,
          photoDescription: "double truck day load capacity increase ",
          header: "ERP system for construction materials factory",
          text: "Custom logistics software includes several modules that enabled to fully digitalize a factory" +
              "– Order and stock management optimization\n" +
              "– Automatic invoicing and accounting\n" +
              "– Delivery scheduling and route planning\n" +
              "– Automatic contractors selection\n" +
              "\n" +
              "Eliminating manual work enabled the factory to double truck day load capacity (an increase from " +
              "45 to 92 trucks per day) and save over 60.000 EUR in the first year. "
        },
        {
          photo: image_2,
          photoDescription: "2double truck day load capacity increase ",
          header: "2ERP system for construction materials factory",
          text: "2Custom logistics software includes several modules that enabled to fully digitalize a factory" +
              "– Order and stock management optimization\n" +
              "– Automatic invoicing and accounting\n" +
              "– Delivery scheduling and route planning\n" +
              "– Automatic contractors selection\n" +
              "\n" +
              "Eliminating manual work enabled the factory to double truck day load capacity (an increase from " +
              "45 to 92 trucks per day) and save over 60.000 EUR in the first year. "
        },
        {
          photo: image_3,
          photoDescription: "3double truck day load capacity increase ",
          header: "3ERP system for construction materials factory",
          text: "3Custom logistics software includes several modules that enabled to fully digitalize a factory" +
              "– Order and stock management optimization\n" +
              "– Automatic invoicing and accounting\n" +
              "– Delivery scheduling and route planning\n" +
              "– Automatic contractors selection\n" +
              "\n" +
              "Eliminating manual work enabled the factory to double truck day load capacity (an increase from " +
              "45 to 92 trucks per day) and save over 60.000 EUR in the first year. "
        }
      ]
    }
  },
  methods: {
    renderElems() {
      return this.items.filter((item, index) => {
        return index < 1
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
    }
  }
}
</script>

<style scoped>
.Dots {
  padding-top: 25px;
}

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
  margin-right: 25px;
  opacity: 0.5;
}

.Right {
  margin-left: 50px;
  opacity: 0.5;
}

.Left:hover {
  opacity: 1;
}

.Right:hover {
  opacity: 1;
}

.Buttons {
  display: flex;
  justify-content: center;
}

.Carousel > article {
  display: flex;
  flex-direction: row;
  justify-content: center;
  flex-wrap: wrap;
  margin-top: 50px;
}

.ImageField {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.ImageHeader {
  text-transform: uppercase;
  text-align: center;
  width: 345px;
  height: 20px;
  margin: 1px 0 172px 16px;
  font-family: OpenSans;
  font-size: 15px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: -0.38px;
  color: #1e1e1e;
}

.TextField {
 margin-left: 80px
}

.TextField > h3 {
  text-align: left;
  white-space: pre-wrap;
  height: 60px;
  width: auto;
  margin: 0 0 10px;
  font-family: Catamaran-Black;
  font-size: 25px;
  font-weight: 900;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.2;
  letter-spacing: -0.63px;
  color: #1e1e1e;
}

.TextField > pre {
  white-space: pre-wrap;
  text-align: left;
  width: 345px;
  height: 276px;
  margin: 10px 0 0;
  opacity: 0.75;
  font-family: OpenSans;
  font-size: 17px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: -0.43px;
  color: #1e1e1e;
}


@media screen and (max-width: 1025px) {
  .Buttons {
    margin-top: 20px;
    margin-left: 112px;
  }
  .TextField {
    margin-left: 0px
  }
  .Carousel {
    margin-left: 112px;
  }

  .ImageHeader {
    width: 345px;
    height: 20px;
    margin: 1px 0 50px 16px;
    font-size: 15px;
  }

  .TextField > h1 {
    text-align: left;
    width: 345px;
    height: 60px;
    font-size: 25px;
    margin-right: 30px;
  }

  .TextField > pre {
    width: auto;
    height: 276px;
    font-size: 17px;
  }
}

@media screen and (max-width: 500px) {
  .dot {
    height: 10px;
    margin-left: 15px;
    width: 10px;
  }

  .TextField {
    margin-left: 0
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

  .Image {
    transform: scale(0.6);
    margin-top: -150px;

  }

  .ImageField {
    max-width: 300px;
  }

  .ImageHeader {
    font-size: 13px;
    margin-top: -100px;
  }

  .TextField {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .TextField > h3 {
    text-align: center;
    font-size: 17px;
  }

  .TextField > pre {
    margin-top: -20px;
    width: auto;
    height: 276px;
    font-size: 14px;
  }
}
</style>

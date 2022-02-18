<template>
  <div>
    <div class="image1x">
      <img src="@/components/Content/assets/group.png">
      <div class="Header">
        HOW CAN YOU BENEFIT FROM
        CUSTOM LOGISTICS SOFTWARE?
      </div>
      <div class="Circle1">
        <svg height="107" viewBox="0 0 106 107" width="106" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <filter id="a" filterUnits="objectBoundingBox" height="141.9%" width="142.1%" x="-21%" y="-20.9%">
              <feGaussianBlur in="SourceGraphic" stdDeviation="5.607"/>
            </filter>
          </defs>
          <g fill="none" fill-rule="evenodd" transform="translate(13 8)">
            <ellipse cx="40" cy="45.81" fill="#F79369" filter="url(#a)" opacity=".5" rx="40" ry="40.19"/>
            <ellipse cx="40" cy="40.19" fill="#F79369" rx="40" ry="40.19"/>
            <text fill="#FFF" font-family="Catamaran-Black, Catamaran Black" font-size="19.626" font-weight="700"
                  letter-spacing="-.491">
              <tspan x="36.217" y="48.98">1</tspan>
            </text>
          </g>
        </svg>
        <div class="TextField">
          <h1>{{ this.items[0].header }}</h1>
          <p>{{ this.items[0].text }}</p>
        </div>
      </div>
      <div class="Circle2">
        <svg height="107" viewBox="0 0 106 107" width="106" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <filter id="a" filterUnits="objectBoundingBox" height="141.9%" width="142.1%" x="-21%" y="-20.9%">
              <feGaussianBlur in="SourceGraphic" stdDeviation="5.607"/>
            </filter>
          </defs>
          <g fill="none" fill-rule="evenodd" transform="translate(13 8)">
            <ellipse cx="40" cy="45.81" fill="#F79369" filter="url(#a)" opacity=".5" rx="40" ry="40.19"/>
            <ellipse cx="40" cy="40.19" fill="#F79369" rx="40" ry="40.19"/>
            <text fill="#FFF" font-family="Catamaran-Black, Catamaran Black" font-size="19.626" font-weight="700"
                  letter-spacing="-.491">
              <tspan x="36.217" y="48.98">2</tspan>
            </text>
          </g>
        </svg>
        <div class="TextField">
          <h1>{{ this.items[1].header }}</h1>
          <p>{{ this.items[1].text }}</p>
        </div>
      </div>
      <div class="Circle3">
        <svg height="107" viewBox="0 0 106 107" width="106" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <filter id="a" filterUnits="objectBoundingBox" height="141.9%" width="142.1%" x="-21%" y="-20.9%">
              <feGaussianBlur in="SourceGraphic" stdDeviation="5.607"/>
            </filter>
          </defs>
          <g fill="none" fill-rule="evenodd" transform="translate(13 8)">
            <ellipse cx="40" cy="45.81" fill="#F79369" filter="url(#a)" opacity=".5" rx="40" ry="40.19"/>
            <ellipse cx="40" cy="40.19" fill="#F79369" rx="40" ry="40.19"/>
            <text fill="#FFF" font-family="Catamaran-Black, Catamaran Black" font-size="19.626" font-weight="700"
                  letter-spacing="-.491">
              <tspan x="36.217" y="48.98">3</tspan>
            </text>
          </g>
        </svg>
        <div class="TextField">
          <h1>{{ this.items[2].header }}</h1>
          <p>{{ this.items[2].text }}</p>
        </div>
      </div>
      <div class="Circle4">
        <svg height="107" viewBox="0 0 106 107" width="106" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <filter id="a" filterUnits="objectBoundingBox" height="141.9%" width="142.1%" x="-21%" y="-20.9%">
              <feGaussianBlur in="SourceGraphic" stdDeviation="5.607"/>
            </filter>
          </defs>
          <g fill="none" fill-rule="evenodd" transform="translate(13 8)">
            <ellipse cx="40" cy="45.81" fill="#F79369" filter="url(#a)" opacity=".5" rx="40" ry="40.19"/>
            <ellipse cx="40" cy="40.19" fill="#F79369" rx="40" ry="40.19"/>
            <text fill="#FFF" font-family="Catamaran-Black, Catamaran Black" font-size="19.626" font-weight="700"
                  letter-spacing="-.491">
              <tspan x="36.217" y="48.98">4</tspan>
            </text>
          </g>
        </svg>
        <div class="TextField">
          <h1>{{ this.items[3].header }}</h1>
          <p>{{ this.items[3].text }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "groupDecorCircles",
  data() {
    return {
      items: [
        {
          header: "Customized to your needs",
          text: "A software is developed exclusively with your needs and plans in mind. This enables to solve unique problems efficiently"
        },
        {
          header: "Short-term ROI",
          text: "You will experience the first returns right in the first month after integrating the system in your current processes"
        },
        {
          header: "Predictable scalability",
          text: "A custom system grows along with your business since your company goals are taken into account in the development process"
        },
        {
          header: "Improve, not rebuild",
          text: "Custom software supports and improves your running processes step-by-step. Your current system keeps working  "
        },
      ]
    }
  }
}
</script>

<style scoped>
.image1x {
  position: relative;
  margin-left: 157px;
  display: flex;
  flex-wrap: wrap;
  z-index: -50;
  background: white;
}

.Circle1 {
  position: absolute;
  top: 256px;
  left: 75px;
  display: flex;
}

.Circle2 {
  position: absolute;
  top: 256px;
  left: 604px;
}

.Circle3 {
  position: absolute;
  bottom: 66px;
  left: 75px;
}

.Circle4 {
  position: absolute;
  bottom: 66px;
  left: 604px;
}

.TextField {
  position: absolute;
  left: 125px;
  top: -20px;
}

.TextField > * {
  text-align: left;
  overflow: auto;
}

.TextField > h1 {
  width: 287px;
  height: 41px;
  font-family: Catamaran-Black;
  font-size: 25px;
  font-weight: 900;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: -0.63px;
  text-align: left;
  color: #1e1e1e;
}

.TextField > p {
  width: 345px;
  height: auto;
  margin: 20px 0 0;
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

.Header {
  position: absolute;
  text-align: left;
  top: 44px;
  left: 142px;
  width: 625px;
  height: 70px;
  font-family: Catamaran-Black;
  font-size: 35px;
  font-weight: 900;
  font-stretch: normal;
  font-style: normal;
  line-height: 1;
  letter-spacing: -0.88px;
  color: #1e1e1e;
}

@media screen and (max-width: 1025px) {
  .Header {
    width: 500px;
    height: 50px;
    font-size: 25px;
    font-weight: 900;
    font-stretch: normal;
    font-style: normal;
    line-height: 1;
    letter-spacing: -0.63px;
  }

  .image1x {
    margin: 0;
  }

  .image1x > img {
    position: static;
    margin-top: 300px;
    margin-left: -200px;
    transform: rotateZ(90deg);
    display: flex;
    flex-wrap: wrap;
  }

  .Circle1 {
    position: absolute;
    top: 202px;
    left: 51px;
    display: flex;
  }

  .Circle2 {
    position: absolute;
    top: 380px;
    left: 51px;
  }

  .Circle3 {
    position: absolute;
    top: 556px;
    left: 51px;
  }

  .Circle4 {
    position: absolute;
    top: 732px;
    left: 51px;
  }

  .image1x > div > svg > g > text > tspan {
    font-size: 20px;
  }

  .TextField > h1 {
    font-size: 20px;
  }

  .TextField > p {
    font-size: 17px;
    margin-top: -20px;
  }
}

@media screen and (max-width: 500px) {
  .image1x {
    margin: 0;
  }

  .image1x > img {
    position: static;
    margin-top: 300px;
    margin-left: -600px;
    transform: rotateZ(90deg);
    display: flex;
    flex-wrap: wrap;
  }

  .Circle1 {
    position: absolute;
    top: 202px;
    left: 3px;
    display: flex;
  }

  .Circle2 {
    position: absolute;
    top: 380px;
    left: 3px;
  }

  .Circle3 {
    position: absolute;
    top: 556px;
    left: 3px;
  }

  .Circle4 {
    position: absolute;
    top: 732px;
    left: 3px;
  }

  .Header {
    margin-left: -80px;
    text-align: left;
    font-size: 20px;
    width: auto;
  }

  .TextField {
    width: 50%
  }

  .TextField > h1 {
    font-size: 17px;
    width: 200px;
  }

  .TextField > p {
    font-size: 14px;
    margin-top: 5px;
    width: 200px;
  }
}
</style>

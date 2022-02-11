<template>
  <div class="Feedback">
    <div v-for="item in items" :key="item.name">
      <p>{{ item.text }}</p>
      <div class="FeedbackContainer">
        <span class="CTO-at">
  <span class="text-style-1">{{ item.name }}<br></span>{{ item.position }}</span>
        <img :src="item.photo" alt="" class="Photo"/>
      </div>
    </div>
  </div>
</template>

<script>
const image1 = require("../../assets/feedback-photo-1.png")
const image2 = require("../../assets/feedback-photo-2.png")
export default {
  name: "Feedback",
  data() {
    return {
      items: [
        {
          photo: image1,
          text: "Flawless communication with the Clockwise Software team resulted in a fleet management system that exactly met the needs of the municipal waste transportation company. The software runs on Android smartphones, so there was no need for expensive equipment, and the learning curve was low. We’ve implemented multi-tenancy to use this software in other projects connected with logistics.",
          name: "Dan Weber",
          position: "CEO/CTO at Marketsoup"
        },
        {
          photo: image2,
          text: "With the automatic load scheduling and proper route planning, we are finally able to use 100% of our truck load capacity. Also, order management and delivery have become much more efficient due to custom modules. In the first year, we have covered our investment in custom ERP system development",
          name: "Vadim Chabanenko",
          position: "Director at UDK Gazbeton"
        }
      ]
    }
  }
}
</script>

<style scoped>
.Feedback {
  width: 663px;
  margin-top: 140px;
  padding-top: 96px;
  padding-left: 40px;
  box-shadow: -10px 5px 15px #efefef;

}

.Photo {
  -webkit-filter: grayscale(100%);
  filter: grayscale(100%);
  max-height: 44px;
  max-width: 44px;
  margin-top: 25px;
}

p {
  text-align: left;
  width: 415px;
  height: 184px;
  margin: 0 0 15px;
  font-family: OpenSans;
  font-size: 17px;
  font-weight: 600;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: -0.43px;
  color: #1e1e1e;
}

.FeedbackContainer {
  display: flex;
}

.CTO-at {
  width: 356px;
  height: 44px;
  margin: 25px 15px 71px 0;
  font-family: OpenSans;
  font-size: 15px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: -0.43px;
  text-align: right;
  color: #1e1e1e;
}

.CTO-at .text-style-1 {
  font-size: 17px;
  font-weight: bold;
}

@media screen and (max-width: 1025px) {
  .Feedback {
    margin: 0 0 0 78px;
    padding: 60px 60px;
    box-shadow: 0 0 27px 9px #efefef;
    width: 80%;
  }

  p {
    width: 80%;
    white-space: pre-wrap;
    margin: 0 0 10px 30px;
    font-size: 17px;
  }

  .FeedbackContainer {
    margin-top: -20px;
  }
}

@media screen and (max-width: 500px) {
  .Feedback {
    margin-top: 40px;
    margin-left: 20px;
    padding: 20px;
    box-shadow: 0 0 27px 9px #efefef;
    width: 260px
  }

  .Feedback > div {
    width: 250px;
  }

  .FeedbackContainer {
    margin-left: -100px;
  }

  p {
    width: 220px;
    white-space: pre-wrap;
    margin: 0 0 10px 30px;
    font-size: 12px;
  }

}
</style>

<template>
  <div class="Advantages">
    <h1>OUR ADVANTAGES</h1>
    <div v-for="(item, index) in items" :key="item.header">
      <div class="AdvantageContainer" v-on:click="myFunction(index)">
        <div class="RedCircle"/>
        <h3>{{ item.header }}</h3>
      </div>
      <div :id="index" class="TextField">
        <p>{{ item.text }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Advantages",
  data() {
    return {
      items: [
        {
          header: "System Integration",
          text: "We help you with educating employees and integrating software in your running processes"
        },
        {
          header: "Technical support",
          text: "We guarantee support and product maintenance after release and keep improving the system in cooperation with your team"
        },
        {
          header: "Data security",
          text: "Your data is stored on secure servers based in Germany (or any other country on your request)"
        },
        {
          header: "We speak your language ",
          text: "Our managers are German- and English-speaking, so the business communication is clear and easy"
        },
        {
          header: "Representative in Germany",
          text: "Our business analyst is based in Frankfurt am Main. Discussing all the business issues in person is much more efficient"
        },
        {
          header: "5 years experience in logistics",
          text: "We’ve successfully implemented custom logistics/transportation/stock and order management systems"
        },
      ]
    }
  },
  methods: {
    myFunction(n) {
      if (document.getElementById(`${n}`).style.display === "flex") {
        document.getElementById(`${n}`).style.display = "none";
      } else {
        document.getElementById(`${n}`).style.display = "flex";
      }
    }
  }
}
</script>

<style scoped>
.Advantages {
  margin-left: 226px;
}

h1 {
  margin-top: 168px;
  text-align: left;
  width: 505px;
  height: 44px;
  font-family: Catamaran-Black;
  font-size: 35px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: 1;
  letter-spacing: -0.88px;
  color: #1e1e1e;
}

.RedCircle {
  background: #ea5256;
  border-radius: 50%;
  width: 34px;
  height: 34px;
}

.AdvantageContainer {
  display: flex;
  height: auto;
  width: auto;
  pointer-events: none;
}

.AdvantageContainer .TextField {
  display: flex;
}

h3 {
  text-align: left;
  margin-top: 0;
  margin-left: 43px;
  margin-bottom: 0;
  width: 330px;
  font-family: Catamaran-Black;
  font-size: 21px;
  font-weight: 900;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: -0.53px;
  color: #1e1e1e;
}

p {
  text-align: left;
  width: 345px;
  margin-left: 77px;
  margin-top: 0;
  margin-bottom: 34px;
  opacity: 0.75;
  font-family: OpenSans;
  font-size: 15px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: -0.38px;
  color: #1e1e1e;
}

@media screen and (max-width: 1025px) {
  .Advantages {
    margin: 0 0 0 79px;
  }

  .Advantages > h1 {
    width: 505px;
    height: 44px;
    font-family: Catamaran-Black;
    font-size: 25px;
    font-weight: 900;
    font-stretch: normal;
    font-style: normal;
    line-height: 1;
    letter-spacing: -0.63px;
    color: #1e1e1e;
  }

  p {
    margin-top: -5px;
    font-size: 15px;
    letter-spacing: -0.38px;
  }

  h3 {
    font-size: 20px;
  }
}

@media screen and (max-width: 500px) {
  .Advantages {
    margin-left: 10px;

  }

  h1 {
    font-size: 20px;
    margin-top: 100px;
    width: auto;
  }

  h3 {
    margin: 0 0 0 10px;
    font-size: 17px;
  }

  p {
    width: 250px;
    white-space: pre-wrap;
    margin: 0 0 10px 30px;
    font-size: 14px;
  }

  .RedCircle {
    margin-right: 20px;
    border: solid black;
    border-width: 0 3px 3px 0;
    display: inline-block;
    padding: 3px;
    background: white;
    border-radius: 0;
    width: 7px;
    height: 7px;
    transform: rotate(45deg);
    -webkit-transform: rotate(45deg);
  }

  .AdvantageContainer {
    display: flex;
    flex-direction: row-reverse;
    pointer-events: all;
  }

  .AdvantageContainer .TextField {
    display: flex;
  }

  .TextField {
    display: none;
  }
}
</style>

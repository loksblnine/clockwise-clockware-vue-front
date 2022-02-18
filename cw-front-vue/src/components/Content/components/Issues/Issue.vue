<template>
  <div class="Issue">
    <h3>HAVE YOU EXPERIENCED WITH ANY OF THIS ISSUES?</h3>
    <Carousel/>
    <div class="TextField">
      <p>
        Expenses reduction after implementing logistics management software!
      </p>
      <h1>
        49,2 %
      </h1>
    </div>
  </div>
</template>

<script>
import Carousel from "@/components/Content/components/Issues/Carousel";

export default {
  name: "Issue",
  components: {
    Carousel
  }
}
</script>

<style scoped>
.Issue {
  margin: 168px 28px 8px 28px;
}

.Issue > h3 {
  margin-left: 120px;
  width: 910px;
  height: 35px;
  font-family: Catamaran-Black;
  font-size: 35px;
  font-weight: 900;
  font-stretch: normal;
  font-style: normal;
  line-height: 1;
  letter-spacing: -0.88px;
  text-align: center;
  color: #1e1e1e;
}

.TextField {
  display: flex;
  justify-content: center;
  justify-items: center;
}

.TextField > p {
  width: 345px;
  height: 100px;
  margin: 100px 0 100px;
  opacity: 0.75;
  font-family: OpenSans;
  font-size: 25px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.2;
  letter-spacing: -0.63px;
  color: #1a1d1a;
}

.TextField > h1 {
  font-family: Catamaran-Black;
  font-size: 72px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.2;
  width: 346px;
  height: 100px;
  margin: 100px 0 100px;
  color: #1a1d1a;
}

@media screen and (max-width: 1025px) {
  .Issue {
    margin-left: 80px;
  }

  .Issue > div {
    margin-left: -150px;
  }

  .Issue > h3 {
    margin: 139px 91px 65px 0;
    width: 620px;
    height: 25px;
    font-family: Catamaran-Black;
    font-size: 25px;
    font-weight: 900;
    font-stretch: normal;
    font-style: normal;
    line-height: 1;
    letter-spacing: -0.63px;
    text-align: left;
    color: #1e1e1e;
  }

  .TextField {
    display: flex;
    justify-content: center;
    justify-items: center;
    margin-top: 80px;
  }

  .TextField > p {
    width: 245px;
    height: 100px;
    margin: 5px 0 50px 90px;
    opacity: 0.75;
    font-size: 20px;
    line-height: 1.2;
    letter-spacing: -0.63px;
    color: #1a1d1a;
  }

  .TextField > h1 {
    font-size: 52px;
    line-height: 1.2;
    width: 346px;
    height: 100px;
    margin: 0 0 5px;
  }
}

@media screen and (max-width: 500px) {
  .Issue {
    margin: 0;
    align-items: center;
  }

  .Issue > div {
    margin-left: 0;
  }

  .Issue > h3 {
    text-align: center;
    margin-left: 10px;
    margin-bottom: 0;
    width: 300px;
    height: 40px;
    font-size: 17px;
    font-weight: normal;
    font-stretch: normal;
    font-style: normal;
    line-height: normal;
    letter-spacing: -0.38px;
  }

  .TextField {
    display: flex;
    justify-content: center;
    justify-items: center;
    margin-top: 20px;
  }

  .TextField > p {
    width: 345px;
    height: 100px;
    margin: 5px 0 0 20px;
    opacity: 0.75;
    font-size: 14px;
    line-height: 1;
    letter-spacing: -0.63px;
    color: #1a1d1a;
  }

  .TextField > h1 {
    font-size: 36px;
    line-height: 1;
    width: 346px;
    height: 100px;
    margin: 0 0 5px;
  }
}
</style>

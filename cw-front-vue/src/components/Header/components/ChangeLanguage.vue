<template>
  <div class="form_toggle" style="margin-right: 0; margin-left: 0">
    <p>Language</p>
    <div class="form_toggle-item item-1">
      <input id="fid-1" v-model="picked" name="radio" type="radio"
             value="ENG"
             v-on:change="logger({language: picked})">
      <label for="fid-1">ENG</label>
    </div>
    <div class="form_toggle-item item-2">
      <input id="fid-2" v-model="picked" name="radio"
             type="radio" value="DE" v-on:change="logger({language: picked})">
      <label for="fid-2">DE</label>
    </div>
  </div>
</template>

<script>
export default {
  name: "ChangeLanguage",
  data() {
    return {
      picked: `ENG`
    }
  },
  methods: {
    logger: (value) => {
      console.log(value)
    }
  }
}
</script>

<style scoped>
.form_toggle > p {
  display: none;
}

.form_toggle > * {
  font-family: Catamaran, Catamaran, serif;
  font-size: 17px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: -0.53px;
  justify-content: space-between;
}

.form_toggle-item input[type=radio] {
  display: none;
}

.form_toggle-item > *:hover {
  cursor: pointer;
  text-decoration: underline;
  text-underline: #1e1e1e;
}

.form_toggle .item-1 input[type=radio] + label {
  background: white;
  color: rgba(86, 83, 83, 0.4);
}

.form_toggle .item-2 input[type=radio] + label {
  background: white;
  color: rgba(86, 83, 83, 0.4);
}

.form_toggle .item-1 input[type=radio]:checked + label {
  background: white;
  color: #1e1e1e;
}

.form_toggle .item-2 input[type=radio]:checked + label {
  background: white;
  color: #1e1e1e;
}

.form_toggle .item-1 {
  margin-left: 100px;
  margin-right: 20px;
}

.form_toggle .item-2 {
  margin-right: 220px;
}

@media (max-width: 700px) {
  .form_toggle {
    background-color: white;
    border-bottom: 1px solid #f3f3f3;
  }

  .form_toggle > p {
    margin: 0 50px 0 0;
    display: flex;
    background-color: white;
  }

  .form_toggle-item {
    margin: 0 5%;
  }

  .form_toggle .item-1 {
    margin-left: 0;
    margin-right: 0;
  }

  .form_toggle .item-2 {
    margin-right: 0;
  }
}

@media (max-width: 300px) {
  .form_toggle {
    background-color: white;
    border-bottom: 1px solid #f3f3f3;
  }

  .form_toggle > * {
    font-size: 14px;
  }

  .form_toggle > p {
    margin: 0;
    display: flex;
    background-color: white;
  }

  .form_toggle-item {
    margin: 0 5%;
  }
}
</style>

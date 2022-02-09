<template>
  <div class="Menu">
    <input id="menu-toggle" type="checkbox"/>
    <label class='menu-button-container' for="menu-toggle">
      <div class='menu-button'></div>
    </label>
    <div class="menu">
      <p v-on:click="logger(`Benefits`)">Benefits</p>
      <p v-on:click="logger(`Advantages`)">Advantages</p>
      <p v-on:click="logger(`Achievements`)">Achievements</p>
      <ChangeLanguage/>
    </div>
  </div>
</template>

<script>

import ChangeLanguage from "@/components/Header/components/ChangeLanguage";

export default {
  name: "Menu",
  components: {ChangeLanguage},
  methods: {
    logger: (value) => {
      console.log(value)
    }
  }
}
</script>

<style scoped>
.menu {
  display: flex;
  flex-direction: row;
  list-style-type: none;
  margin: 0;
  padding: 0;
}

.menu > * {
  display: flex;
  justify-content: center;
  margin: 0 1rem;
  font-family: Catamaran, Catamaran, serif;
  font-size: 17px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: -0.53px;
  color: #1e1e1e;
}

.menu-button-container {
  display: none;
  height: 100%;
  width: 30px;
  cursor: pointer;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

#menu-toggle {
  display: none;
}

.menu > p:hover {
  text-decoration: underline;
  text-underline: #1e1e1e;
  cursor: pointer;
}

.menu-button,
.menu-button::before,
.menu-button::after {
  display: block;
  background-color: #1e1e1e;
  position: absolute;
  height: 4px;
  width: 30px;
  transition: transform 400ms cubic-bezier(0.23, 1, 0.32, 1);
  border-radius: 2px;
}

.menu-button::before {
  content: '';
  margin-top: -8px;
}

.menu-button::after {
  content: '';
  margin-top: 8px;
}

#menu-toggle:checked + .menu-button-container .menu-button::before {
  margin-top: 0;
  transform: rotate(405deg);
}

#menu-toggle:checked + .menu-button-container .menu-button {
  background: rgba(255, 255, 255, 0);
}

#menu-toggle:checked + .menu-button-container .menu-button::after {
  margin-top: 0;
  transform: rotate(-405deg);
}

@media (max-width: 700px) {
  .menu-button-container {
    display: flex;
  }

  .menu {
    position: absolute;
    top: 0;
    margin-top: 130px;
    left: 0;
    flex-direction: column;
    width: 100%;
    justify-content: center;
  }

  #menu-toggle ~ .menu div {
    display: none;
  }

  #menu-toggle:checked ~ .menu div {
    display: flex;
    height: 1.5em;
    padding: 0.5em;
    transition: height 400ms cubic-bezier(0.23, 1, 0.32, 1);
  }

  #menu-toggle ~ .menu * {
    display: none;
  }

  #menu-toggle:checked ~ .menu * {
    display: flex;
    height: 1.5em;
    padding: 0.5em;
    transition: height 400ms cubic-bezier(0.23, 1, 0.32, 1);
  }

  .menu > p {
    display: flex;
    justify-content: left;
    width: 100%;
    background-color: white;
    color: #1e1e1e;
    margin: 0;
    padding: 0.5em;
    transition: height 400ms cubic-bezier(0.23, 1, 0.32, 1);
    border-bottom: 1px solid #f3f3f3;
  }

  .menu > p:first-child {
    border-top: 1px solid #f3f3f3;
  }
}

@media (max-width: 300px) {
  .menu > * {
    font-size: 15px;
  }
}

</style>

<template>
  <div class="LogoImage">
    <svg height="64" viewBox="0 0 64 64" width="64" xmlns="http://www.w3.org/2000/svg">
      <g fill="none" fill-rule="evenodd">
        <path
            d="m31.687 0 1.733 1.98-1.733 1.98c-15.313 0-27.726 12.414-27.726 27.727s12.413 27.726 27.726 27.726C47 59.413 59.413 47 59.413 31.687h3.961c0 17.5-14.186 31.687-31.687 31.687C14.187 63.374 0 49.188 0 31.687 0 14.187 14.187 0 31.687 0z"
            fill="#EA5256"/>
        <path
            d="m31.687 7.922 1.733 1.98-1.733 1.98c-10.938 0-19.804 8.867-19.804 19.805 0 10.938 8.866 19.805 19.804 19.805 10.938 0 19.805-8.867 19.805-19.805h3.96c0 13.125-10.64 23.766-23.765 23.766S7.922 44.813 7.922 31.687c0-13.125 10.64-23.765 23.765-23.765z"
            fill="#F79369"/>
        <path
            d="m31.687 15.844 1.733 1.98-1.733 1.98c-6.562 0-11.883 5.32-11.883 11.883 0 6.563 5.32 11.883 11.883 11.883 6.563 0 11.883-5.32 11.883-11.883h3.96c0 8.75-7.093 15.844-15.843 15.844s-15.843-7.094-15.843-15.844 7.093-15.843 15.843-15.843z"
            fill="#F9D367"/>
      </g>
    </svg>
    <div class="LogoText">
      <span class="Clockwise">
        CLOCKWISE
      </span>
      <br>
      <span class="Software">
        Software
      </span>
    </div>
  </div>
</template>

<script>

export default {
  name: "LogoImage",
}
</script>

<style scoped>
.LogoImage {
  margin-left: 25px;
  display: flex;
  background: white;
  height: 64px;
  object-fit: contain;
  justify-content: space-between;
  align-items: center;
}

.LogoText {
  text-align: left;
  margin-left: 25px;
}

.Clockwise {
  width: 80px;
  height: 16px;
  margin: 40px 0 48px 0;
  text-align: left;
  font-family: Catamaran-Black;
  font-size: 24px;
  font-weight: 900;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 0.08px;
  color: #1e1e1e;
}

.Software {
  width: 42px;
  text-align: left;
  height: 11px;
  margin: 0 0 40px 0;
  font-family: OpenSans, OpenSans, serif;
  font-size: 17px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: normal;
  letter-spacing: 0.07px;
  color: #1e1e1e;
}
@media screen and (max-width: 800px) {
  .LogoText {
    display: none;
  }
}
</style>

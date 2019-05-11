<template>
  <div class="layout">
    <div class="header">
      <n-link class="logo" to="/"><logo/></n-link>
    </div>
    <nuxt />
    <div class="footer">
      <div class="footer-inner">
        <p>
          <a target="_blank"
              rel="noopener noreferrer"
              href="https://github.com/tylermercer/nuxt-netlifycms-boilerplate">
            View this project on Github
          </a>
        </p>
        <p>
          <n-link to="/admin">
            NetlifyCMS Admin Login
         </n-link>
       </p>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo,
  }
}
</script>

<style>

.header, .footer {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  margin: 40px;
}

.footer-inner {
  background-color: whitesmoke;
  width: 600px;
  padding: 20px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.logo {
  display: block;
  margin: 0;
  padding: 0;
}

html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

a:link {
  color: #41b883;
}

a:visited {
  color: #3b8070;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>

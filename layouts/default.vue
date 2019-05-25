<template>
  <div class="layout">
    <div class="header">
      <!-- This link is an n-link because it links to another Nuxt route -->
      <n-link class="logo" to="/"><Logo/></n-link>
    </div>
    <nuxt class="content" />
    <div class="footer">
      <p>
        <!-- This link is not an n-link because it is external -->
        <a target="_blank"
            rel="noopener noreferrer"
            href="https://github.com/tylermercer/nuxt-netlifycms-boilerplate">
          View this project on Github
        </a>
      </p>
      <p>
        <!-- This is not an n-link because the NetlifyCMS admin page is static.
        If you make it an n-link, you'll get a "Page could not be found" when
        you click it. -->
        <a href="/admin">
          NetlifyCMS Admin Login
       </a>
     </p>
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
.layout {
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
  height: 100vh;
  padding: 40px 20px 10px 20px;
}

.header {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  width: 100%;
}
.content {
  margin-top: 40px;
  margin-bottom: 40px;
}

.footer {
  background-color: whitesmoke;
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.footer > * {
  padding: 20px;
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

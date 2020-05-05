<template>
  <fvMain>
    <fvContent>
      <fvHeader>
        <fvButton
          class="fv-margin-end fv-hidden-lg fv-hidden-xl"
          @click="toggleSidebar"
        >
          <i class="material-icons">menu</i>
        </fvButton>
        <div class="fv-margin-end">
          <FramevuerkLogo />
        </div>
        <div class="fv-grow">
          <h2 class="fv-hidden-xs">
            Reasonable Productivity
          </h2>
          <small class="fv-hidden-sm fv-hidden-xs">
            Life Management System
          </small>
        </div>
        <!-- <fvButton class="fv-margin-end" @click.prevent="toggleDocsMenu">
          <i class="material-icons">list</i>
          <span class="fv-hidden-xs fv-hidden-sm"> Documents </span>
          <fvMenu v-model="docsMenu">
            <div>
              <div class="fv-border-bottom fv-padding">
                <label class="fv-text-light">
                  <i class="material-icons">list</i> Documents
                </label>
              </div>
              <div class="fv-padding">
                <a
                  class="fv-link fv-block fv-margin-bottom"
                  target="_blank"
                  href="https://www.framevuerk.com/"
                  ><i class="material-icons">link</i> Framevuerk Docs</a
                >
                <a
                  class="fv-link fv-block fv-margin-bottom"
                  target="_blank"
                  href="https://github.com/framevuerk/framevuerk"
                  ><i class="material-icons">link</i> Framevuerk on Github</a
                >
                <a
                  class="fv-link fv-block fv-margin-bottom"
                  target="_blank"
                  href="https://nuxtjs.org/"
                  ><i class="material-icons">link</i> Nuxt Docs</a
                >
                <a
                  class="fv-link fv-block"
                  target="_blank"
                  href="https://github.com/nuxt/nuxt.js"
                  ><i class="material-icons">link</i> Nuxt on GitHub</a
                >
              </div>
            </div>
          </fvMenu>
        </fvButton>
        <fvButton class="fv-margin-end">
          <i class="material-icons">clear</i>
          <span class="fv-hidden-xs fv-hidden-sm"> Cancel </span>
        </fvButton>
        <fvButton>
          <i class="material-icons">done</i>
          <span class="fv-hidden-xs fv-hidden-sm"> Submit </span>
        </fvButton> -->
      </fvHeader>
      <div class="content fv-padding">
        <div class="fv-margin-bottom fv-hidden-xs fv-hidden-sm" />
        <div class="content__header fv-margin-bottom fv-padding">
          <div class="fv-padding fv-margin-bottom fv-text-center">
            <img src="clipboard.png" height="200" />
            <!-- <Logo /> -->
          </div>
          <h2>
            Reasonable Productivity is a life management system to handle all of
            the chaos in one place!
          </h2>
          <p>
            Contacts, reminders, lists, calendar, etc. Easy to use interface.
            Works across all your devices. Compatible with GTD, GSD, bullet
            journaling, and other popular task management methodologies.
          </p>
        </div>
        <div class="content__body fv-border fv-radius fv-shadow">
          <label class="fv-control-label fv-padding">
            <h3>Sign up to test our app when it launches!</h3>
          </label>
          <div class="fv-padding container">
            <form method="POST" action="https://formspree.io/email@email.com">
              <input
                type="hidden"
                name="_subject"
                value="Contact request from personal website"
              />
              <fvFormElement class="fv-col-md-12" label="Name">
                <fvInput v-model="exmps.name" placeholder="Enter Name" />
              </fvFormElement>
              <fvFormElement class="fv-col-md-12" label="Email">
                <fvInput
                  v-model="exmps.email"
                  type="email"
                  name="_replyto"
                  placeholder="Enter Email"
                  required
                />
              </fvFormElement>
              <fvButton
                type="submit"
                class="fv-primary fv-margin fv-margin-bottom"
              >
                Submit
              </fvButton>
            </form>
          </div>
        </div>
      </div>
    </fvContent>
  </fvMain>
</template>

<script>
import FramevuerkLogo from '~/components/FramevuerkLogo.vue'

export default {
  components: {
    FramevuerkLogo
  },
  data() {
    return {
      sidebar: false,
      docsMenu: false,
      slider: 'One',
      exmps: {
        name: '',
        email: ''
      }
    }
  },
  methods: {
    toggleSidebar() {
      this.sidebar = !this.sidebar
    },
    toggleDocsMenu() {
      setTimeout(() => {
        this.docsMenu = !this.docsMenu
      })
    }
  }
}
</script>

<style scoped>
.content {
  margin: 0 auto;
  max-width: 768px;
}
.sidebar {
  min-width: 300px;
}
</style>

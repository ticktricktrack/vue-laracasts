/*global Vue*/

Vue.component("message", {
  props: ["title", "body"],
  data() {
    return {
      isVisible: true,
    }
  },

  template: `
    <transition name="fade">
      <article class="message" v-show="isVisible">
        <div class="message-header">
          {{ title }}
          <button type="button" @click="isVisible = false" class="button is-danger is-small is-pulled-right">
            x
          </button>
        <div class="message-body">
          {{ body }}
        </div>
      </article>
    </transition
  `
})

new Vue({
  el: "#root",
});

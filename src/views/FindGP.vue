<template>
  <div class="nhsuk-width-container">
    <main id="main-content" class="nhsuk-main-wrapper">
      <div class="nhsuk-warning-callout">
        <h3 class="nhsuk-warning-callout__label">
          <span role="text">Mental Health Finder - API Evaluation App</span>
        </h3>
        <p>Results presented are for development and evaluation purposes only.</p>
      </div>

      <div class="nhsuk-u-reading-width">
        <h1>We need to know where your GP is</h1>
        <p>This is so we can get you to the right psychological therapies service.</p>
        <div class="nhsuk-form-group" :class="inputError ? 'nhsuk-form-group--error': ''" >
          <label class="nhsuk-label" for="Location">Enter the name of your GP surgery (or the street name):</label>
          <span v-if="inputError" class="nhsuk-error-message" id="example-error">You must enter the name of your GP find a service</span>
            <input
              class="nhsuk-input nhsuk-input--width-20"
              type="text"
              id="Location"
              name="Location"
              value=""
              @keyup.enter="onSearchEnter($event)"
              v-model="searchText"/>
            <p></p>
            <details class="nhsuk-details" nhsuk-polyfilled="true" id="nhsuk-details">
              <summary class="nhsuk-details__summary" 
                role="button" aria-controls="nhsuk-details__text0" tabindex="0" :aria-expanded="bPermissionNoteExapand">
                <span class="nhsuk-details__summary-text">Does my GP need to know?</span>
              </summary>
              <div class="nhsuk-details__text" id="nhsuk-details__text0" aria-hidden="false">
                  <p>The service will only tell your GP with your permission.</p>
                  <p>The only time they will contact your GP without your permission is if they believe you are at risk of harming yourself or other people.</p>                
              </div>
            </details>
        </div>
        <button
          @click="onSearchClick"
          class="nhsuk-button nhsuk-u-margin-bottom-4"
          type="submit">
          Continue
        </button>
      </div>
    </main>
  </div>
</template>

<script>
import { mapState } from "vuex";

export default {
  name: "FindGP",
  computed: {
    ...mapState("search", [
      "gpSearchResults",
    ]),
  },
  watch: {
    // eslint-disable-next-line no-unused-vars
    gpSearchResults(n, o) {
      if (n) {
        // Results available -> route to display them
        this.$router.push({ name: "FindGPSearchResults" });
      }
    },
  },
  methods: {
    // eslint-disable-next-line no-unused-vars
    onSearchEnter(event) {
      if (this.searchText.length > 0) {
        this.inputError = false;
        // this.searchText = this.searchText.replace(' ','+');
        this.$store.dispatch("search/postSearchGP", {
          search: this.searchText,
        });
      } else {
        this.inputError = true;
      }
    },
    onSearchClick() {
      if (this.searchText.length > 0) {
        this.inputError = false;
        // this.searchText = this.searchText.replace(' ','+');
        this.$store.dispatch("search/postSearchGP", {
          search: this.searchText,
        });
      } else {
        this.inputError = true;
      }
    },
  },
  data: () => ({
    searchText: "",
    inputError: false,
    bPermissionNoteExapand: false
  }),
  mounted() {
    this.searchText = "";
    this.$store.dispatch("search/resetFinder");
  },
};
</script>

<style>
</style>

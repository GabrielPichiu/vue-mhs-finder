<template>
  <header class="nhsuk-header" role="banner">
    <div class="nhsuk-width-container nhsuk-header__container">
      <div class="nhsuk-header__logo">
        <a class="nhsuk-header__link"
          href="/find-gp"
          aria-label="NHS homepage">
          <svg
            class="nhsuk-logo"
            xmlns="http://www.w3.org/2000/svg"
            role="presentation"
            focusable="false"
            viewBox="0 0 40 16"
          >
            <path class="nhsuk-logo__background" d="M0 0h40v16H0z"></path>
            <path
              class="nhsuk-logo__text"
              d="M3.9 1.5h4.4l2.6 9h.1l1.8-9h3.3l-2.8 13H9l-2.7-9h-.1l-1.8 9H1.1M17.3 1.5h3.6l-1 4.9h4L25 1.5h3.5l-2.7 13h-3.5l1.1-5.6h-4.1l-1.2 5.6h-3.4M37.7 4.4c-.7-.3-1.6-.6-2.9-.6-1.4 0-2.5.2-2.5 1.3 0 1.8 5.1 1.2 5.1 5.1 0 3.6-3.3 4.5-6.4 4.5-1.3 0-2.9-.3-4-.7l.8-2.7c.7.4 2.1.7 3.2.7s2.8-.2 2.8-1.5c0-2.1-5.1-1.3-5.1-5 0-3.4 2.9-4.4 5.8-4.4 1.6 0 3.1.2 4 .6"
            ></path>
            <image src="https://assets.nhs.uk/images/nhs-logo.png" xlink:href=""></image>
          </svg>
        </a>
      </div>
      <span class="small">&nbsp;{{version}}</span>
    </div>

    <nav
      class="nhsuk-header__navigation"
      id="header-navigation"
      role="navigation"
      aria-label="Primary navigation"
      aria-labelledby="label-navigation"
    >
      <div class="nhsuk-width-container">
        <p class="nhsuk-header__navigation-title">
          <span id="label-navigation">Menu</span>
          <button class="nhsuk-header__navigation-close" id="close-menu">
            <svg
              class="nhsuk-icon nhsuk-icon__close"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 24 24"
              aria-hidden="true"
              focusable="false"
            >
              <path
                d="M13.41 12l5.3-5.29a1 1 0 1 0-1.42-1.42L12 10.59l-5.29-5.3a1 1 0 0 0-1.42 1.42l5.3 5.29-5.3 5.29a1 1 0 0 0 0 1.42 1 1 0 0 0 1.42 0l5.29-5.3 5.29 5.3a1 1 0 0 0 1.42 0 1 1 0 0 0 0-1.42z"
              ></path>
            </svg>
            <span class="nhsuk-u-visually-hidden">Close menu</span>
          </button>
        </p>
        <ul class="nhsuk-header__navigation-list">
          <li
            class="
              nhsuk-header__navigation-item
              nhsuk-header__navigation-item--for-mobile
            "
          >
            <a class="nhsuk-header__navigation-link" href="">
              Home
              <svg
                class="nhsuk-icon nhsuk-icon__chevron-right"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                aria-hidden="true"
              >
                <path
                  d="M15.5 12a1 1 0 0 1-.29.71l-5 5a1 1 0 0 1-1.42-1.42l4.3-4.29-4.3-4.29a1 1 0 0 1 1.42-1.42l5 5a1 1 0 0 1 .29.71z"
                ></path>
              </svg>
            </a>
          </li>
          <li class="nhsuk-header__navigation-item">
            <a
              class="nhsuk-header__navigation-link"
              href=""
            >
              Health A-Z
              <svg
                class="nhsuk-icon nhsuk-icon__chevron-right"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                aria-hidden="true"
              >
                <path
                  d="M15.5 12a1 1 0 0 1-.29.71l-5 5a1 1 0 0 1-1.42-1.42l4.3-4.29-4.3-4.29a1 1 0 0 1 1.42-1.42l5 5a1 1 0 0 1 .29.71z"
                ></path>
              </svg>
            </a>
          </li>
          <li class="nhsuk-header__navigation-item">
            <a
              class="nhsuk-header__navigation-link"
              href=""
            >
              Live Well
              <svg
                class="nhsuk-icon nhsuk-icon__chevron-right"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                aria-hidden="true"
              >
                <path
                  d="M15.5 12a1 1 0 0 1-.29.71l-5 5a1 1 0 0 1-1.42-1.42l4.3-4.29-4.3-4.29a1 1 0 0 1 1.42-1.42l5 5a1 1 0 0 1 .29.71z"
                ></path>
              </svg>
            </a>
          </li>
          <li class="nhsuk-header__navigation-item">
            <a
              class="nhsuk-header__navigation-link"
              href=""
            >
              Mental health
              <svg
                class="nhsuk-icon nhsuk-icon__chevron-right"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                aria-hidden="true"
              >
                <path
                  d="M15.5 12a1 1 0 0 1-.29.71l-5 5a1 1 0 0 1-1.42-1.42l4.3-4.29-4.3-4.29a1 1 0 0 1 1.42-1.42l5 5a1 1 0 0 1 .29.71z"
                ></path>
              </svg>
            </a>
          </li>
          <li class="nhsuk-header__navigation-item">
            <a
              class="nhsuk-header__navigation-link"
              href=""
            >
              Care and support
              <svg
                class="nhsuk-icon nhsuk-icon__chevron-right"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                aria-hidden="true"
              >
                <path
                  d="M15.5 12a1 1 0 0 1-.29.71l-5 5a1 1 0 0 1-1.42-1.42l4.3-4.29-4.3-4.29a1 1 0 0 1 1.42-1.42l5 5a1 1 0 0 1 .29.71z"
                ></path>
              </svg>
            </a>
          </li>
          <li class="nhsuk-header__navigation-item">
            <a
              class="nhsuk-header__navigation-link"
              href=""
            >
              Pregnancy
              <svg
                class="nhsuk-icon nhsuk-icon__chevron-right"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                aria-hidden="true"
              >
                <path
                  d="M15.5 12a1 1 0 0 1-.29.71l-5 5a1 1 0 0 1-1.42-1.42l4.3-4.29-4.3-4.29a1 1 0 0 1 1.42-1.42l5 5a1 1 0 0 1 .29.71z"
                ></path>
              </svg>
            </a>
          </li>
          <li class="nhsuk-header__navigation-item">
            <a
              class="nhsuk-header__navigation-link"
              href=""
            >
              NHS services
              <svg
                class="nhsuk-icon nhsuk-icon__chevron-right"
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 24 24"
                aria-hidden="true"
              >
                <path
                  d="M15.5 12a1 1 0 0 1-.29.71l-5 5a1 1 0 0 1-1.42-1.42l4.3-4.29-4.3-4.29a1 1 0 0 1 1.42-1.42l5 5a1 1 0 0 1 .29.71z"
                ></path>
              </svg>
            </a>
          </li>
          <li>
            <img src="@/assets/data-explorer.png" style="float:right;width:30px;height:30px;cursor:pointer;margin-top: 12px;" @click="exploreData()">
          </li>
        </ul>
      </div>
    </nav>
  </header>
</template>

<script>
import { mapState } from "vuex";

export default {
  name: "Header",
  computed: {
    ...mapState("app", ["version"]),
  },
  methods: {
    exploreData() {
      this.$router.push({ name: "DataExplorer" });
    }
  }
}
</script>


<style>
span.small {
  color : yellow;
  font-size: 14px;
  font-weight: 600;
  padding-top: 10px;
}
</style>

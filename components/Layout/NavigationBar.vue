<template>
  <!-- Navigation -->
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark fixed-top">
    <div class="container">
      <NuxtLink class="navbar-brand" :to="localePath('/')">
        <img src="/img/icon.png" style="width: calc(20px + 0.1rem)" />
        <span>&nbsp;PoliNetwork PC 💻</span>
      </NuxtLink>
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarResponsive"
        aria-controls="navbarResponsive"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarResponsive">
        <ul class="navbar-nav ml-auto">
          <li class="nav-item active">
            <a class="nav-link" :href="'/' + $i18n.locale + '/'">
              Home 🏠
              <span class="sr-only">(current)</span>
            </a>
          </li>

          <li class="nav-item">
            <NuxtLink :to="localePath('/contact-us')" class="nav-link"
              >{{ $t("Contatti") }} 💬</NuxtLink
            >
          </li>
          <li class="nav-item">
            <div
              style="
                border: 1px solid #00000029;
                margin: auto;
                border-radius: 10px;
              "
            >
              <table style="display: inline">
                <tr>
                  <td>
                    <NuxtLink :to="switchLocalePath('it')"
                      ><img src="/img/it.png" style="width: 35px; padding: 6px"
                    /></NuxtLink>
                  </td>
                  <td>
                    <NuxtLink :to="switchLocalePath('en')"
                      ><img src="/img/en.png" style="width: 35px; padding: 6px"
                    /></NuxtLink>
                  </td>
                </tr>
              </table>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>


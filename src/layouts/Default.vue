<template>
  <v-app>
    <v-navigation-drawer permanent fixed>
      <v-list-item>
        <!-- <v-list-item-avatar>
              <v-img src="/Users/paigewalters/Desktop/Vue3Projects/gridsome-portfolio/portfolio-app/src/portfolioPic.jpg"></v-img>
            </v-list-item-avatar> -->
        <v-list-item-content>
          <v-list-item-title class="title">
            Paige Walters
          </v-list-item-title>
          <v-list-item-subtitle>
            Software Developer
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list
        dense
        nav
      >
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
          :to="`#${item.title.toLowerCase().replace(' ', '-')}`"
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-main>
      <v-container>
    <slot/>
    </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
    data () {
      return {
        items: [
          { title: 'About', icon: 'mdi-account' },
          { title: 'Projects', icon: 'mdi-apps' },
          { title: 'Education', icon: 'mdi-school-outline' },
          { title: 'Contact', icon: 'mdi-phone-outline' },
        ],
        right: null,
      }
    },
  }
</script>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
.v-application--wrap {
  flex-direction: row;
}

.v-main {
  margin-left: 20em;
  flex: 1 0;
}

</style>

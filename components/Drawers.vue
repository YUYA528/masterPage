<template>
    <v-app>
    <v-container>
    <v-list-item>
        <v-list-item-content>
        <v-list-item-title class="text-h6">
            <v-avatar
                color="teal"
                size="51"
            ></v-avatar>
            <div>Application</div>
        </v-list-item-title>
        <v-list-item-subtitle>
            subtext
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
        >
        <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
        </v-list-item-icon>

        <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item-content>
        </v-list-item>
    </v-list>
    </v-container>
    <v-footer app padless>
    <v-col
      class="text-center"
      cols="12"
    >
      {{ new Date().getFullYear() }} — <strong>VuetifyApp</strong>
    </v-col>
  </v-footer>
</v-app>
</template>

<script>
    export default {
      data () {
        return {
          props: ['to'],
          items: [
            { title: 'ようこそ', icon: 'mdi-view-dashboard', to:"/index" },
            { title: 'SNS', icon: 'mdi-image', to:"/inspire" },
            { title: 'お問い合わせ', icon: 'mdi-help-box', to:"/form" },
          ],
          right: null,
        }
      },
    }
  </script>
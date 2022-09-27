<template>
  <v-app>
    <v-app-bar app color="primary" dense dark>
      <v-btn href="/" text>
        <span class="mr-2">IOfree.xyz</span>
      </v-btn>
      <v-spacer></v-spacer>
      <v-btn :href=blog target="_blank" text>
        <span class="mr-2">blog</span>
      </v-btn>
    </v-app-bar>

    <v-main>
      <Home/>
    </v-main>

    <v-footer color="white">
      <v-card-text class="text-center">
        <a href="https://beian.miit.gov.cn/" target="_blank">苏ICP备2022013870号-1</a>
        | &copy; {{ new Date().getFullYear() }}

        <v-btn :href=i.href v-for="i in info" :key="i" target="_blank" icon>
          <v-icon size="20px">{{ i.icon }}</v-icon>
        </v-btn>
      </v-card-text>
    </v-footer>
  </v-app>
</template>

<script>
import Home from './components/home';

export default {
  name: 'App',

  components: {
    Home,
  },

  data: () => ({
    domain: "iofree.xyz",
    blog: "https://blog.iofree.xyz",

    info: [
      {
        icon: 'mdi-twitter',
        href: 'https://twitter.com/Allen_Xuxu',
      },
      {
        icon: 'mdi-email',
        href: 'mailto:admin@iofree.xyz',
      },
    ],
  }),
};
</script>

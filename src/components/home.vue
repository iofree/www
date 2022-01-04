<template>
  <v-container>
    <v-row class="text-center">
      <v-col class="my-16 py-16">
        <h1 class="display-2 font-weight-bold">{{ title }}</h1>
      </v-col>

      <v-col class="mb-5" cols="12">
        <h2 class="headline font-weight-bold mb-3">我的作品</h2>

        <v-list-item v-for="(p, i) in production" :key="i">
          <v-list-item-content>
            <v-btn :href="p.href" target="_blank" text>
              <span class="font-weight-black">{{ p.text }}</span>
              - {{ p.subtitle }}
            </v-btn>
          </v-list-item-content>
        </v-list-item>
      </v-col>

    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'Home',

  data: () => ({
    title: '几时归去做个闲人',

    production: [
      {
        text: '不忘提醒',
        subtitle: '让你不忘记任何一件小事',
        href: 'https://reminder.iofree.xyz',
      },
    ],
  }),
}
</script>

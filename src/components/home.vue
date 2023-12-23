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
              <span class="font-weight-black text-decoration-underline">{{ p.text }}</span>
              - {{ p.subtitle }}
            </v-btn>
          </v-list-item-content>
        </v-list-item>
      </v-col>

      <v-col class="mb-5" cols="12">
        <h2 class="headline font-weight-bold mb-3">开源项目</h2>
        <v-list-item v-for="(p, i) in openSourceProject" :key="i">
          <v-list-item-content>
            <v-btn :href="p.href" target="_blank" text>
              <span class="text-capitalize font-weight-black text-decoration-underline">{{ p.text }}</span>
              - <span class="text-capitalize">{{ p.subtitle }}</span>
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
        text: '人生笔记',
        subtitle: '用图文,视频,录音日记一生',
        href: 'https://lifelog.iofree.xyz/',
      },
      {
        text: '人生规划局',
        subtitle: '帮助你规划自己的人生',
        href: 'https://planning.iofree.xyz/',
      },
      {
        text: '不忘提醒',
        subtitle: '帮助你不忘记任何一件小事',
        href: 'https://reminder.iofree.xyz',
      },
    ],
    openSourceProject: [
      {
        text: 'gev',
        subtitle: '比标准库更快的 TCP 网络库',
        href: 'https://github.com/Allenxuxu/gev',
      },
    ],
  }),
}
</script>

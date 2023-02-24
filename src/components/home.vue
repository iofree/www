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
        text: '不忘提醒',
        subtitle: '帮助你不忘记任何一件小事',
        href: 'https://reminder.iofree.xyz',
      },
      {
        text: '人生笔记',
        subtitle: '离线私人朋友圈，写日记,贴视频,贴照片,永久保存',
        href: 'https://lifelog.iofree.xyz/',
      },
      {
        text: '友窗',
        subtitle: '分享你的心动时刻到好友桌面',
        href: 'https://apps.apple.com/cn/app/id1614830371',
      },
      {
        text: 'Doit TODO',
        subtitle: '支持多项目分类管理，支持日历视角，习惯打卡，通知提醒的 TODO 工具',
        href: 'https://apps.apple.com/cn/app/id1623401995',
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

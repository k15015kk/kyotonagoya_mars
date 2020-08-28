<template>
  <v-container fluid class="bg">
    <v-row>
      <v-col cols="12" class="text-center pa-0">
        <v-row>
          <v-col cols="12" class="text-center pt-8 pl-8 pr-8 pb-4">
            <v-btn
              class="text-h2 font-weight-bold white--text"
              color="orange darken-2"
              height="180"
              elevation="8"
              style="text-transform: none"
              block
              >Welcome to OSAKA
            </v-btn>
          </v-col>

          <v-col
            v-for="(item, i) in items"
            :key="i"
            cols="12"
            sm="6"
            md="3"
            class="text-center pt-4 pl-8 pr-8 pb-8"
          >
            <v-btn
              height="60"
              class="text-h5 font-weight-bold black--text"
              color="grey lighten-4"
              style="text-transform: none"
              :href="item.href"
              target="_blank"
              block
            >
              <v-img
                :src="item.icon"
                height="48"
                max-width="48"
                aspect-ratio="1"
                contain
              ></v-img>
              {{ item.title }}
            </v-btn>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<style scoped>
.bg {
  background-image: url('~@/assets/img/tokyostation.jpg');
  height: 100%;
  width: 100%;
  background-size: cover;
}
</style>

<script>
export default {
  data() {
    return {
      image_src: require('@/assets/img/tokyostation.jpg'),
      items: [
        {
          icon: require('@/assets/img/Twitter_Logo_Blue.png'),
          title: 'Twitter',
          href: 'https://twitter.com/kyotonagoya1476',
        },
        {
          icon: require('@/assets/img/IG_Glyph_Fill.png'),
          title: 'Instagram',
          href: 'https://www.instagram.com/kyoto.nagoya',
        },
        {
          icon: require('@/assets/img/logo_symbol.png'),
          title: 'note',
          href: 'https://note.com/kyoto_nagoya',
        },
        {
          icon: require('@/assets/img/hatenablog-logo.png'),
          title: 'BLOG',
          href: 'https://kyoto-nagoya.hatenablog.com/',
        },
      ],
    }
  },
}
</script>

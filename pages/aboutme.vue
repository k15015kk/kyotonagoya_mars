<template>
  <v-container>
    <v-row>
      <v-col cols="12" class="pl-8 pr-8">
        <v-card class="mx-auto" max-width="640px">
          <div class="text-center pt-8">
            <v-avatar size="144px">
              <v-img :src="profile_img" alt="Haruki Inoue" />
            </v-avatar>
          </div>
          <v-card-text>
            <h1 class="text-h4 text-center pb-4">Haruki Inoue</h1>
            <p>
              千葉県流山市に住んでおり，東京に出勤している社会人初心者です．位置情報のアプリケーションに関する仕事をしています．最近はスマートフォアプリの開発とWebアプリケーションの開発をしています．週末は公共交通機関を使ってお出かけをしています．乗ることがお出かけのメインです．あと，よくヒトカラに行きます．
            </p>
            <h5 class="text-h5">Profile</h5>
            <!-- <div class="pt-2 pb-2">
              <span class="font-weight-bold pr-4">所属</span>
              <br />
              東京のどこかにいます
            </div> -->
            <div class="pt-2 pb-2">
              <span class="font-weight-bold pr-4">居住地</span>
              <br />
              千葉県流山市
            </div>
            <div class="pt-2 pb-2">
              <span class="font-weight-bold pr-4">出身地</span>
              <br />
              愛知県豊橋市
            </div>
            <div class="pt-2 pb-2">
              <span class="font-weight-bold pr-4">誕生日</span>
              <br />
              1997-01-17
            </div>
            <div class="pt-2 pb-2">
              <span class="font-weight-bold pr-4">趣味</span>
              <br />
              公共交通機関を使ってお出かけ/カラオケ
            </div>
            <div class="pt-2 pb-2">
              <span class="font-weight-bold pr-4">好きなアニメ</span>
              <ul>
                <li>ひだまりスケッチ</li>
                <li>三ツ星カラーズ</li>
                <li>恋する小惑星</li>
              </ul>
            </div>
            <div class="pt-2 pb-2">
              <span class="font-weight-bold pr-4">好きな電車</span>
              <br />最近は つくばエクスプレス
              によく乗っています．どちらかというと新しい列車の方が好きですが，古い列車も乗りに行きます．
            </div>
            <div class="pt-2 pb-2">
              <span class="font-weight-bold pr-4"
                >いままで使っていた言語・技術</span
              >
              <ul>
                <li>Swift(iOS)</li>
                <li>Kotlin(Android)</li>
                <li>JavaScript(Node.js/Express)</li>
                <li>Python</li>
                <li>Ruby(Ruby on Rails)</li>
              </ul>
            </div>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      profile_img: require('@/assets/img/my_identity.png'),
    }
  },
}
</script>

<template>
  <v-container>
    <v-row>
      <v-col cols="12" class="pl-8 pr-8">
        <v-card class="mx-auto" max-width="640px">
          <div class="text-center pt-8">
            <v-avatar size="180px">
              <v-img :src="profile_img" alt="Haruki Inoue" />
            </v-avatar>
          </div>
          <v-card-text>
            <h1 class="text-h2 text-center pb-4">Haruki Inoue</h1>
            <p>
              情報科学を専攻している大学院修士2年です．公共交通機関と位置情報アプリを絡めた研究をしています．最近はスマートフォアプリの開発とWebアプリケーションの開発をしています．週末は公共交通機関を使ってお出かけをしています．乗ることがお出かけのメインです．あと，よくヒトカラに行きます．2021年から千葉県内のどこかに住みます．
            </p>
            <h5 class="text-h5">Profile</h5>
            <div class="pt-2 pb-2">
              <span class="font-weight-bold pr-4">所属</span>
              <br />
              愛知工業大学大学院 経営情報科学専攻 修士2年
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
              <br />多すぎて決められない
            </div>
            <div class="pt-2 pb-2">
              <span class="font-weight-bold pr-4">使ってる言語・技術</span>
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
      profile_img: require('@/assets/img/my_face.jpg'),
    }
  },
}
</script>

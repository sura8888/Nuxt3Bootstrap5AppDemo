<template>
  <div class="container text-center my-5">
    <h1>{{ data.title }}</h1>
    <div class="alert alert-primary" role="alert">{{ data.description }}</div>
  </div>
  <div class="container mb-5">
    <div class="card mb-3 mx-auto">
      <div class="row g-0">
        <div class="col-md-4">
          <img
            src="~/assets/img/kenta.png"
            class="img-fluid rounded-start" alt="...">
        </div>
        <div class="col-md-8">
          <div class="card-body">
            <h5 class="card-title">{{data.zairyo}}</h5>
            
            <div class="card-text">
              <ul>
                <li v-for="item in data.material">{{ item.text }}</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="container mb-5">
    <h2>{{ data.make }}</h2>
    <div>
    <ol class="custom-list row row-cols-1 row-cols-sm-2 row-cols-md-4">
      <li class="col border p-2" v-for="(item, index) in data.making" :key="item.id">
        <span v-html="item.text"></span>
    </li>
    </ol>
  </div>
    <div class="row row-cols-1 row-cols-sm-2 row-cols-md-4">
    </div>
    <ol>

    </ol>
  </div>
  <div class="container mb-5">
    <div class="row gx-5">
      <div class="col-sm">
        <h3>コツ・ポイント</h3>

        <p>揚げる際鍋底での焦げ防止に衣が軽く揚がるまで菜箸等で時々浮かせて下さい</p>
        <p>好みで粉類に粗びき黒胡椒小さじ1/2を足しても◎</p>
        <p>にんにくチューブ２センチはガーリックパウダー小さじ１に変えて粉類と混ぜても美味しいです。</p>
        <p>パプリカパウダーは無くても可</p>
      </div>
      <div class="col-sm">
        <h3>このレシピの生い立ち</h3>

        <p>今まで作ったKFCレシピは、卵液や粉もかなり余るし、何よりも
          何かひと味足りない……と思って、やっとKFC味にたどり着きました！</p>
        <p>どの家庭にもあるような材料で☆</p>
        <p>牛乳と卵液、粉類も必要量のみになっているので無駄が無く経済的です☆</p>
      </div>
    </div>
  </div>
</template>
<style>
.custom-list {
  list-style-position: inside; /* リストアイテムの数字を内側に配置 */
  padding-left: 0; /* リストアイテムの左の余白を削除 */
}
</style>
<script setup>
 const data = useRecipe()
</script>

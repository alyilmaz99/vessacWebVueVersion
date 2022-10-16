<template>
  <section class="scene-intro" id="intro">
    <div class="static-container">
      <h1 class="title">
        <span class="iuri">Vessac</span>
        <span class="func">.gameStudio()</span>
      </h1>

      <TextBlock>
        <p class="-purple">Game Development</p>
        <p class="-gray">Hayallerimizi Oyunlaştırıyoruz</p>
      </TextBlock>
    </div>
  </section>
</template>

<script>
import TextBlock from '../TextBlock.vue'

export default {
  name: 'IntroScene',
  components: { TextBlock },
}
</script>

<template>
  <div class="earlyDays">
    <TitleSection scene="earlyTitle">
      <TitleFunction
        params="2022,2023"
        subtitle="&lt;hızlı&gt;&lt;planlı&gt;&lt;efektif&gt;..."
        >kısaDönemPlanlar</TitleFunction
      >

      <div class="clouds cloud-1"></div>
      <Pepe v-bind="{ isPlaying }" />
      <div class="clouds cloud-2"></div>
      <div class="clouds cloud-3"></div>
      <Ocean v-bind="{ isPlaying }" />
    </TitleSection>

    <SceneSection id="early-days">
      <TextBlock>
        <p>Geliştirme & Yayınlama.</p>
        <p class="-big">
         Halihazırda planladığımız oyunları<br />
          <span class="-purple">önümüzdeki süreçte hızlı ve emin adımlarla</span>
        yayınlamaya devam edeceğiz.
        </p>
      </TextBlock>
    </SceneSection>
    <SceneSection id="early-days2">
      <TextBlock>
        <p class="-big">
          <span class="-purple">Freelance</span> &
          <span class="-purple">startup,</span><br />
          <span class="-purple">İnçler</span> &
          <span class="-purple">pikseller.</span>
        </p>
        <p>
          Freelance projeler ile müşteri odaklı çalışmaya hakim olduğumuzdan geliştirdiğimiz, startup projelerimizde ve oyun projelerimizde kullanıcı kitlesinin isteklerini karşılayacak tecrübe ve birikeme sahibiz.<br />
        </p>
      </TextBlock>
    </SceneSection>
    <SceneSection id="early-days3">
      <TextBlock>
        <p>
          Ulu Önder Mustafa Kemal Atatürk'ün<br />
          sözleri bu yolda bize yol gösterici oldu:
          <span class="-big -purple"
            ><em>Yerinde duran</em>, <em>geriye gidiyor demektir</em>. İleri,
            <em>daima ileri...</em></span
          >
          
        </p>
      </TextBlock>
    </SceneSection>
  </div>
</template>

<script>
import Pepe from '../Characters/Pepe/Pepe.vue'
import Ocean from '../Characters/Ocean/Ocean.vue'
import TitleSection from '../TitleSection.vue'
import TitleFunction from '../TitleFunction.vue'
import TextBlock from '../TextBlock.vue'
import SceneSection from '../SceneSection.vue'

export default {
  name: 'EarlyDaysScene',
  components: {
    TitleSection,
    Pepe,
    Ocean,
    TitleFunction,
    TextBlock,
    SceneSection,
  },
  props: {
    isPlaying: Boolean,
  },
}
</script>

<style lang="scss">
.earlyDays {
  .pepe {
    position: absolute;
    z-index: 2;
    top: 50%;
    left: 100%;
    transform: scale(0.4) translate3d(0, -50%, 0);
    transform-origin: 0 0;

    @media screen and (max-width: 568px) {
      transform: scale(0.2) translate3d(0, -50%, 0);
    }
  }

  .clouds {
    position: absolute;
    width: 150vw;
    height: 150vh;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    transform-origin: 50% 50%;
    background: url('../Characters/Pepe/assets/clouds-1.png') no-repeat center;
    background-size: contain;
    opacity: 0.5;

    &.cloud-2 {
      background-image: url('../Characters/Pepe/assets/clouds-2.png');
    }

    &.cloud-3 {
      background-image: url('../Characters/Pepe/assets/clouds-3.png');
      width: 100vw;
      height: 100vh;
      z-index: -1;
      opacity: 0.25;
    }
  }
}
</style>

<template>
    <section class="project-description">
        <h1 class="project-description__title">{{ projectDetail.title }}</h1>
        <p class="project-description__text">{{ projectDetail.text }}</p>
        <div class="project-description__img-box">
            <img :src="require('../../assets/' + projectDetail.image)" :alt="projectDetail.title" class="project-description__img">
            <svg class="project-description__zoom" width="172" height="172" viewBox="0 0 172 172" fill="none" xmlns="http://www.w3.org/2000/svg">
            <g filter="url(#filter0_d_1418_52)">
            <circle cx="86" cy="76" r="66" fill="white"/>
            <path d="M104.433 90.2861L96.0452 81.8984C98.0646 79.21 99.1547 75.9378 99.151 72.5755C99.151 63.9872 92.1638 57 83.5755 57C74.9872 57 68 63.9872 68 72.5755C68 81.1638 74.9872 88.151 83.5755 88.151C86.9378 88.1547 90.21 87.0646 92.8984 85.0452L101.286 93.4329C101.711 93.8125 102.264 94.0151 102.834 93.9991C103.403 93.9832 103.945 93.7499 104.347 93.3472C104.75 92.9445 104.983 92.403 104.999 91.8337C105.015 91.2644 104.812 90.7107 104.433 90.2861ZM72.4501 72.5755C72.4501 70.3751 73.1026 68.2242 74.3251 66.3946C75.5476 64.565 77.2851 63.1391 79.318 62.297C81.3509 61.455 83.5879 61.2346 85.746 61.6639C87.9041 62.0932 89.8864 63.1528 91.4423 64.7087C92.9983 66.2646 94.0578 68.247 94.4871 70.4051C94.9164 72.5632 94.6961 74.8001 93.854 76.833C93.012 78.8659 91.586 80.6035 89.7564 81.8259C87.9269 83.0484 85.7759 83.7009 83.5755 83.7009C80.626 83.6974 77.7982 82.5241 75.7126 80.4384C73.627 78.3528 72.4537 75.5251 72.4501 72.5755Z" fill="#CDA274"/>
            </g>
            <defs>
            <filter id="filter0_d_1418_52" x="0" y="0" width="172" height="172" filterUnits="userSpaceOnUse" color-interpolation-filters="sRGB">
            <feFlood flood-opacity="0" result="BackgroundImageFix"/>
            <feColorMatrix in="SourceAlpha" type="matrix" values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0" result="hardAlpha"/>
            <feOffset dy="10"/>
            <feGaussianBlur stdDeviation="10"/>
            <feComposite in2="hardAlpha" operator="out"/>
            <feColorMatrix type="matrix" values="0 0 0 0 0.752941 0 0 0 0 0.752941 0 0 0 0 0.752941 0 0 0 0.25 0"/>
            <feBlend mode="normal" in2="BackgroundImageFix" result="effect1_dropShadow_1418_52"/>
            <feBlend mode="normal" in="SourceGraphic" in2="effect1_dropShadow_1418_52" result="shape"/>
            </filter>
            </defs>
            </svg>
        </div>
    </section>
</template>

<script>
  import { mapGetters, mapActions } from 'vuex';

  export default {
    name: 'ProjectDescriptionComp',
    mounted() {
      this.fetchProjectDetail()
    },
    computed: {
      ...mapGetters(['projectDetail'])
    },
    methods: {
      ...mapActions(['fetchProjectDetail']),
    }
  }
</script>

<style scoped lang="scss">
  .project-description {
    width: 1200px;
    margin: 200px auto;

    &__title {
      display: block;
      width: 658px;
      margin: 0px auto 11px auto;
      color: #292F36;
      font-family: DM Serif Display;
      font-size: 50px;
      font-style: normal;
      font-weight: 400;
      line-height: 62.5px;
      letter-spacing: 1px;
    }
    &__text {
      display: block;
      width: 658px;
      margin: 0px auto 100px auto;
      color: #4D5053;
      font-family: Jost;
      font-size: 22px;
      font-style: normal;
      font-weight: 400;
      line-height: 33px;
      letter-spacing: 0.22px;
    }
    &__img-box {
      position: relative;
    }
    &__img {
      width: 100%;
      height: auto;
      border-radius: 70px;
    }
    &__zoom {
      position: absolute;
      left: 0;
      right: 0;
      top: 0;
      bottom: 0;
      margin: auto;
      cursor: pointer;
    }
  }
  </style>

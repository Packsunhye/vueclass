<template>
     <section id="imageType" :class="attr" class="image__wrap">
        <h2>{{ top.title }}</h2>
        <p>{{ top.desc }}</p>
        <div :class="layout" class="image__inner">
            <article class="image img1" 
            :class="text.class"
            v-for="text in titles"
            v-bind:key="text.key">
                <h3 class="image__title">{{ text.title }}</h3>
                <p class="image__desc">{{ text.desc }}</p>
                <a class="image__btn" href="/" title="자세히 보기">{{ text.more }}</a>
            </article>
        </div>
    </section>
</template>

<script>
export default {
  props: {
    attr: String,
    layout : String,
  },
  data: function () {
        return {
          top: {
            title: "해파리들이 둥둥 떠다니는 모습",
            desc: "정해진 갈 길 없이 흘러가는 대로 움직이다보면 새로운 만남이 있어요.",
          },
          titles: [
            {
              title: "화려한 모습의 해파리",
              desc: "색감과 그 화려한 치마와 같은 구완들이 바다속에서 자유롭게 있어요, 만지면 돌이킬 수 없을 정도로 아프니 주의합시다.",
              more: "더 자세히 보기",
              class : "img1",
            },
            {
              title: "동그란 모습의 해파리",
              desc: "콕, 찔러보아 젤리처럼 부드럽게 흐물거리는 모습을 보고싶지만 해파리 주변엔 해파리들이 가득있어요 바라보기만 합시다.",
              more: "더 자세히 보기",
              class : "img2",
            },
          ],
        };
    },
}
</script>

<style>
/* img type */

.image__inner {
    display: flex;
    justify-content: space-between;
}
.image {
    width: 49%;
    height: 370px;
    color: #fff;
    padding: 200px 30px 30px 30px;
    box-sizing: border-box;
    overflow: hidden;
    transition: all 0.15s ease-in-out;
}
.image.img1 {
    background: url(../../assets/img/imgType01_01.png) no-repeat center;
    
}
.image.img2 {
    background: url(../../assets/img/imgType01_02.png) no-repeat center;
}
.image.img1:hover,.image.img2:hover  {
    transform: scale(1.01);
    filter: brightness(110%);
    
}
.image__title {
    font-size: 32px;
    margin-bottom: 10px;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
}
.image__desc {
    font-size: 16px;
    font-weight: 300;
    margin-bottom: 10px;
    line-height: 1.5;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
}
.image__btn {
    font-size: 16px;
    color: #fff;
    background-color: #1f1d94af;
    padding: 10px 20px;
    display: inline-block;
}
.image__btn.yellow {
    background-color: #626cc9b6;
}

@media(max-width: 960px){}
@media(max-width: 600px){
    .image__inner {
        flex-direction: column;
    }
    .image {
        width: 100%;
        padding: 205px 20px 20px 20px;
    }
    .image:first-child {
        margin-bottom: 20px;
    }
    .image__title {
        font-size: 24px;
    }
    .image__desc {
        font-size: 16px;
    }
}
</style>
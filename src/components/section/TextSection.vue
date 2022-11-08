<template>
    <section id="textType" class="text__wrap" :class ="attr">
        <span>텍스트 유형 01</span>
        <h2 class="mb70">해파리의 신기한 이야기들</h2>
        <div class="text__inner" :class ="layout">
            <div class="text"
            :class="text.class"
            v-for="text in titles"
            v-bind:key="text.key"
            >
                <h3 class="text__title">{{ text.title }}</h3>
                <p class="text__desc">{{ text.desc }}</p>
                <a class="text_btn" href="/">{{ text.amore }}</a>
            </div>
        </div>
    </section> 
</template>

<script>
export default {
    props: {
        attr: String,
        layout: String,
    },
    data: function () {
    return {
      top: {
        span: "텍스트 유형 01",
        title: "해파리의 신기한 이야기들",
      },
      titles: [
        {
          title: "말랑해보인다",
          desc: "자주 이야기 하지만, 말랑해보이지 않나요? 돌고래의 놀이감이 되는 이유가 있습니다.",
          class: "t1",
          amore: "더보기",
        },
        {
          title: "보는 것 만으로 즐겁다.",
          desc: "흔들리는 것 만으로도 마치 마리모를 보는 것과 같이 마음의 평화를 얻을 수 있어요.",
          class: "t2",
          amore: "더보기",
        },
        {
          title: "온도에 따라 나타난다.",
          desc: "보통 따뜻할 때에 나타나지만, 깊은 심해속에서도 살 수 있으니 차가운 물에 등장하는 아이도 있답니다.",
          class: "t3",
          amore: "더보기",
        },
        {
          title: "혼자서 증식이 가능하다",
          desc: "놀랍게도 갈라진다면 세포분열을 통해 재생하여 증식해 별개의 해파리가 된답니다. 놀랍지 않나요?",
          class: "t4",
          amore: "더보기",
        },
        {
          title: "영원히 사는 종이 있다.",
          desc: "'작은보호탑 해파리'는 생존에 부적절한 환경이 되면 몸을 뒤집어 세포 분열을 통해 어린 상태로 되돌아간대요",
          class: "t5",
          amore: "더보기",
        },
        {
          title: "스스로 빛을 낼 수 있다.",
          desc: "어두운 심해에서 먹이를 유혹하거나, 천적에게 위협을 가하기 위해 빛을 낼 수 있습니다.",
          class: "t6",
          amore: "더보기",
        },
      ],
    };
  },
}
</script>


<style>
/* 텍스트 유형 */
.text__inner {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
}
.text {
    width: 32%;
    margin-bottom: 2%;
    padding: 20px;
    box-sizing: border-box;
    border-radius: 10px;
    transition: background 0.4s;
}
.text:hover {
    background-color: #f5f5f5;

}
.text__title {
    font-size: 24px;
    line-height: 1;
    margin-bottom: 10px;
    white-space: nowrap;
    text-overflow: ellipsis;
    position: relative;
    padding-top: 75px;
}

.text__title::before {
    content: '';
    position: absolute;
    left: 0;
    top: 0;
    width: 60px;
    height: 60px;
    background: url(../../assets/img/text_type_01_.svg);
    border-radius: 50%;
}
.text.t1 .text__title::before {
    background-position: 0 0;
}
.text.t2 .text__title::before {
    background-position: -100px 0;
}
.text.t3 .text__title::before {
    background-position: -200px 0;
}
.text.t4 .text__title::before {
    background-position: -300px 0;
}
.text.t5 .text__title::before {
    background-position: -400px 0;
}
.text.t6 .text__title::before {
    background-position: -500px 0;
}


.text__desc {
    font-size: 18px;
    font-weight: 300;
    line-height: 1.4;

    overflow: hidden; /* 2줄 이상 효과 */
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 3; 
    -webkit-box-orient: vertical;
    margin-bottom: 20px;

}
.text_btn {
    font-size: 16px;
    line-height: 1;
    text-decoration: underline;
    color: #666;
    text-underline-position: under;
}

@media (max-width: 960px) {
    .text {
        width: 49%;
        background: #f5f5f5;
    }
}
@media (max-width: 600px) {
    .text__title {
        font-size: 18px;
    }
    .text__desc {
        font-size: 16px;
    }
}
@media (max-width: 480px) {
   .text {
        width: 100%;
   }

}
</style>
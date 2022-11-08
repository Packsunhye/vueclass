<template>
    <section id="cardType" class="card_wrap" :class ="attr">
        <h2>{{ top.title }}</h2>
        <p>{{ top.desc }}</p>
        <div class="card_inner" :class ="layout">
            <article class="card" v-for="text in titles" v-bind:key="text.key">
                <figure class="card_header">
                    <img src="../../assets/img/card_bg01.jpg" alt="고양이가 가만히 있을 때" />
                </figure>
                <div class="card_body">
                    <h3 class="tit">{{ text.title }}</h3>
                    <p class="desc">{{ text.desc }}</p>
                    <a href="/" class="btn">
                        {{ text.more }} 
                        <span aria-hidden="true">
                            <svg width="65" height="8" viewBox="0 0 65 8" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M64.3536 4.35355C64.5488 4.15829 64.5488 3.84171 64.3536 3.64645L61.1716 0.464466C60.9763 0.269204 60.6597 0.269204 60.4645 0.464466C60.2692 0.659728 60.2692 0.976311 60.4645 1.17157L63.2929 4L60.4645 6.82843C60.2692 7.02369 60.2692 7.34027 60.4645 7.53553C60.6597 7.7308 60.9763 7.7308 61.1716 7.53553L64.3536 4.35355ZM0 4.5H64V3.5H0V4.5Z" fill="black"/>
                            </svg>
                        </span>
                    </a>
                </div>
            </article>
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
            title: "해파리가 흘러갑니다 - ଳ",
            desc: "흔들흔들 , 사람들이 일상에 치이는 것처럼 해파리도 물살에 치여 움직인답니다.",
          },
          titles: [
            {
              title: "넙적한 해파리",
              desc: "넙적한 상산이 작은 촉수들과 어울려 바다에서 흔들립니다. 파란색 해파리를 멍하게 바라보다 보면 어느샌가 시간이 엄청 지나가있어요, 그렇지만 빠져들게 되지 않나요?",
              more: "더 자세히 보기",
              img: "../../assets/img/card_bg01.jpg",
            },
            {
              title: "조그마한 해파리",
              desc: "바쁜듯 열심히 구완을 흩날리고 있지만 사실은 해파리는 흘러가고 있답니다. 하루에 할일이 지나다니는 것 뿐이라니 부러워요 저도 요 조그마한 해파리 처럼 가만히 즐기고 싶다.",
              more: "더 자세히 보기",
              img: "../../assets/img/card_bg02.jpg",
            },
            {
              title: "풍선같은 해파리",
              desc: "보자마자 풍선같은 생김새에 웃음이 나와요. 후 바람을 부르면 하늘로 올라같 것 같습니다. 사실은 바다가 제 2의 하늘이 아닐까요? 높이 높이 올라가렴 작은 풍선 해파리야",
              more: "더 자세히 보기",
              img: "../../assets/img/card_bg03.jpg",
            },
          ],
        };
    },
}
</script>

<style>
/* cardType */
.card_inner {
    display: flex;
    justify-content: space-between;  /* 가운데 정렬로 맞추기*/
}
.card {
    width: 32%;
    background-color: #f5f5f5;
}
.card_body {
    padding: 24px;
}
.card_body .tit {
    font-size: 24px;
    margin-bottom: 10px;
    overflow: hidden; /* 한줄 효과 */
    white-space: nowrap;
    text-overflow: ellipsis;
    padding-right: 20px;
}
.card_body .desc {
    font-size: 18px;
    line-height: 1.4;
    color: #666;
    margin-bottom: 20px;
    font-weight: 300;
    overflow: hidden; /* 2줄 이상 효과 */
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 4; 
    -webkit-box-orient: vertical;
}

@media(max-width: 960px){
    .card_inner {
        flex-wrap: wrap;
    }
    .card {
        width: 49%;
    }

    .card:last-child {
        display: none;
    }
}
@media(max-width: 600px){
    .card {
        width: 100%;
    }

    .card:first-child {
        margin-bottom: 20px;
    }

    .card_body {
        padding: 20px;
    }

    .card_body .desc {

    }
}

</style>
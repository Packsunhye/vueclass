<template>
     <section id="imgTextType" class="imgText__wrap" :class="attr">
        <h2 class="blind">해파리의 신비한 빛깔</h2>
        <div class="imgText__inner" :class="layout">
            <div class="imgText__txt">
                <span>{{ top.title }}</span>
                <h3>{{ top.desc }}</h3>
                <p>{{ top.msg }}</p>
                <ul>
                    <li><a href="/">{{ top.name1 }}</a></li>
                    <li><a href="/">{{ top.name2 }}</a></li>
                    <li><a href="/">{{ top.name3 }}</a></li>
                    <li><a href="/">{{ top.name4 }}</a></li>
                    <li><a href="/">{{ top.name5 }}</a></li>
                    <li><a href="/">{{ top.name6 }}</a></li>
                </ul>
            </div>
            <div class="imgText__img" 
            :class="text.class"
            v-for="text in titles"
            v-bind:key="text.key">
                <a href="/">{{ text.title }}</a>
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
            title: "jellu fisf color",
            desc: "해파리의 신비한 빛깔",
            msg: "빛에 따라 달라지지만, 어떠한 색깔도 잘 어울리는 모습을 보입니다.",
            name1: "노무라입깃해파리",
            name2: "보름달물해파리",
            name3: "사자갈기해파리",
            name4: "스티기오메두사",
            name5: "숲뿌리해파리",
            name6: "범피",
          },
          titles: [
            {
              title: "대양해파리",
              class : "img1",
            },
            {
              title: "커튼원양해파리",
              class : "img2",
            },
          ],
        };
    },
}
</script>

<style>
/* 이미지 텍스트 유형 */
.imgText__inner {
    display: flex;
    justify-content: space-between;
}

.imgText__inner div {
    width: 32%;
    height: 500px;
}

.imgText__txt span {
    font-size: 16px;
    color: #666;
    text-decoration: underline;
    text-underline-position: under;
    margin-bottom: 20px;
    display: block;
}

.imgText__txt h3 {
    color: #fff;
    font-size: 50px;
    font-weight: 300;
    /* word-break: keep-all;
    line-height: 1.4; */
    margin-bottom: 20px;
}

.imgText__txt p {
    font-size: 18px;
    font-weight: 300;
    line-height: 1.5;
    color: rgb(218, 218, 218);
    margin-bottom: 10px;
}

.imgText__txt ul {
    font-size: 18px;
    font-weight: 300;
    line-height: 1.6;
}

.imgText__txt ul li {
    padding-left: 20px;
    position: relative;
}

.imgText__txt ul li a {
    color: rgb(148, 148, 148);
}

.imgText__txt ul li::before {
    content: '';
    width: 5px;
    height: 5px;
    border-radius: 50%;
    position: absolute;
    left: 5px;
    top: 9px;
    background: rgb(148, 148, 148);
}

.imgText__wold {
    display: contents;
}

.imgText__img {
    border-radius: 10px;
    position: relative;
}

.imgText__img a {
    position: absolute;
    left: 30px;
    bottom: 30px;
    background-color: #66a4ce7a;
    color: #fff;
    font-size: 18px;
    padding: 10px 30px;
    border-radius: 30px;
    display: inline-block;
}

.imgText__img a.blue {
    background-color: rgba(125, 102, 209, 0.527);
}

.imgText__img.img1 {
    background: url(../../assets/img/imgText_01.jpg) no-repeat center / cover;
}

.imgText__img.img2 {
    background: url(../../assets/img/imgText_02.jpg) no-repeat center / cover;
}

@media(max-width: 960px) {
    .imgText__inner {
        flex-wrap: wrap;
    }

    .imgText__txt h3 {
        font-size: 40px;
    }

    .imgText__txt p {
        margin-bottom: 60px;
    }

    .imgText__inner>div.imgText__txt {
        width: 100%;
        height: auto;
        text-align: center;
    }

    .imgText__inner>div.imgText__txt ul {
        display: none;
    }

    .imgText__inner>div.imgText__img {
        width: 49%;
    }

}

@media(max-width: 600px) {
    .imgText__txt span {
        font-size: 14px;
        margin-bottom: 10px;
    }

    .imgText__txt h3 {
        font-size: 30px;
    }

    .imgText__txt p {
        margin-bottom: 50px;
        font-size: 16px;
    }

    .imgText__inner>div.imgText__img {
        width: 100%;
        height: 200px;
    }

    .imgText__inner>div.imgText__img.img1 {
        margin-bottom: 20px;
    }

    .imgText__img a {
        left: 20px;
        bottom: 20px;
    }
}
</style>
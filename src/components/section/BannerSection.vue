<template>
    <section id="bannerType" class="banner__wrap" :class="attr">
        <h2 class="blind">배너 영역</h2>
        <div class="banner__inner">
            <h3 class="title">{{ titles[0].title }}</h3>
            <p class="desc">{{ titles[0].desc }}
                <a href="/" title="해파리 보러가기">{{ titles[0].to }}</a>
            </p>
            <span class="small">{{ titles[0].about }}</span>
        </div>
    </section>    
</template>

<script>
export default {
  props: {
    attr: String,
  },
  data: function () {
    return {
      titles: [
        { title: "해파리 사이트" },
        { desc: "해파리들이 얼마나 아름다운지 알리는 사이트" },
        { link: "/" },
        { to: "어떠신가요?" },
        { about: "배너 유형 01" },
      ],
    };
  },
}
</script>

<style>
.banner__inner {
    background-image: url(../../assets/img/banner_bg01.jpg);
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    text-align: center;
    padding: 120px 0;
    color: #fff;
}

.banner__inner .title {
    font-size: 50px;
    line-height: 1;
    font-weight: 500;
    margin-bottom: 40px;
}

.banner__inner .desc {
    font-size: 24px;
    line-height: 1.5;
    font-weight: 300;
    margin-bottom: 70px;
}

.banner__inner .desc a {
    color: #fff;
    display: block;
}

.banner__inner .desc a:hover {
    text-decoration: underline;
}

.banner__inner .small {
    font-size: 16px;
    text-decoration: underline;
}

@media(max-width: 960px) {
    .banner__inner {
        padding: 100px 0;
    }
}

@media(max-width: 600px) {
    .banner__inner {
        padding: 80px 0;
    }

    .banner__inner .title {
        font-size: 30px;
        margin-bottom: 20px;
    }

    .banner__inner .desc {
        font-size: 16px;
        margin-bottom: 40px;
    }
}
</style>
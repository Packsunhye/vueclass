<template>
    <footer id="footerType" class="footer__wrap nexon section gray scroll">
        <h2 class="blind">푸터 영역</h2>
        <div class="footer__inner container">
            <div class="footer__menu">
                <div>
                    <h3>사이트</h3>
                    <ul>
                        <li><a href="/">웹표준 사이트</a></li>
                        <li><a href="/">반응형 사이트</a></li>
                        <li><a href="/">패럴랙스 사이트</a></li>
                        <li><a href="/">포트폴리오 사이트</a></li>
                    </ul>
                </div>
                <div>
                    <h3>헤더 영역</h3>
                    <ul>
                        <li><a href="/">메뉴 유형01</a></li>
                        <li><a href="/">메뉴 유형02</a></li>
                    </ul>
                </div>
                <div>
                    <h3>슬라이드 영역</h3>
                    <ul>
                        <li><a href="/">슬라이드 유형01</a></li>
                        <li><a href="/">슬라이드 유형02</a></li>
                    </ul>
                </div>
                <div>
                    <h3>이미지 영역</h3>
                    <ul>
                        <li><a href="/">이미지 유형01</a></li>
                        <li><a href="/">이미지 유형02</a></li>
                        <li><a href="/">이미지/텍스트 유형01</a></li>
                        <li><a href="/">이미지/텍스트 유형02</a></li>
                        <li><a href="/">텍스트 유형01</a></li>
                    </ul>
                </div>
                <div>
                    <h3>컨텍츠 영역</h3>
                    <ul>
                        <li><a href="/">카드 유형01</a></li>
                        <li><a href="/">카드 유형02</a></li>
                        <li><a href="/">카드 유형03</a></li>
                    </ul>
                </div>
                <div>
                    <h3>푸터 영역</h3>
                    <ul>
                        <li><a href="/">푸터 메뉴 유형01</a></li>
                        <li><a href="/">푸터 컨택트 유형02</a></li>
                        <li><a href="/">푸터 이메일 유형03</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer__rigth">
                2022 Manyong. Portfolio is Power <br />
                All rights reserved.
            </div>
        </div>
    </footer>
</template>

<style>
.footer__inner {}
.footer__inner .footer__menu {
    display: flex;
    margin-bottom: 70px;
}
.footer__inner .footer__menu > div {
    width: 16%;
}

.footer__inner .footer__menu h3 {
    font-size: 18px;
    margin-bottom: 20px;
}
.footer__inner .footer__menu li a {
    font-size: 14px;
    color: #666;
    margin-bottom: 10px;
    display: block;
}
.footer__inner .footer__rigth {
    border-top: 1px solid #d9d9d9;
    text-align: center;
    padding-top: 40px;
    color: #666;
    line-height: 1.5;
}


@media (max-width: 960px){
    .footer__menu {
        display: none !important;
    }

    .footer__rigth {
        padding-top: 0 !important;
        border-top: 0 !important;
    }

    .footer__wrap {
        padding: 40px 0 !important;
    }
    
}
@media (max-width: 600px){
   
}
@media (max-width: 480px){
   
}
</style>
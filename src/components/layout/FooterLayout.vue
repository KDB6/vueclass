<template>
    <section id="footerType" class="footer__wrap content" :class="attr">
        <h2 class="blind">푸터 영역</h2>
        <div class="footer__inner" :class="layout">
            <div class="footer__menu">
                <div>
                    <h3>POTTERY</h3>
                    <ul>
                        <li><a href="#">웹표준 사이트</a></li>
                        <li><a href="#">반응형 사이트</a></li>
                        <li><a href="#">패럴랙스 사이트</a></li>
                        <li><a href="#">포트폴리오 사이트</a></li>
                    </ul>
                </div>
                <div>
                    <h3>Header</h3>
                    <ul>
                        <li><a href="#">메뉴 유형01</a></li>
                        <li><a href="#">메뉴 유형02</a></li>
                    </ul>
                </div>
                <div>
                    <h3>22AW Lookbook</h3>
                    <ul>
                        <li><a href="#">슬라이드 유형01</a></li>
                        <li><a href="#">슬라이드 유형02</a></li>
                    </ul>
                </div>
                <div>
                    <h3>NEW ARRIVALS</h3>
                    <ul>
                        <li><a href="#">이미지 유형01</a></li>
                        <li><a href="#">이미지 유형02</a></li>
                        <li><a href="#">이미지/텍스트 유형01</a></li>
                        <li><a href="#">이미지/텍스트 유형02</a></li>
                        <li><a href="#">텍스트 유형01</a></li>
                    </ul>
                </div>
                <div>
                    <h3>HQ Service</h3>
                    <ul>
                        <li><a href="#">카드 유형01</a></li>
                        <li><a href="#">카드 유형02</a></li>
                        <li><a href="#">카드 유형03</a></li>
                    </ul>
                </div>
                <div>
                    <h3>Pottery</h3>
                    <ul>
                        <li><a href="#">푸터 메뉴 유형01</a></li>
                        <li><a href="#">푸터 컨택트 유형02</a></li>
                        <li><a href="#">푸터 이메일 유형03</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer__right">
                2022 Pottery.<br>
                All rights reserved.
            </div>
        </div>
    </section>
</template>

<script>
export default {
  props: {
    attr: String,
    layout: String
  }
}
</script>

<style>
.footer__menu {
    display: flex;
    margin-bottom: 70px;
    text-align: center;
}
.footer__menu > div {
    width: 16%;
}
.footer__menu > div h3 {
    font-size: 18px;
    margin-bottom: 20px;
}
.footer__menu li {
    font-size: 14px;
    color: #666;
    margin-bottom: 10px;
    display: block;
}
.footer__right {
    border-top: 1px solid #d9d9d9;
    text-align: center;
    padding-top: 40px;
    color: #666;
    line-height: 1.5;
}

@media (max-width: 960px ) {
    .footer__menu {
        display: none;
    }
    .footer__right {
        padding-top: 0;
        border-top: 0;
    }
    .footer__wrap {
        padding: 40px 0;
    }
}

/* @media (max-width: 768px) {
    .footer__inner {
        margin-left: 25px;
    }
    .footer__menu {
        width: 768px;
        display: flex;
        margin-bottom: 20px;
    }
    .footer__right {
        width: 720px;
    }
} */
</style>
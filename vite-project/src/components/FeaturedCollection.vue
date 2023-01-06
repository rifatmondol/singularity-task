<template>
    <div id="featured-collection-main">
        <div class="container">
            <h4>Collection Featured NFTs</h4>
            <div class="row">
                <div
                    class="col-md-4"
                    v-for="item in collectionSection"
                    :key="item.id"
                >
                    <div class="featured-collection-item">
                        <div class="row">
                            <div class="col-md-8">
                                <div class="img-left">
                                    <img
                                        :src="item.bigImage"
                                        alt="main image"
                                        class="main-img"
                                    />
                                    <h5>{{ item.title }}</h5>
                                    <img
                                        :src="item.avatarImage"
                                        alt="avatar"
                                        class="avatar-2"
                                    />
                                    <span>{{ item.linkText }}</span>
                                </div>
                            </div>
                            <div class="col-md-4">
                                <div class="img-right">
                                    <div
                                        v-for="image in item.rightImage"
                                        :key="image.id"
                                    >
                                        <img
                                            :src="image.img"
                                            alt="secondary image"
                                        />
                                    </div>
                                    <a href="#">{{ item.btnText }}</a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            collectionSection: [
                {
                    id: 0,
                    bigImage:
                        "/src/assets/img/feature/unsplash_F56Y7dgrAkc.png",
                    title: "Amazing Collection",
                    avatarImage: "/src/assets/img/banner/Ellipse 95.png",
                    linkText: "by Arkhan",
                    btnText: "Total 54 items",
                    rightImage: [
                        {
                            id: 0,
                            img: "/src/assets/img/feature/unsplash_pVoEPpLw818.png",
                        },
                        {
                            id: 1,
                            img: "/src/assets/img/feature/unsplash_LpbyDENbQQg.png",
                        },
                        {
                            id: 2,
                            img: "/src/assets/img/feature/unsplash_9anj7QWy-2g.png",
                        },
                    ],
                },
                {
                    id: 1,
                    bigImage:
                        "/src/assets/img/feature/unsplash_F56Y7dgrAkc (1).png",
                    title: "Amazing Collection",
                    avatarImage: "/src/assets/img/banner/Ellipse 95.png",
                    linkText: "by Arkhan",
                    btnText: "Total 54 items",
                    rightImage: [
                        {
                            id: 0,
                            img: "/src/assets/img/feature/unsplash_LpbyDENbQQg.png",
                        },
                        {
                            id: 1,
                            img: "/src/assets/img/feature/unsplash_pVoEPpLw818.png",
                        },
                        {
                            id: 2,
                            img: "/src/assets/img/feature/unsplash_9anj7QWy-2g (1).png",
                        },
                    ],
                },
                {
                    id: 2,
                    bigImage:
                        "/src/assets/img/feature/unsplash_F56Y7dgrAkc (2).png",
                    title: "Amazing Collection",
                    avatarImage: "/src/assets/img/banner/Ellipse 95.png",
                    linkText: "by Arkhan",
                    btnText: "Total 54 items",
                    rightImage: [
                        {
                            id: 0,
                            img: "/src/assets/img/feature/unsplash_pVoEPpLw818 (1).png",
                        },
                        {
                            id: 1,
                            img: "/src/assets/img/feature/unsplash_LpbyDENbQQg (1).png",
                        },
                        {
                            id: 2,
                            img: "/src/assets/img/feature/unsplash_pVoEPpLw818.png",
                        },
                    ],
                },
            ],
        };
    },
};
</script>

<style lang="scss">
@import "../style.scss";
div#featured-collection-main {
    padding: 70px 0px;
    background: rgba(217, 224, 236, 0.3);
    h4 {
        font-family: $fontFamily;
        margin-bottom: 40px;
        font-weight: $fontBold;
    }
    .featured-collection-item {
        .col-md-4 {
            padding-left: 0;
        }
        .img-left {
            img.main-img {
                width: 100%;
            }
            h5 {
                margin-top: 15px;
                font-weight: $fontBold;
            }
            span {
                margin-left: 10px;
                font-weight: 500;
            }
        }
        .img-right {
            position: relative;
            height: 100%;
            img {
                width: 100%;
                margin-bottom: 10px;
                height: 76px;
                object-fit: cover;
                border-radius: 10px;
            }
            a {
                color: $textBlue;
                border: 1px solid $textBlue;
                padding: 7px 0px;
                border-radius: 30px;
                font-weight: $fontBold;
                font-size: 11px;
                width: 100%;
                display: block;
                text-align: center;
                position: absolute;
                bottom: 0;
                right: 0;
                transition: background 0.3s linear;

                &:hover {
                    background: $textBlue;
                    color: $textWhite;
                }
            }
        }
    }
}
</style>
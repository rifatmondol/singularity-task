<template>
    <div id="collection-main">
        <div class="container">
            <div class="row">
                <div class="col-md-4">
                    <div class="collection-left">
                        <div class="collection-left-top">
                            <img
                                src="../assets/img/collection/unsplash_F56Y7dgrAkc.png"
                                alt="image"
                            />
                        </div>

                        <div class="collection-left-bottom">
                            <div class="row">
                                <div class="col-md-9">
                                    <img
                                        src="../assets/img/banner/Ellipse 95.png"
                                        alt=""
                                        class="avatar"
                                    />
                                    <span
                                        >The Futr Abstr <br />
                                        <span>10 in the stock</span></span
                                    >
                                </div>
                                <div class="col-md-3">
                                    <p>Highest Bid</p>
                                    <font-awesome-icon
                                        icon="fa-brands fa-ethereum"
                                    />
                                    <p>0.25 ETH</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-8">
                    <div class="collection-right">
                        <div class="row">
                            <div class="col-md-6">
                                <div class="collection-right-first">
                                    <div class="row">
                                        <div
                                            class="col-md-12 mb-4"
                                            v-for="items in sections"
                                            :key="items.id"
                                        >
                                            <div class="row">
                                                <div class="col-md-5">
                                                    <img
                                                        :src="items.mainImage"
                                                        alt="image"
                                                        class="abstract-img"
                                                    />
                                                </div>
                                                <div class="col-md-7">
                                                    <h5>{{ items.title }}</h5>
                                                    <img
                                                        :src="items.avatarImage"
                                                        alt="avatar"
                                                        class="avatar-2"
                                                    />
                                                    <a href="#">
                                                        <font-awesome-icon
                                                            icon="fa-brands fa-ethereum"
                                                        />
                                                        <span>{{
                                                            items.linkText
                                                        }}</span>
                                                    </a>
                                                    <span>{{
                                                        items.subTitle
                                                    }}</span>
                                                    <input
                                                        type="submit"
                                                        :value="
                                                            items.buttonText
                                                        "
                                                    />
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="col-md-6">
                                <div class="collection-right-second">
                                    <h5>Top Collections over</h5>
                                    <p>Last 7 days</p>
                                    <div class="row">
                                        <div
                                            class="col-md-12"
                                            v-for="items in collectionList"
                                            :key="items.id"
                                        >
                                            <div
                                                class="right-second-inner-main"
                                            >
                                                <div class="row">
                                                    <div class="col-md-4">
                                                        <div
                                                            class="
                                                                second-inner-left
                                                            "
                                                        >
                                                            <span class="id">{{
                                                                items.id + 1
                                                            }}</span>
                                                            <img
                                                                :src="
                                                                    items.image
                                                                "
                                                                alt="abstract image"
                                                            />
                                                            <img
                                                                :src="
                                                                    items.tickImage
                                                                "
                                                                alt="tick image"
                                                                class="tick-img"
                                                                v-if="
                                                                    items.tick ===
                                                                    true
                                                                "
                                                            />
                                                        </div>
                                                    </div>
                                                    <div class="col-md-8">
                                                        <div
                                                            class="
                                                                avatar-details
                                                            "
                                                        >
                                                            <h6>
                                                                {{
                                                                    items.header
                                                                }}
                                                            </h6>
                                                            <p>
                                                                <font-awesome-icon
                                                                    icon="fa-brands fa-ethereum"
                                                                />
                                                                <span>{{
                                                                    items.description
                                                                }}</span>
                                                            </p>
                                                        </div>
                                                        <h5
                                                            :class="
                                                                items.colorRed ==
                                                                true
                                                                    ? 'red'
                                                                    : 'cyan'
                                                            "
                                                        >
                                                            {{ items.rating }}
                                                        </h5>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
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
            sections: [
                {
                    id: 0,
                    mainImage: "/src/assets/img/collection/Group 88.png",
                    title: "The Futr Abstr",
                    avatarImage: "/src/assets/img/banner/Ellipse 95.png",
                    linkText: "0.25 ETH",
                    subTitle: "1 of 8",
                    buttonText: "Place a bid",
                },
                {
                    id: 1,
                    mainImage: "/src/assets/img/collection/Group 89.png",
                    title: "The Futr Abstr",
                    avatarImage: "/src/assets/img/banner/Ellipse 95.png",
                    linkText: "0.25 ETH",
                    subTitle: "1 of 8",
                    buttonText: "Place a bid",
                },
                {
                    id: 2,
                    mainImage: "/src/assets/img/collection/Group 90.png",
                    title: "The Futr Abstr",
                    avatarImage: "/src/assets/img/banner/Ellipse 95.png",
                    linkText: "0.25 ETH",
                    subTitle: "1 of 8",
                    buttonText: "Place a bid",
                },
            ],
            collectionList: [
                {
                    id: 0,
                    image: "/src/assets/img/collection/unsplash_k0rVudBoB4c.png",
                    tickImage: "/src/assets/img/collection/Vector.png",
                    header: "CryptoFunks",
                    description: "19,769.39",
                    rating: "+26.52%",
                    tick: true,
                    colorRed: false,
                },
                {
                    id: 1,
                    image: "/src/assets/img/collection/unsplash_fT49QnFucQ8.png",
                    tickImage: "/src/assets/img/collection/Vector.png",
                    header: "Cryptix",
                    description: "2,769.39",
                    rating: "+10.52%",
                    tick: false,
                    colorRed: true,
                },
                {
                    id: 2,
                    image: "/src/assets/img/collection/unsplash_5MTf9XyVVgM.png",
                    tickImage: "/src/assets/img/collection/Vector.png",
                    header: "Frensware",
                    description: "9,232.39",
                    rating: "+2.52%",
                    tick: false,
                    colorRed: false,
                },
                {
                    id: 3,
                    image: "/src/assets/img/collection/unsplash_zkNT5mikUuo.png",
                    tickImage: "/src/assets/img/collection/Vector.png",
                    header: "PunkArt",
                    description: "3,769.39",
                    rating: "+1.52%",
                    tick: true,
                    colorRed: false,
                },
                {
                    id: 4,
                    image: "/src/assets/img/collection/unsplash_WjIB-6UxA5Q.png",
                    tickImage: "/src/assets/img/collection/Vector.png",
                    header: "Art Crypto",
                    description: "10,769.39",
                    rating: "+2.52%",
                    tick: false,
                    colorRed: true,
                },
            ],
        };
    },
};
</script>

<style lang="scss">
@import "../style.scss";

div#collection-main {
    padding: 70px 0px;
    margin-bottom: 50px;
    .collection-left {
        .collection-left-top img {
            width: 100%;
        }
        .collection-left-bottom {
            margin-top: 30px;
            img.avatar {
                float: left;
                margin-right: 10px;
            }
            span {
                font-weight: $fontBold;
                font-size: 20px;
                line-height: 1px;
                span {
                    font-weight: 400;
                    color: #363639;
                    font-size: 14px;
                }
            }
            p {
                color: #3a3a3a;
                font-size: 12px;
                font-weight: 500;
                margin-bottom: 5px;
            }

            svg + p {
                color: #3a3a3a;
                font-size: 16px;
                float: right;
            }
        }
    }
    .collection-right {
        .collection-right-first {
            img.abstract-img {
                width: 100%;
            }
            img.avatar-2 {
                vertical-align: bottom;
            }
            h5 {
                font-weight: $fontBold;
                margin-top: 5px;
            }
            a {
                border: 1px solid $textGreen;
                color: $textGreen;
                font-weight: $fontBold;
                padding: 6px 10px;
                font-size: 12px;
                border-radius: 7px;
                display: inline-block;
                margin-left: 10px;
                svg {
                    font-size: 14px;
                }
                span {
                    margin-left: 5px;
                }
            }
            a + span {
                margin-left: 10px;
                color: #757575;
                font-size: 14px;
            }
            input {
                background: $textWhite;
                color: $textMagenta;
                border: 2px solid $textMagenta;
                font-weight: $fontBold;
                padding: 10px 20px;
                margin-top: 17px;
                border-radius: 30px;
                font-size: 14px;
                transition: background 0.4s linear;
                display: block;
                &:hover {
                    background: $textMagenta;
                    color: $textWhite;
                }
            }
        }
        .collection-right-second {
            border-left: 1px solid #f0f0f0;
            padding-left: 35px;
            h5 {
                font-weight: $fontBold;
                font-family: $fontFamily;
            }
            p {
                color: $textMagenta;
                font-weight: 500;
                font-size: 18px;
            }
            .right-second-inner-main {
                padding: 15px 0px;
                border-bottom: 1px solid #f0f0f0;
                span.id {
                    font-weight: 500;
                    font-size: 24px;
                    margin-right: 20px;
                    display: inline-block;
                    color: $textBlack;
                }
                .second-inner-left {
                    position: relative;
                    img.tick-img {
                        position: absolute;
                        right: 0px;
                        top: -5px;
                    }
                }
                .avatar-details {
                    float: left;
                    p {
                        color: $textBlack;
                        margin: 0;
                        svg {
                            margin-right: 8px;
                        }
                        span {
                            color: #636363;
                            font-size: 14px;
                        }
                    }
                }
                .avatar-details + h5 {
                    font-weight: $fontBold;
                    font-family: "sans-serif";
                    float: right;
                    margin: 0;
                    margin-top: 15px;
                }
                h5.cyan {
                    color: #14c8b0;
                }
                h5.red {
                    color: #ff002e;
                }
            }
            .col-md-12:last-child .right-second-inner-main {
                border-bottom: inherit;
            }
        }
    }
}
</style>
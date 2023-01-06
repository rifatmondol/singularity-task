<template>
    <div id="banner-main">
        <div class="container">
            <div class="row banner">
                <div class="col-md-6 banner-left">
                    <h2>Discover, and collect Digital Art NFTs</h2>
                    <p>
                        Digital marketplace for crypto collectibles and <br />
                        non-fungible tokens (NFTs). Buy, Sell, and discover
                        <br />
                        exclusive digital assets.
                    </p>
                    <input type="submit" class="explore" value="Explore Now" />
                    <div class="row art-auction-artist">
                        <div
                            class="col-3 inner-item"
                            v-for="items in threeList"
                            :key="items.id"
                        >
                            <h4>{{ items.header }}<span>K+</span></h4>
                            <p>{{ items.description }}</p>
                        </div>
                    </div>
                </div>
                <div class="col-md-6 banner-right">
                    <div class="image-box one">
                        <img
                            src="../assets/img/banner/unsplash_tZCrFpSNiIQ.png"
                            alt="vector"
                        />
                    </div>
                    <div class="image-box two">
                        <img
                            src="../assets/img/banner/unsplash_pVoEPpLw818.png"
                            alt="vector"
                        />
                    </div>
                    <div class="image-box three">
                        <img
                            src="../assets/img/banner/unsplash_E8Ufcyxz514.png"
                            alt="vector"
                        />
                        <div class="text-box">
                            <div class="text-header">
                                <h4>Abstr Gradient NFT</h4>
                                <img
                                    src="../assets/img/banner/Ellipse 95.png"
                                    alt="avatar"
                                />
                                <span>Arkhan17</span>
                            </div>
                            <div class="text-bottom">
                                <div class="row">
                                    <div class="col-md-6">
                                        <div class="inner-text">
                                            <h5>Current Bid</h5>
                                            <font-awesome-icon
                                                icon="fa-brands fa-ethereum"
                                            />
                                            <span>0.25 ETH</span>
                                        </div>
                                    </div>
                                    <div class="col-md-6">
                                        <div class="inner-text">
                                            <h5>Ends in</h5>
                                            <p>
                                                <span>12h</span><span>43m</span
                                                ><span>42s</span>
                                            </p>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <img
                            src="../assets/img/banner/Group-83.png"
                            alt="img"
                            class="diamond-big"
                        />
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
            threeList: [
                {
                    id: 0,
                    header: "98",
                    description: "Artwork",
                },
                {
                    id: 0,
                    header: "12",
                    description: "Auction",
                },
                {
                    id: 0,
                    header: "15",
                    description: "Artist",
                },
            ],
        };
    },
};
</script>



<style lang="scss" scoped>
@import "../style.scss";

div#banner-main {
    padding: 50px 0px;
    margin-bottom: 50px;
    .banner-left {
        h2 {
            margin: 0;
            margin-top: 15px;
            margin-bottom: 25px;
            font-family: $fontFamily;
            font-size: 40px;
            font-weight: $fontBold;
        }
        > p {
            color: $textGray;
            font-size: 20px;
            margin: 0;
        }
        .explore {
            background: $textMagenta;
            border-radius: 30px;
            font-weight: $fontBold;
            padding: 10px 30px;
            color: $textWhite;
            border: none;
            margin: 35px 0px;
        }
        .art-auction-artist {
            .inner-item {
                h4 {
                    font-family: $fontFamily;
                    font-weight: $fontBold;
                    font-size: 40px;
                    margin: 0;
                    span {
                        font-family: "sans-serif";
                    }
                }
                p {
                    font-size: 20px;
                    color: $textGray;
                }
            }
        }
    }
    .banner-right {
        position: relative;
        .image-box {
            position: absolute;
            top: 0;
        }
        .one {
            right: 40px;
            top: 60px;
        }
        .two {
            right: 70px;
            top: 30px;
        }
        .three {
            right: 100px;
            top: 0;
            .text-box {
                .text-header {
                    position: absolute;
                    top: 40px;
                    left: 30px;
                    h4 {
                        color: $textWhite;
                        font-size: 28px;
                        word-spacing: -2px;
                        font-weight: $fontBold;
                    }
                    img {
                        margin-right: 15px;
                    }
                    span {
                        display: inline-block;
                        color: $textWhite;
                        font-weight: $fontBold;
                        font-size: 20px;
                    }
                }
                .text-bottom {
                    margin: 0px 30px;
                    padding: 20px 0px;
                    padding-left: 30px;
                    position: relative;
                    margin-top: -120px;
                    border-radius: 15px;
                    .inner-text {
                        position: relative;
                        z-index: 1;
                        h5 {
                            font-size: 12px;
                            color: $textWhite;
                        }
                        svg {
                            margin-right: 10px;
                            color: $textWhite;
                        }
                        span {
                            font-size: 16px;
                            display: inline-block;
                            color: $textWhite;
                            font-weight: $fontBold;
                        }
                        p {
                            margin: 0;
                            color: $textWhite;
                            span {
                                margin-right: 10px;
                                font-weight: $fontBold;
                            }
                        }
                    }
                    &:after {
                        content: "";
                        background-image: url("../assets/img/banner/Rectangle\ 183.png");
                        background-position: center;
                        background-size: cover;
                        background-repeat: no-repeat;
                        position: absolute;
                        top: 0;
                        left: 0;
                        width: 100%;
                        height: 100%;
                        border-radius: 15px;
                    }
                }
            }
            .diamond-big {
                position: absolute;
                bottom: 22%;
                left: -50px;
            }
        }
    }
}
</style>

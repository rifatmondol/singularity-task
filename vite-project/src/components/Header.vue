<script>
import { ref } from "vue";
export default {
  data() {
    return {
      menuList: [
        {
          id: 0,
          name: "Marketplace",
          link: "https://www.google.com",
        },
        {
          id: 1,
          name: "Resource",
          link: "https://www.facebook.com",
        },
        {
          id: 2,
          name: "About",
          link: "https://www.twitter.com",
        },
      ],
    };
  },
};
</script>

<template>
  <div id="header-main">
    <div class="container">
      <div class="row header">
        <div class="col-md-6">
          <div class="row header-left">
            <div class="col-md-3 logo">
              <a href="#">NFTERS</a>
            </div>
            <div class="col-md-9 manu-item">
              <ul>
                <li v-for="list in menuList" :key="list.id">
                  <a :href="list.link">{{ list.name }}</a>
                </li>
              </ul>
            </div>
          </div>
        </div>
        <div class="col-md-6">
          <div class="row header-right">
            <div class="col-md-5 search">
              <input type="text" placeholder="Search" />
              <font-awesome-icon icon="fa-solid fa-magnifying-glass" />
            </div>
            <div class="col-md-7 input-box">
              <input type="submit" class="upload" value="Upload" />
              <input type="submit" class="wallet" value="Connect Wallet" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import "../style.scss";

#header-main {
  border-bottom: 1px solid #f4f4f4;
}
.header {
  padding: 30px 0px 30px 0px;
  align-items: center;
  .header-left {
    align-items: center;
    .logo {
      border-right: 1px solid #f4f4f4;
      a {
        color: $textMagenta;
        font-family: $fontFamily;
        font-weight: $fontBold;
        text-decoration: $none;
        font-size: 24px;
      }
    }
    .manu-item ul {
      display: flex;
      margin: 0;
      padding-left: 20px;
      li {
        list-style: $none;
        a {
          text-decoration: $none;
          color: $textBlack;
          padding-right: 40px;
          display: inline-block;
          font-weight: $fontBold;
        }
      }
    }
  }
}

.header-right {
  .search {
    position: relative;
    input {
      box-sizing: border-box;
      padding: 10px 20px;
      border-radius: 30px;
      border: 1px solid $textLightGray;
      outline: none;
      width: 100%;
    }
    svg {
      position: absolute;
      right: 25px;
      top: 50%;
      transform: translateY(-50%);
      color: $textLightGray;
      cursor: pointer;
    }
  }
  .input-box {
    display: flex;
    justify-content: end;
    position: relative;
    input[type="submit"] {
      cursor: pointer;
    }
    .upload,
    .wallet {
      border-radius: 30px;
      font-weight: $fontBold;
    }
    .upload {
      background: $textMagenta;
      padding: 10px 25px;
      color: $textWhite;
      border: none;
      margin-right: 30px;
      width: 110px;
    }

    .wallet {
      background: $textWhite;
      padding: 10px 20px;
      color: $textMagenta;
      border: 1px solid $textMagenta;
      width: 150px;
    }
  }
}
</style>

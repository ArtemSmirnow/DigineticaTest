<template>
  <div class="products">
    <div class="productCard" v-for="card in cards">
      <div class="sectionLogo">
        <div class="productLogo">
          <img src="../../../images/productLogo.png" alt="Logo of Product" class="logo">
        </div>
        <p v-if="card.hitOfSales" class="salesHit">Хит продаж</p>
        <p v-if="card.discount" class="discount">{{ card.discount }}</p>
      </div>
      <div class="productDescription">
        <p class="brand">Бренд</p>
        <p class="title">{{ card.title }}</p>
      </div>
      <div class="productPrice">
        <span class="price" v-if="card.warehouse == 'inStock'">{{ card.price }}&#x20bd;</span>
        <span class="beforePrice" v-if="card.discount">{{ card.priceBeforeDiscount }}&#x20bd;</span>
      </div>
      <div class="buyBtn">
        <button class="activeBtn" v-if="card.warehouse == 'inStock'">Купить</button>
        <button class="disabledBtn" v-if="card.warehouse !== 'inStock'">Сообщить о поступлении</button>
      </div>
    </div>
  </div>
</template>
<script>
import { cards } from '../../../data/productsCards.js';
export default {
  data() {
    return {
      cards
    }
  }
}
</script>
<style scoped>
.products {
  width: 100%;
  height: 1132px;
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
}

.productCard {
  width: 24%;
  height: 356px;
  position: relative;

  .sectionLogo {
    width: 100%;
    height: 200px;
    background-color: #F8F8FA;
    position: relative;

    .productLogo {
      width: 100%;
      height: 200px;
      background-color: #F8F8FA;
      display: flex;
      align-items: center;
      justify-content: center;

      .logo {
        width: 60px;
        height: 60px;
        transition: 0.5s;
      }
    }

    .salesHit {
      width: 112px;
      height: 32px;
      background-color: white;
      display: flex;
      align-items: center;
      justify-content: flex-start;
      padding-left: 6px;
      font-size: 14px;
      font-weight: 400;
      position: absolute;
      top: 6%;
      left: 6%;
      background-image: url("../../../images/sale.png");
      background-repeat: no-repeat;
      background-position: 98%;
      border: 1px solid#F2F2F2;
      border-radius: 4px;
    }

    .discount {
      width: 48px;
      height: 26px;
      background-color: #7397F5;
      font-size: 14px;
      font-weight: 700;
      color: white;
      position: absolute;
      bottom: 6%;
      left: 6%;
      display: flex;
      align-items: center;
      justify-content: center;
      border: 1px solid #7397F5 transparent;
      border-radius: 4px;
    }
  }

  .productDescription {
    font-size: 14px;
    font-weight: 400;
    margin-top: 16px;
    width: 100%;
    height: 56px;

    .brand {
      color: #AAAAAA;
    }

    .title {
      margin-top: 8px;
      color: #333333;
      overflow: hidden;
      text-overflow: ellipsis;
      display: -webkit-box;
      -webkit-line-clamp: 2;
      -webkit-box-orient: vertical;
    }
  }

  .productPrice {
    margin-top: 16px;
    display: flex;
    gap: 8px;
    align-items: center;

    .price {
      font-size: 16px;
      font-weight: 700;
    }

    .beforePrice {
      font-size: 12px;
      font-weight: 400;
      color: #AAAAAA;
      text-decoration: line-through;
    }
  }

  .buyBtn {
    margin-top: 8px;

    .activeBtn {
      width: 75px;
      height: 38px;
      background: none;
      outline: none;
      font-size: 14px;
      font-weight: 700;
      color: #7397F5;
      border: 1px solid #7397F5;
      border-radius: 4px;
    }

    .activeBtn:hover {
      background-color: #7397F5;
      color: white;
    }

    .disabledBtn {
      position: absolute;
      bottom: 0;
      width: 100%;
      height: 38px;
      background: none;
      outline: none;
      color: #AAAAAA;
      font-size: 14px;
      font-weight: 700;
      border: 1px solid #AAAAAA;
      border-radius: 4px;
    }
  }
}

.productCard:hover .logo {
  scale: 1.37;
}

.productCard:hover .title {
  color: #125BAE
}
</style>

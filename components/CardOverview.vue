<template>
  <div class="card">
    <div class="headerCard">
      <div class="containerImg">
        <!-- <img v-if="type == 'income'" src="../assets/images/income.png" />
            <img v-else src="../assets/images/spending.png" /> -->
        <!-- INCOME -->

        <!-- INCOME -->
        <svg
          v-if="type == 'income'"
          version="1.0"
          xmlns="http://www.w3.org/2000/svg"
          width="500.000000pt"
          height="500.000000pt"
          viewBox="0 0 500.000000 500.000000"
          preserveAspectRatio="xMidYMid meet"
        >
          <g
            transform="translate(0.000000,500.000000) scale(0.100000,-0.100000)"
            fill="#FFF"
            stroke="none"
          >
            <path
              d="M2418 4800 c-41 -12 -86 -48 -106 -83 -16 -30 -17 -115 -22 -1184
          l-5 -1152 -220 204 c-121 113 -234 211 -252 220 -17 8 -56 15 -87 15 -111 0
          -183 -66 -193 -178 -8 -82 17 -132 103 -214 280 -266 734 -680 760 -693 50
          -23 152 -20 202 7 47 26 676 716 730 801 27 43 32 61 32 111 0 125 -79 206
          -200 206 -73 0 -127 -43 -296 -233 l-159 -178 -5 1113 c-5 1217 -1 1139 -62
          1195 -50 47 -145 66 -220 43z"
            />
            <path
              d="M236 2904 c-34 -11 -64 -31 -101 -67 -73 -73 -85 -115 -85 -292 0
          -567 228 -1172 612 -1620 321 -375 752 -647 1211 -764 231 -60 288 -66 597
          -66 318 0 399 10 651 79 709 195 1308 711 1611 1391 141 314 218 662 218 978
          0 131 -2 146 -26 197 -32 69 -75 115 -139 147 -141 72 -326 -8 -383 -165 -8
          -20 -18 -108 -23 -194 -14 -251 -53 -440 -136 -648 -212 -538 -643 -950 -1179
          -1129 -814 -273 -1652 26 -2127 759 -108 168 -201 379 -252 576 -37 143 -55
          267 -65 446 -7 135 -12 165 -33 211 -65 141 -205 206 -351 161z"
            />
          </g>
        </svg>
        <!-- SPENDING -->
        <svg
          v-else
          version="1.0"
          xmlns="http://www.w3.org/2000/svg"
          width="500.000000pt"
          height="500.000000pt"
          viewBox="0 0 500.000000 500.000000"
          preserveAspectRatio="xMidYMid meet"
        >
          <g
            transform="translate(0.000000,500.000000) scale(0.100000,-0.100000)"
            fill="#FFF"
            stroke="none"
          >
            <path
              d="M2404 4894 c-25 -12 -490 -436 -758 -692 -86 -82 -111 -132 -103
          -214 10 -112 82 -178 193 -178 31 0 70 7 87 15 18 9 131 107 252 220 l220 204
          5 -1152 c5 -1080 6 -1154 23 -1185 54 -98 225 -123 318 -45 69 58 63 -31 69
          1201 l5 1113 159 -178 c169 -190 223 -233 296 -233 121 0 200 81 200 206 0 50
          -5 68 -32 111 -54 85 -683 775 -730 801 -50 27 -155 30 -204 6z"
            />
            <path
              d="M236 2904 c-34 -11 -64 -31 -101 -67 -73 -73 -85 -115 -85 -292 0
          -567 228 -1172 612 -1620 321 -375 752 -647 1211 -764 231 -60 288 -66 597
          -66 318 0 399 10 651 79 709 195 1308 711 1611 1391 141 314 218 662 218 978
          0 131 -2 146 -26 197 -32 69 -75 115 -139 147 -141 72 -326 -8 -383 -165 -8
          -20 -18 -108 -23 -194 -14 -251 -53 -440 -136 -648 -212 -538 -643 -950 -1179
          -1129 -814 -273 -1652 26 -2127 759 -108 168 -201 379 -252 576 -37 143 -55
          267 -65 446 -7 135 -12 165 -33 211 -65 141 -205 206 -351 161z"
            />
          </g>
        </svg>
      </div>
      <div>
        <!-- Mudar para variavel futuramente -->
        <span
          v-if="type == 'income'"
          style="color: var(--income); font-weight: 600"
          >+2,63%</span
        >
        <span v-else style="color: var(--spending); font-weight: 600"
          >-1,89%</span
        >
      </div>
    </div>
    <div class="footerCard">
      <div class="containerPrice">
        <span
          v-if="type == 'income'"
          style="color: var(--arrow); font-weight: 600"
          >Incomes</span
        >
        <span v-else style="color: var(--arrow); font-weight: 600"
          >Spending</span
        >
        <span class="price">$ 3.000,00</span>
      </div>
      <div class="containerIcon"></div>
    </div>
  </div>
</template>
<script>
export default {
  name: "CardOverview",
  props: { type: String },
}
</script>
<style scoped>
.card {
  margin-top: 10px;
  width: 60%;
  background-color: #fff;
  height: 13vh;
  border-radius: 15px;
  padding: 5px 10px;
}

.containerImg {
  background-color: #000;
  border-radius: 50%;
  width: 35px;
  text-align: center;
}

.headerCard {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}
.footerCard {
  margin-top: 18%;
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
}
.containerPrice {
  display: flex;
  flex-direction: column;
}
.price {
  font-weight: 700;
  font-size: 1.1rem;
}
.containerIcon {
  width: 30px;
  height: 30px;
  border-radius: 50%;
  border: 1px solid black;
}

svg {
  width: 25px !important;
  color: #fff;
}
</style>

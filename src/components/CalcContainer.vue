<template >
  <div class="calcContainer">
    <div class="monitor"></div>
    <div class="keys">
      <div class="thirdRow">
        <div class="num" @click="hello">9</div>
        <div class="num">8</div>
        <div class="num">7</div>
        <div class="num oprations divide"><svg xmlns="http://www.w3.org/2000/svg" height=".7em"
            viewBox="0 0 576 512">
            <path
            fill="white"  d="M576 128c0-35.3-28.7-64-64-64H205.3c-17 0-33.3 6.7-45.3 18.7L9.4 233.4c-6 6-9.4 14.1-9.4 22.6s3.4 16.6 9.4 22.6L160 429.3c12 12 28.3 18.7 45.3 18.7H512c35.3 0 64-28.7 64-64V128zM271 175c9.4-9.4 24.6-9.4 33.9 0l47 47 47-47c9.4-9.4 24.6-9.4 33.9 0s9.4 24.6 0 33.9l-47 47 47 47c9.4 9.4 9.4 24.6 0 33.9s-24.6 9.4-33.9 0l-47-47-47 47c-9.4 9.4-24.6 9.4-33.9 0s-9.4-24.6 0-33.9l47-47-47-47c-9.4-9.4-9.4-24.6 0-33.9z" />
          </svg></div>
      </div>
      <div class="secondRow">
        <div class="num">6</div>
        <div class="num">5</div>
        <div class="num">4</div>
        <div class="num oprations multiple">*</div>

      </div>
      <div class="firstRow">
        <div class="num">3</div>
        <div class="num">2</div>
        <div class="num">1</div>
        <div class="num oprations">+</div>
        
      </div>
      <div class="baseRow">
        <div class="zero">0</div>
        <div class="num oprations">-</div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  methods: {
    hello(){
      console.log('salam')
    }  
  },
}
</script>
<style lang="scss" scoped>
.calcContainer {
  width: 447px;
  height: 570px;
  background-color: var(--dark-gray);
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  justify-content: start;
  padding: 15px 15px;

  .monitor {
    border-radius: 20px;
    width: 100%;
    height: 17%;
    background-color: var(--light-gray);
    align-self: center;
    margin-bottom: 20px;
  }

  .keys {

    .thirdRow,.secondRow, .firstRow,.baseRow {
      display: flex;
      justify-content: space-around;
    }
    .thirdRow{
      margin-top: 10px;
    }
    .secondRow,.firstRow {
      margin-top: 30px;
    }
    .baseRow{
      width: 97%;
      height: 80px;
      margin-top: 20px;
      display: flex;
      justify-content: space-between;
      border-radius: 25px;
      
      .zero{
        background-color: var(--light-gray);
        width: 72%;
        border-radius: 25px;
        color: aliceblue;
        font-size: 46px;
        font-weight: 400;
        display: flex;
        justify-content: center;
        align-items: center;
        margin-left: 10px;
        cursor: pointer;
      }
    }

    .num {
      display: flex;
      align-items: center;
      flex-direction: column;
      justify-content: center;
      width: 80px;
      height: 80px;
      background-color: var(--light-gray);
      border-radius: 20px;
      cursor: pointer;
      color: aliceblue;
      font-size: 26px;
      font-weight: 400;
    }

    .oprations {
      background-color: var(--green);
      font-size: 48px;
      font-weight: 600;
    }

    .divide {
      svg{
        color: whtie;
        
      }
    }
    .multiple{
      padding-top: 15px;
    }
  }
}
</style>
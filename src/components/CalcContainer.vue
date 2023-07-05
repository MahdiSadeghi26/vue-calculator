<script setup>
    methods: {
      
    }
</script>
<template >
  <div class="calcContainer">
    <div class="monitor"></div>
    <div class="keys">
      <div class="firstRow">
      <div class="key oprations">C</div>
      <div class="key oprations multiple">*</div>
      <div class="key oprations">/</div>
      <div class="key oprations">-</div>
    </div>
    <div class="secondRow">
      <div class="key">7</div>
      <div class="key">8</div>
      <div class="key">9</div>
      <div class="key oprations">+</div>
    </div>
    <div class="thirdRow">
      <div class="key">4</div>
      <div class="key">5</div>
      <div class="key">6</div>
      <div class="key oprations">%</div>
    </div>
    <div class="forthRow">
      <div class="key">1</div>
      <div class="key">2</div>
      <div class="key">3</div>
      <div class="key oprations">=</div>
    </div>
    <div class="fifthRow">
      <div class="key zero">0</div>
      <div class="key">.</div>

    </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
  .calcContainer{
    width: 400px;
    height: 500px;
    background-color: var(--dark-gray);
    padding: 20px;
    border-radius: 10px;
    .monitor{
      width: 100%;
      height: 20%;
      background-color: var(--light-gray);
      border-radius: 10px;
    }
    .keys{
      &:hover{
        cursor: pointer;
      }
      margin-top: 15px;
      .firstRow,.secondRow,.thirdRow,.forthRow{
        display: flex;
        justify-content: space-between;
        margin-bottom: 15px;
      }
      .fifthRow{
        display: flex;
        justify-content:space-between;
        .zero{
          width: 74%;
        }
      }
      color: aliceblue;
      .key{
        display: flex;
        justify-content: center;
        align-items: center;
        width: 80px;
        height: 60px;
        background-color: var(--light-gray);
        border-radius: 10px;
        font-size: 26px;
      }
      .oprations{
        background-color: var(--green);
        font-size: 30px;
        font-weight: 400;
      }
      .multiple{
        padding-top: 10px;
      }
  }
}
</style>
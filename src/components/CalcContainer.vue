<template >
  <div class="calcContainer">
    <div class="monitor">{{ calculatorValue || 0 }}</div>
    <div class="keys">
      <div class="firstRow">
        <div @click="action()" class="key oprations">C</div>
        <div @click="action()" class="key oprations multiple">*</div>
        <div @click="action()" class="key oprations">/</div>
        <div @click="action()" class="key oprations">-</div>
      </div>
      <div class="secondRow">
        <div @click="action()" class="key">7</div>
        <div @click="action()" class="key">8</div>
        <div @click="action()" class="key">9</div>
        <div @click="action()" class="key oprations">+</div>
      </div>
      <div class="thirdRow">
        <div @click="action()" class="key">4</div>
        <div @click="action()" class="key">5</div>
        <div @click="action()" class="key">6</div>
        <div @click="action()" class="key oprations">%</div>
      </div>
      <div class="forthRow">
        <div @click="action()" class="key">1</div>
        <div @click="action()" class="key">2</div>
        <div @click="action()" class="key">3</div>
        <div @click="action()" class="key oprations">=</div>
      </div>
      <div class="fifthRow">
        <div @click="action()" class="key zero">0</div>
        <div @click="action()" class="key">.</div>

      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      calculatorValue: '',
      oprator: null,
      previousCalculatorValue: ''
    }
  }, methods: {
    // append Value
    action() {
      let innerHTML = event.target.innerHTML;
      let eventTarget = event.target;
      if (!isNaN(innerHTML) || innerHTML === '.') {
        this.calculatorValue += innerHTML + ''
      }
      // clear value
      if (innerHTML === 'C') {
        this.calculatorValue = ''
      }
      // precentage
      if (innerHTML === '%') {
        this.calculatorValue = this.calculatorValue / 100 + ''
      }

      if (['/', '*', '-', '+'].includes(innerHTML)) {
        this.oprator = innerHTML;
        this.previousCalculatorValue = this.calculatorValue
        this.calculatorValue = ''
        // changing backgorund color of oprator target
        eventTarget.style.background = '#45CFDD'
        setTimeout(() => {
          eventTarget.style.background = '#40B984'
        }, 1000);
      }
      // result section
      if (innerHTML == '=') {
        this.calculatorValue = eval(
          this.previousCalculatorValue + this.oprator + this.calculatorValue
        )

        this.previousCalculatorValue = ''
        this.oprator = null
      }

    },
  },
}
</script>
<style lang="scss" scoped>
.calcContainer {
  width: 400px;
  height: 500px;
  background-color: var(--dark-gray);
  padding: 20px;
  border-radius: 10px;

  .monitor {
    color: aliceblue;
    width: 100%;
    height: 20%;
    background-color: var(--light-gray);
    border-radius: 10px;
    display: flex;
    align-items: flex-end;
    font-size: 45px;
    justify-content: flex-end;
    padding: 20px;
  }

  .keys {
    &:hover {
      cursor: pointer;
    }

    margin-top: 15px;

    .firstRow,
    .secondRow,
    .thirdRow,
    .forthRow {
      display: flex;
      justify-content: space-between;
      margin-bottom: 15px;
    }

    .fifthRow {
      display: flex;
      justify-content: space-between;

      .zero {
        width: 74%;
      }
    }

    color: aliceblue;

    .key {
      display: flex;
      justify-content: center;
      align-items: center;
      width: 80px;
      height: 60px;
      background-color: var(--light-gray);
      border-radius: 10px;
      font-size: 26px;
    }

    .oprations {
      background-color: var(--green);
      font-size: 30px;
      font-weight: 400;
    }

    .multiple {
      padding-top: 10px;
    }
  }
}
</style>
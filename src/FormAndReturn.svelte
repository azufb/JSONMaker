<script>
  let data = [];
  let message;
  let jsonData = 'Result is here...';

  // 入力された内容を配列に格納。
  function addArray() {
    if (data.value1 == undefined && data.value2 == undefined && data.value3 == undefined && data.value4 == undefined && data.value5 == undefined) {
      message = "1つ以上の値を入力してください。";
      jsonData = message;
      
    } else {
      data = [
        {
          key1: data.value1,
          key2: data.value2,
          key3: data.value3,
          key4: data.value4,
          key5: data.value5,
        },
      ];

      // JSON形式に変換。
      jsonData = JSON.stringify(data);
      let comma = /,/gim;
      let startBrackets = /\[{/gim;
      let endBrackets = /}]/gim;
      let startMiddleBrackets = /{/gim;
      let endMiddleBrackets = /}/gim;
      jsonData = jsonData.replace(comma, ',\n');
      jsonData = jsonData.replace(startBrackets, '');
      jsonData = jsonData.replace(endBrackets, '');
      jsonData = jsonData.replace(startMiddleBrackets, '');
      jsonData = jsonData.replace(endMiddleBrackets, '');
    }
    
  }
</script>

<div class="contentAll">
  <div class="content">
    <div class="form from">
      <div class="inputProperty">
        <label for="label">Key1:</label>
        <input
          type="text"
          bind:value={data.value1}
          placeholder="入力してください1"
        />
      </div>
      <div class="inputProperty">
        <label for="label">Key2:</label>
        <input
          type="text"
          bind:value={data.value2}
          placeholder="入力してください2"
        />
      </div>
      <div class="inputProperty">
        <label for="label">Key3:</label>
        <input
          type="text"
          bind:value={data.value3}
          placeholder="入力してください3"
        />
      </div>
      <div class="inputProperty">
        <label for="label">Key4:</label>
        <input
          type="text"
          bind:value={data.value4}
          placeholder="入力してください4"
        />
      </div>
      <div class="inputProperty">
        <label for="label">Key5:</label>
        <input
          type="text"
          bind:value={data.value5}
          placeholder="入力してください5"
        />
      </div>
    </div>

    <div class="toJSONBtn">
      <button on:click={addArray}>JSON!</button>
    </div>

    <div class="form to">
      <div>
        <p>&#123;</p>
        <p class="jsonAppear">{jsonData}</p>
        <p>&#125;</p>
      </div>
    </div>
  </div>
</div>

<style>
  .contentAll {
    display: flex;
    flex-direction: column;
    height: 100vh;
    padding: 3rem 5rem;
  }

  .content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 100%;
  }

  .form {
    background-color: #c4c4c4;
    height: 100%;
    border-radius: 2.5rem;
  }

  .from {
    width: 40%;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
  }

  .inputProperty {
    display: flex;
    align-items: center;
    padding: 0 1rem;
  }

  .inputProperty:nth-child(1) {
    padding-top: 1rem;
  }

  .inputProperty:nth-last-child(1) {
    padding-bottom: 1rem;
  }

  .inputProperty label {
    padding-right: 2rem;
    font-weight: bold;
  }

  .inputProperty input {
    width: 100%;
    margin: 0;
  }

  .toJSONBtn {
    width: 15%;
  }

  .toJSONBtn button {
    margin-bottom: 0;
    background-color: #2d2c2c;
    border: none;
    border-radius: 15rem;
    color: #ffffff;
    width: 100%;
    padding: 2rem 0;
    font-weight: bold;
    font-size: 24px;
  }

  .to {
    width: 40%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .to div {
    background-color: #ffffff;
    width: 95%;
    height: 95%;
    border-radius: 2rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .to div p {
    padding: 0.5rem;
  }

  .to div p:not(.jsonAppear) {
    margin: 0;
  }

  .jsonAppear {
    white-space: pre-wrap;
    margin-left: 2em;
    font-size: 24px;
  }
</style>

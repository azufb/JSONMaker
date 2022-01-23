<script>
  // 入力された内容を配列に格納。

  // JSON形式に変換。

  // JSON表示。
</script>

<div class="contentAll">
  <div class="content">
    <div class="form from">
      <div class="inputProperty">
        <!-- svelte-ignore a11y-label-has-associated-control -->
        <label>Key1:</label>
        <input type="text" placeholder="入力してください1" />
      </div>
      <div class="inputProperty">
        <!-- svelte-ignore a11y-label-has-associated-control -->
        <label>Key2:</label>
        <input type="text" placeholder="入力してください2" />
      </div>
      <div class="inputProperty">
        <!-- svelte-ignore a11y-label-has-associated-control -->
        <label>Key3:</label>
        <input type="text" placeholder="入力してください3" />
      </div>
      <div class="inputProperty">
        <!-- svelte-ignore a11y-label-has-associated-control -->
        <label>Key4:</label>
        <input type="text" placeholder="入力してください4" />
      </div>
      <div class="inputProperty">
        <!-- svelte-ignore a11y-label-has-associated-control -->
        <label>Key5:</label>
        <input type="text" placeholder="入力してください5" />
      </div>
    </div>

    <div class="toJSONBtn">
      <button>JSON!</button>
    </div>

    <div class="form to">
      <div>
        <p>#Return is here.</p>
      </div>
    </div>
  </div>
</div>

<style>
  .contentAll {
    display: flex;
    flex-direction: column;
    height: 100vh;
    padding: 1.5rem 2rem;
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
    border-radius: 5%;
  }

  .from {
    width: 40%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
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
    border-radius: 15px;
    color: #ffffff;
    width: 100%;
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
    border-radius: 5%;
  }

  .to div p {
    margin: 0;
    padding: 0.5rem;
  }
</style>

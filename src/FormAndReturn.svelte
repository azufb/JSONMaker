<script>
</script>

<div class="contentAll">
  <div class="content">
    <div class="form from">
      <p>#Form is here.</p>
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
  }
</style>

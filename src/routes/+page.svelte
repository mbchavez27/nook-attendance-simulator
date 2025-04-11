<script>
  import "../global.css";

  let inputValue = "";

  const clearValue = () => {
    inputValue = "";
  };
</script>

<div class="content">
  <h1>Nook Attendance Tracker Simulator</h1>
  <div class="tracker">
    <div class="idInput">
      <input type="text" class="idInput" bind:value={inputValue} />
    </div>
    <div class="numpad">
      <button
        on:click={() => {
          inputValue += "1";
        }}>1</button
      >
      <button
        on:click={() => {
          inputValue += "2";
        }}>2</button
      >
      <button
        on:click={() => {
          inputValue += "3";
        }}>3</button
      >
      <button
        on:click={() => {
          inputValue += "4";
        }}>4</button
      >
      <button
        on:click={() => {
          inputValue += "5";
        }}>5</button
      >
      <button
        on:click={() => {
          inputValue += "6";
        }}>6</button
      >
      <button
        on:click={() => {
          inputValue += "7";
        }}>7</button
      >
      <button
        on:click={() => {
          inputValue += "8";
        }}>8</button
      >
      <button
        on:click={() => {
          inputValue += "9";
        }}>9</button
      >
      <button
        on:click={() => {
          inputValue += "0";
        }}>0</button
      >
    </div>
    <div class="enter">
      <button
        on:click={() => {
          alert("ID Number: " + inputValue);
        }}>Enter</button
      >
      <button on:click={clearValue}>Clear</button>
    </div>
  </div>
</div>

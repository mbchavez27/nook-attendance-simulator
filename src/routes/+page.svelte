<script lang="ts">
  import axios from 'axios'
  import '../global.css'

  const BASE_URL = import.meta.env.VITE_API_BASE_URL

  let inputValue = ''
  let response = ''
  let error = ''

  const clearValue = () => {
    inputValue = ''
  }

  async function tapOfficer() {
    try {
      const res = await axios.post(`${BASE_URL}/user`, {
        idNum: Number(inputValue),
      })
      response = res.data.message
      alert(response)
    } catch (err: any) {
      error = err.message
      alert(error)
    }
  }
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
          inputValue += '1'
        }}>1</button
      >
      <button
        on:click={() => {
          inputValue += '2'
        }}>2</button
      >
      <button
        on:click={() => {
          inputValue += '3'
        }}>3</button
      >
      <button
        on:click={() => {
          inputValue += '4'
        }}>4</button
      >
      <button
        on:click={() => {
          inputValue += '5'
        }}>5</button
      >
      <button
        on:click={() => {
          inputValue += '6'
        }}>6</button
      >
      <button
        on:click={() => {
          inputValue += '7'
        }}>7</button
      >
      <button
        on:click={() => {
          inputValue += '8'
        }}>8</button
      >
      <button
        on:click={() => {
          inputValue += '9'
        }}>9</button
      >
      <button
        on:click={() => {
          inputValue += '0'
        }}>0</button
      >
    </div>
    <div class="enter">
      <button
        on:click={() => {
          tapOfficer()
        }}>Enter</button
      >
      <button on:click={clearValue}>Clear</button>
    </div>
  </div>
</div>

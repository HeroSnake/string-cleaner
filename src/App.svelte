<script>
  let inputText = "";
  let outputText = "";

  function removeNullBytes() {
    outputText = inputText.replace(/\u000B/g, " ");
    navigator.clipboard.writeText(outputText);
  }
</script>

<style>
  textarea {
    width: 300px;
    height: 200px;
    margin-bottom: 10px;
  }
  button {
    padding: 8px 16px;
    background-color: #4caf50;
    color: white;
    border: none;
    cursor: pointer;
  }
</style>

<textarea bind:value={inputText}></textarea>
<button on:click={removeNullBytes}>Remove Null Bytes & Copy</button>
<pre style="text-align: left;">{outputText}</pre>

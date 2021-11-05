<script>
  import MessageBar from './MessageBar.svelte'

  function handleMessage(event) {
    alert(event.detail.text)
  }

  let messages = [
    { text: "First Message" },
    { text: "Second Message" }
  ]
  let msg = ""

  const addItem = () => {
    messages = [
      ...messages,
      msg
    ]
  }
</script>

<main>
  <div id="container">
    <ul>
      {#each messages as message}
        <li>message</li>
      {/each}
    </ul>
  </div>
  <MessageBar on:message={handleMessage}/>
</main>

<style>
  div {
    border: 1px solid #e4e4e4;
    height: 80vh;
    padding: 15px;
    margin: 15px;
  }

  ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
  }

  li {
    padding: 0.5rem 1rem;
    animation: fade-in 2s;
  }

  li:nth-child(odd) {
    background: #efefef;
  }

</style>
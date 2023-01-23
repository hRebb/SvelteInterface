<script>
  export let text = "Add Text"

  let newText = ""

  function addText() {
    text = newText
    newText = ""
  }
</script>

<section class="second">
  <form on:submit|preventDefault={addText}>
    <p class="text">{text}</p>
    <br />
    <label>
      Nouveau Texte:
      <input type="text" bind:value={newText} placeholder="Entrez votre texte" />
      <button class="addbtn" type="submit">Ajouter</button>
    </label>
  </form>
</section>
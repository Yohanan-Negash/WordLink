<script lang="ts">
  let scribbledText: String = ''
  let convertedText: String = ''
  let selectedLanguage: String = 'english'

  const translateText = () => {
      if(selectedLanguage === 'english') {
        convertedText = 'English'
      } else if (selectedLanguage === 'amharic'){
        convertedText = 'Amharic'
      }
  }
</script>

<div>
  <div class="mt-5">
    <textarea bind:value={scribbledText} placeholder="Enter word or phrase"></textarea>
  </div>
  <div class="mt-5">
    <select bind:value={selectedLanguage}>
      <option value="english">English</option>
      <option value="amharic">Amharic</option>
    </select>
  </div>
  <div class="mt-5">
    <input type="text" bind:value={convertedText} readonly>
  </div>
  
  <button class="mt-5 rounded-sm border-black border-solid border-2 p-2 " on:click = {translateText}>
    Convert
  </button>
</div>


<template>
    <div >
        <div
            contenteditable class="text"
            @keypress="handleEnter"
            @paste.prevent="handlePaste"
        >
          <b>134</b> <p>2423434</p>
            
        </div>
    </div>
</template>

<script>
export default {
    methods: {
      handleEnter(event) {
        if (event.key === 'Enter') {
          event.preventDefault(); // Запобігаємо стандартній поведінці
          document.execCommand('insertHTML', false, '<br><br>'); // Вставляємо два <br> для нового рядка
        }
      },
      handlePaste(event) {
        const text = (event.clipboardData || window.clipboardData).getData('text');
        document.execCommand('insertHTML', false, text.replace(/(?:\r\n|\r|\n)/g, '<br><br>')); // Заміна нових рядків на <br>
      }
  },
}
</script>

<style lang="scss">
.text{
    border: 1px solid #ccc;
    padding: 20px;
    border-radius: 20px;
    outline: none;
}
</style>
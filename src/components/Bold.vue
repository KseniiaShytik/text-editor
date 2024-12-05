<template>
    <div class="bold-wrap" @click="boldSelectedText" >
      <img src="@/assets/bold.svg" alt="bold">
    </div>
</template>

<script>
export default {
  name: "Bold",
  data() {
    return {
      isBold: false
    }
  },
  methods: {
    boldSelectedText() {
      const selection = window.getSelection();
      selection.extentNode.parentNode.localName !== 'b' ? this.isBold = false : this.isBold = true

      if (selection.rangeCount > 0) {
        const range = selection.getRangeAt(0);
        const selectedText = range.toString();

        if (selectedText) {
          // TODO
          if ( selection.extentNode.parentNode.localName === 'span' ) {
            range.startContainer.parentNode.remove()
          }
          
          if ( this.isBold ) {
            const newSpan = document.createElement("span");
            newSpan.textContent = selectedText;
            range.startContainer.parentNode.remove()
            range.insertNode(newSpan);
            return;
          }

          const span = document.createElement('b');
          span.textContent = selectedText;
          range.deleteContents();
          range.insertNode(span);
          this.isBold = true
        }
      }
    }
  }
}
</script>


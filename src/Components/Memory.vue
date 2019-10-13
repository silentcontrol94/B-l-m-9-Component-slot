<template>
  <div>
    <div>
      <slot name="heading"></slot>
    </div>
    <div>
      <slot></slot>
    </div>
    <div class="memory">
      <slot name="author">
        <h3>Author</h3>
        <p>Buraya herhangi bir içerik gelmemiş.</p>
      </slot>
    </div>
  <section>
      <h1>This is fancy...</h1>
      <p> {{   }} </p>
    </section>
    <app-slot>
      <h2>Slotla Gönderilen Default İnfo</h2>
      <p slot="secret">Secret Bilgi</p>
    </app-slot>
  </div>
</template>
<script>
import Slot from "./Slot"
export default {
  props : ["content"],
  components : {
    appSlot : Slot
  }
}
</script>
<style scoped>
  div {
    border: 1px solid #ccc;
    box-shadow: 1px 1px 2px #666;
    padding: 20px 20px;
    margin-top: 20px;
  }
  section {
    padding: 4em;
  } h1{
    font-size : 3em;
    margin : 2em auto;
    width: 70%
  }
  section h1::before {
      content: '';
      border-top : 5px solid rgb(173, 172, 172);
      display: block;
      margin-bottom: 0px;
      width: 60%
    }
</style>

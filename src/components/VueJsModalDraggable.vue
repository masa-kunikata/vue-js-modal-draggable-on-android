<template>
  <div class="wrap">
    <button @click="msg= ''; $modal.show('partial-draggable')">partial draggable</button>

    <modal name="partial-draggable" draggable=".draggable-area">
      <div class="draggable-area">
        draggable area<br>
        <button @click="msg = 'draggable area button clicked.'">button</button><br>
        <input type="button" value="input type=button" @click="msg = 'draggable area input type=button clicked.'"><br>
        <a href="#" @click="msg = 'draggable area anchor clicked.'">anchor link</a><br>
        <label @click="msg = 'draggable area label clicked.'">
          label
          <input type="text">
        </label>
        
      </div>
      <div class="no-draggable-area">
        no draggable area<br>
        <button @click="msg = 'button clicked.'">button</button><br>
        <input type="button" value="input type=button" @click="msg = 'input type=button clicked.'"><br>
        <a href="#" @click="msg = 'anchor clicked.'">anchor link</a><br>
        <label @click="msg = 'label clicked.'">
          label
          <input type="text">
        </label>

        <hr/>
        <div>{{msg}}</div>
      </div>
    </modal>

    <button @click="msg= ''; $modal.show('whole-draggable')">whole draggable</button>

    <modal name="whole-draggable" :draggable="true">
      draggable area<br>
      <button @click="msg = 'draggable area button clicked.'">button</button><br>
      <input type="button" value="input type=button" @click="msg = 'draggable area input type=button clicked.'"><br>
      <a href="#" @click="msg = 'draggable area anchor clicked.'">anchor link</a><br>
      <label @click="msg = 'draggable area label clicked.'">
        label
        <input type="text">
      </label>
      
      <hr/>
      <div>{{msg}}</div>
    </modal>

  </div>
</template>

<script>
export default {
  name: 'VueJsModalDraggable',
  data: () => ({
    msg: '',
  }),
}
</script>

<style scoped>
.wrap {
  font-size: 0.9rem;
}
.draggable-area {
  background-color: #ccc;
}
</style>

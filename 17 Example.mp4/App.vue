<template>
  <div id="app">

    <h1> {{ AppMessage }} </h1>

    <nestedone :message="AppMessage" @BubbleOne=" AppMessage = $event "></nestedone>

  </div>
</template>

<script>
import nestedone from './components/NestedOne';

export default {
  name: 'app',
  data()
  { 
    return { AppMessage: "App Message Here!" }
  },
  components:{ nestedone }
}
</script>

<style>

  body
  {
    padding: 25px;
    font-family: "helvetica";
    box-sizing: border-box;
  }

  #app > section
  {
    margin: 25px;
  }

  h1
  {
    font-size:20px;
    font-weight: normal;
    color: #333;
  }

  #app > h1
  {
    margin: 0;
    font-size: 25px;
  }

  section
  {
    margin: 25px 0 0 0;
    padding: 25px;
    border-radius: 5px;
    background: rgba(200,200,200,0.4);
  }

  section h1
  {
    padding: 0;
    margin: 0;
  }
</style>

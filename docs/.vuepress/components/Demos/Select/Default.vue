<template lang="html">
  <div class="con-select-example">
    {{select1}}
    <input type="text" name="" value="">
    <vs-select
    vs-multiple
      class="selectExample"
      v-model="select1"
      >
      <vs-select-item :vs-text="option.text" :key="index" v-for="option,index in options3" :vs-value="option.value">
      </vs-select-item>
    </vs-select>
    {{select2}}
    <vs-select
      vs-multiple
      vs-autocomplete
      vs-color="rgb(22, 185, 112)"
      class="selectExample"
      v-model="select1"
      >
      <vs-select-item :vs-text="option.text" :key="index" v-for="option,index in options3" :vs-value="option.value">
      </vs-select-item>
    </vs-select>
    <!-- <vs-select
    class="selectExample"
      label="Figuras"
      v-model="select3"
      :options="options3"
      ></vs-select>
      <vs-select
      class="selectExample"
        disabled="true"
        label="Colores"
        v-model="select2"
        :options="options2"
        ></vs-select> -->
  </div>
</template>

<script>
export default {
  name:'',
  data(){
    return {
      select1Normal:'',
      select1:[],
      select2:'',
      select3:1,
      options1:[
        {text:'IT',value:0},
        {text:'Blade Runner',value:2},
        {text:'Thor Ragnarok',value:3},
      ],
      options2:[
        {text: 'Red', value: 1},
        {text: 'Green', value: 2},
        {text: 'Blue', value: 3},
        {text: 'Purple', value: 4},
      ],
      options3:[
        {text: 'Square', value: 1},
        {text: 'Rectangle', value: 2},
        {text: 'Rombo', value: 3},
        {text: 'Romboid', value: 4},
        {text: 'Trapeze', value: 5},
        {text: 'Triangle', value: 6},
        {text: 'Polygon', value: 7},
        {text: 'Regular polygon', value: 8},
        {text: 'Circumference', value: 9},
        {text: 'Circle', value: 10},
        {text: 'Circular sector', value: 11},
        {text: 'Circular trapeze', value: 12},
      ]
    }
  },
  methods:{
    prueba(){
      console.log("prueba de focsu");
    }
  }
}
</script>

<style lang="css">
.selectExample {
  margin: 10px;
}
.con-select-example {
  display: flex;
  align-items: center;
  justify-content: center;
}
.con-select .vs-select {
  width: 100%
}
@media (max-width: 550px) {
  .con-select {
    flex-direction: column;
  }
  .con-select .vs-select {
    width: 100%
  }
}
</style>

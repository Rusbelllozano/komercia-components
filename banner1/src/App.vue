<template>
  <div id="app">
    <!-- <banner1/> -->
    <setting :setting="setting"/>
    <banner2 :setting="setting"/>
  </div>
</template>

<script>
import banner1 from './components/banner1'
import setting from './components/setting'
import banner2 from './components/banner2'


export default {
  name: 'App',
  components: {
    banner1,
    setting,
    banner2,
  },
  data(){
    return {
      setting: [{
        photo: 'https://images.pexels.com/photos/910329/pexels-photo-910329.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940',
        title: 'SUMMER',
        description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ',
        redirect_url: '',
        button_text: 'SHOP NOW',
      },
      {
        photo: 'https://images.pexels.com/photos/1153838/pexels-photo-1153838.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940',
        title: 'SPRING',
        description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
        redirect_url: '',
        button_text: 'SELL IT',
      }]
    }
  }
}

</script>

<style>
*{
  padding: 0;
  margin: 0;
}
</style>

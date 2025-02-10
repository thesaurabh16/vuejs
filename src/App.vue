<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <!-- <ComputedProperties/> -->
  <!-- <FormHandling/> -->
  <!-- <Methods/>
  <HomePage />
 <DataBinding />
 <EventHandling />
 <Directives/>
 <Parent/>
 <Child/> -->
 <!-- <Watchers/> -->
 <!-- <props name="gautam" heroName="Batman"/>
 <props name="bibek" heroName="superman"/>
 <props name="aviraj" heroName="ironman"/>
 <props :name="name" :heroName="channel"/> -->
  <!-- <Article id="my-article" title="Article Title" :likes="50" :isPublished="true" /> -->
   <!-- <button @click="showPopup = true">Show Popup</button>
   <Popup v-show="showPopup" @close="closePopup"/> -->
   <!-- <Vmodel />
   <Input v-model="surname"/> -->
   <!-- <Card></Card>
   <Card >Card Content</Card>
   <Card ><h2>card Content</h2></Card>
   <Card ><img src="https://picsum.photos/200" /></Card>
   <Card>
    <template v-slot:header>
      <h3>Header</h3>
   </template >
   <template v-slot:default>
    <img src="https://picsum.photos/200" />
   </template>
   <template v-slot:footer>
    <button>View Details</button>
   </template>
  </Card> -->
   <!-- <Slots>
    <template v-slot:default="slotProps">
      {{ slotProps.firstName }} {{ slotProps.lastName }}
    </template>
   </Slots>
   <Slots>
    <template v-slot:default="slotProps">
      {{ slotProps.lastName }}, {{ slotProps.firstName }}
    </template>
   </Slots>
   <Slots>
    <template v-slot:default="slotProps">
      {{ slotProps.firstName }} 
    </template>
   </Slots> -->
   <!-- <h4>App Component text</h4>
   <ChildStyle><h4>Childstyles Component text</h4></ChildStyle> -->
   <button @click="activeTab = 'TabA' " >Tab A</button>
   <button @click="activeTab = 'TabB' ">Tab B</button>
   <button @click="activeTab = 'TabC' ">Tab C</button>
   <!-- <TabA v-if="activeTab === 'TabA'"/>
   <TabB v-if="activeTab === 'TabB'"/>
   <TabC v-if="activeTab === 'TabC'"/> -->
   <KeepAlive>
   <component :is="activeTab"/>
  </KeepAlive>
  <!-- <Teleport to="#portal-root">
    <Portal/>
  </Teleport> -->
  <!-- <Father/> -->
  
  
</template>

<script>


// import FormHandling from './components/FormHandling.vue';
// import ComputedProperties from './components/computedProperties.vue';
// import Article from './components/Article.vue';
// import ChildStyle from './components/ChildStyle.vue';
// import Father from './components/Father.vue';
import HelloWorld from './components/HelloWorld.vue';

// import Portal from './components/Portal.vue';
import TabA from './components/TabA.vue';
import TabB from './components/TabB.vue';
import TabC from './components/TabC.vue';
// import Slots from './components/Slots.vue';
// import Card from './components/Card.vue';
// import Input from './components/input.vue';
// import Popup from './components/Popup.vue';
// import Vmodel from './components/Vmodel.vue';
// import Props from './components/props.vue';
// import Watchers from './components/Watchers.vue';
// import HomePage from './components/HomePage.vue';
// import DataBinding from './components/DataBinding.vue';
// import EventHandling from './components/EventHandling.vue';
// import Directives from './components/Directives.vue';
// import Parent from './components/Parent.vue';
// import Child from './components/Child.vue';
// import Methods from './components/Methods.vue';



export default {
  name: 'App',
  components: {
    HelloWorld,
    // ComputedProperties,
    // Watchers,
    // Props,
    // Article
    // FormHandling
    // HomePage,
    // DataBinding,
    // EventHandling,
    // Directives,
    // Parent,
    // Child,
    // Methods
    // Popup,
    // Vmodel,
     // Input,
    //  Card,
    //  Slots,
    // ChildStyle,
    TabA,
    TabB,
    TabC,
    // Portal
    // Father,
   
     
       
  },
  data(){
    return{
      name:'saurabh',
      channel:'nepaltv',
      showPopup:false,
      surname:'',
      activeTab:'TabA'
    }
  },
  methods:{
    closePopup(name){
      this.showPopup = false
      console.log('name',name)
    }
  }
}
</script>
<style scoped>
#app{
    font-family: Arial, Helvetica, sans-serif;
    -webkit-font-smoothing:antialiased;
    -moz-osx-font-smoothing:grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
h4{
  color:aqua
}
</style>



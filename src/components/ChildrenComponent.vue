<template>
<div>
  <h1>Children component</h1>
  <h3>userName of ChildrenComponent : {{ userNameProps }}</h3>
  <h3>Age of ChildrenComponent : {{ ageProps }}</h3>
  <h3>ChildrenComponent : {{ Nameprops }}</h3>
</div>
</template>

<script setup>
    const {userNameProps,ageProps,userInfoProps,Nameprops} = defineProps(["userNameProps","ageProps","userInfoProps","Nameprops"]);
    console.log("userInfoProps",userInfoProps);
    
   
    
</script>

<style>

</style>
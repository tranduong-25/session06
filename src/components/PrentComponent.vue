<template>
    <div>
        <h1>Parent Component</h1>
        <h3>userName of ParentComponent : {{ userName }}</h3>
        <h3> ParentComponent : {{ Name }}</h3>
        <p>------------------------------------------</p>
        <ChildrenComponent :userNameProps="userName" :ageProps="age" :userInfoProps="userInFo" :Nameprops="Name"/>
    </div>
  
</template>

<script setup>
    import ChildrenComponent from './ChildrenComponent.vue';
    const userName = "Nguyen Van A"
    const age = 20
    const userInFo ={
        id : 1,
        name:"Nguyễn Văn B",
        age:21,
    }
    const Name = "Rikkei Academy"
</script>

<style>

</style>
<script>
export default {
name:'MainComp'
}
</script>

<template>
<main>
  <div class="content">
    <h2>Content Goes Here</h2>
  </div>
</main>


</template> 

<style lang="scss" scoped>
@use '../styles/varibles' as *;

main{
  max-width: 100%;
  background-color: #1C1C1C; 
 .content{
height: 120px;
width: 70%;
display: flex;
align-items: center;
margin: auto;
h2{
  color: white;
}
} 
}

</style>
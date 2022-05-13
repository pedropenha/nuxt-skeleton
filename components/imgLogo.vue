<template>
    <div class="img">
        <img src="../static/img/logo.svg" :style="'max-width:'+maxWidth+';'"/>
    </div>
</template>

<script>
export default{
    props:{
        maxWidth: {
            type: String,
            required: true
        }
    }
}
</script>
<style scoped>
.img{
  display: flex;
  width: 100%;
  justify-content: center;
}

.img > img{
  max-width: 200px;
  width: 100%;
  height: 100%;
}
</style>

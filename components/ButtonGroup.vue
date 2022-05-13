<template>
    <button :class="color+' button--modal button'">
        <span class="button--frase">{{ labelButton }}</span>
    </button>
</template>

<script>
export default{
  props:{
    labelButton:{
        type: String,
        required: true
    },
    color:{
      type: String,
      required: true
    }
  }
}
</script>
<style scoped>
.button{
    cursor: pointer;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    align-content: center;
    border-radius: 4px;
    border: none;
}

.button--frase{
    font-size: 18px;
    font-family: Arial, Helvetica, sans-serif;
    padding: 7px;
    font-weight: 500;
}

.primary{
  background: rgba(6, 37, 98, 0.8);
  box-shadow: 0px 10px 1px #062562;
  border-color: #062562;
}

.primary:hover{
  box-shadow: 0px 8px 1px #062562;
  transition: all .1s ease-out;
}

.secondary{
  background: rgba(53, 61, 159, 0.8);
  box-shadow: 0px 10px 1px #353D9F;
  border-color: #353D9F;
}

.secondary:hover{
  box-shadow: 0px 8px 1px #353D9F;
  transition: all .1s ease-out;
}

.info{
  background: rgba(81, 99, 247, 0.8);
  box-shadow: 0px 10px 1px #5163F7;
  border-color: #5163F7;
}

.info:hover{
  box-shadow: 0px 8px 1px #5163F7;
  transition: all .1s ease-out;
}

.warning{
  background: rgba(255, 201, 0, 0.8);
  box-shadow: 0px 10px 1px #FFC900;
  border-color: #FFC900;
}

.warning:hover{
  box-shadow: 0px 8px 1px #FFC900;
  transition: all .1s ease-out;
}

.success{
    background: rgba(23, 133, 36, 1);
    /* box-shadow: 0px 8px 1px #178524;
    border-color: #178524; */
    border-bottom: 4px solid darkgreen !important;
    color: white;
    transition: all .1s ease-out;
}

.success:hover{
    background: rgb(21, 123, 32);
    border-bottom: 3px solid darkgreen !important;
    /* box-shadow: 0px 8px 1px #178524; */
    
}

.danger{
  background: rgba(213, 27, 64, 0.8);
  box-shadow: 0px 10px 1px #D51B40;
  border-color: #D51B40;
}

.danger:hover{
  box-shadow: 0px 8px 1px #D51B40;
  transition: all .1s ease-out;
}

.light{
  background: rgba(255, 255, 255, 0.8);
  box-shadow: 0px 10px 1px #f2f2f2;
  border-color: #f2f2f2;
}

.light:hover{
  box-shadow: 0px 8px 1px #f2f2f2;
  transition: all .1s ease-out;
}
</style>

<template>
    <div class="form">
        <div class="form-label">
            <label :for="id">{{textoLabel}}</label>
        </div>
        <div class="form-input">
            <input class="form-control" :type="tipo" :name="name" :id="id" :placeholder="textPlaceholder">
        </div>
    </div>
</template>

<script>
export default{
  props:{
    tipo:{
        type: String,
        required: true
    },
    name:{
      type: String,
      required: true
    },
    id:{
        type: String,
        required: true
    },
    textoLabel:{
        type: String,
        required: true
    },
    textPlaceholder:{
        type: String,
        required: true
    }
  }
}
</script>
<style scoped>
.form-control{
    margin-top: 5%;
    width: 100%;
    border-top: none;
    border-left: none;
    border-right: none;

    border-bottom: 2px solid #6c6c6c;
    transition: all .2s ease-in-out;

    font-family: Arial, Helvetica, sans-serif;
    font-size: 18px;
}

.form-control:hover{
    border-color: #202020;
}

.form-control:focus{
    border-bottom: 2px solid #202020;
    outline: none;
}

.form{
    width: 100%;
}

.form-label{
    font-size: 18px;
    font-family: Arial, Helvetica, sans-serif;
    color: rgb(82, 82, 82);
}

.form-input{
    overflow: hidden;
    width: 100%;
}
</style>

<template>
<div class="wrap-content-all"> 
    <div class="wrap-content">
       <p class="content-header">
           Nội dung 18+, vui lòng đăng nhập trước khi xem.
       </p>
       <input 
            class="text-input" 
            v-model="email"
            type="text" 
            placeholder="Email hoặc Số điện thoại"> 
       <input 
            class="text-input" 
            v-model="password"
            type="text" 
            placeholder="Mật Khẩu">
       <button
       @click="submit"
        class="btn-submit">
        Đăng Nhập
        </button>
    </div>
</div>
</template>

<script>
export default {
    data(){
        return{
            email : '',
            password : ''
        }
    },
    methods: {
        submit: function(){
            if(this.email === 'admin' && this.password === '123456'){
                alert('OKE');
            }else       
                    {
                        alert('NOT Oke')
                    }                  
        }
    }
    
}
</script>

<style>
.wrap-content{
    background-color: #eceff5;
    margin: 0px auto;
    width: 400px;
    padding: 15px;
}
.content-header{
    background-color: #fff9d7;
    margin: 3px auto;
    padding: 10px;
    border: 1px solid #e2c822;
    text-align: left;
    font-size: 14px;
    line-height: 18px;
    direction: ltr;
    font-family: helvetica, arial, sans-serif;

}
.text-input{
    display: block;
    font-size: 14px;
    line-height: 18px;
    width: 99%;
    height: 30px;
    
}

.btn-submit{
     background-color: #627aad;
     margin-top: 5px;
     padding: 12px;
     text-align: center;
     vertical-align: middle; 
     border-radius: 4px;
     width: 100%;
     box-sizing: border-box;
     font-weight: bold;
     color: white;
}


</style>



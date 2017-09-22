在vue.js里面
1.可以使用jQuery的AJAX
2.vue-resource
   目前已经不再维护，建议用axios
   使用方式：
       需要引入vue-resource
       引入后再vue里面直接使用
       this.$http.get()
       this.$http.post("url链接"，传的参数)

   http请求方式
   get(url,[options])
   head(url,[options])
   delete(url,[options])
   jsonp(url,[options])
   post(url,[body],[options])
   put(url,[body],[options])
   patch(url,[body],[options])

3.axios
   支持：post get
   自己本身不支持jsonp

   使用方式：
       引入axios插件


       axios.get()
       可以选择两种传参方式：
       1.直接在URL后面拼接
           user?id=12345
       2.在第二个参数传参
           axios.get("/user",{
             params: {
             ID:12345
             }
           }).then(function(res){

           }).catch(function(error){

           });



       axios.post()
             axios.post("/user",{
                  firstName: "xxx",
                  lastName: "yyy"
                  }).then(function(res){

                  }).catch(function(error){

             });

传参有区别
一:VUE 框架的input上传前客户端获取视频信息

//HTML
<input type="file" id="filepicker" accept="video/mp4" @change="chooseVideoInput" class="uploadVideo_input">
    <video id="video" poster="封面图路径" :src="video_url" :controls="controls" x5-playsinline="" playsinline="" webkit-playsinline preload="auto"></video>
//JavaScript 
    chooseVideoInput(event) {
        var files = document.getElementById("filepicker").files[0];
        var url = URL.createObjectURL(files);
        this.video_url= url;
    },
 
    
    :controls="controls" x5-playsinline="" playsinline="" webkit-playsinline preload="auto"

--------------------- 
二:VUE框架获取图片的--input
  
  <input id="filepicker" @change="chooseImgInput" type="file" class="upload_icon">
    <img :src="imgUrl" src=""> 
 
    chooseImgInput(event) {
        var files = document.getElementById("filepicker").files[0];
        var url = URL.createObjectURL(files);
        this.imgUrl = url;
    }
--------------------- 
二-1:获取图片,方法2

   <input id="filepicker" @change="chooseImgInput" type="file" class="upload_icon">
    <img :src="imgUrl" src=""> 
 
    chooseImgInput(event) { //选择图片加载到图片裁剪工具里
        var that = this;
 
        var files = document.getElementById("filepicker").files[0];
        this.fileName = files.name;
 
        var reader = new FileReader();
        reader.readAsDataURL(files);
            reader.onload = function(e) {
            that.visible = true;
            that.imgUrl = this.result;
        }
 
    },
--------------------- 

# uploadFileDemo
前端文件上传和调用摄像头原理和DEMO
<pre>
上传文件到后台。

<input type='file' accept='image/*' capture='camera'>    //capture='camera' 可调用摄像头（不兼容部分手机----小米）
	
H5添加了一个新的接口——FormData。利用 FormData 对象，我们可以通过 JavaScript 用一些键值对来模拟一系列表单控件。

var file=e.target.files || e.dataTransfer.files;   //获取input的文件
var formData=new FormData();     //创建一个FormData空对象
formData.append('file',file[0])  //然后用append方法给对象添加key/value    键 值对

//然后用ajax方法把formData对象传到后台服务器。
$.ajax({
	url:'',
	data:formData,
	……
})
//图片替换 在本地浏览器选好图片后，替换选中的图片
var avatarImg=e.target.files || e.dataTransfer.files;
src = window.URL.createObjectURL(avatarImg[0])
</pre>


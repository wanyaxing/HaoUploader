# HaoUploader
The uploader of Image, support single image or multiple images.

* 此脚本会自动处理class为 input_which_upload_to_qiniu 的INPUT，从而支持图片上传或修改。
* 如果需要自定义图片缩略图的大小，请自定义相关css。
* 通过HaoUploader.init($('.input_which_upload_to_qiniu')[0])可以初始化对应的input元素，获得uploader对象。
* 再次使用HaoUploader.init($('.input_which_upload_to_qiniu')[0])，可以重新获得对应的uploader对象。
* 如果在其他地方修改input值后，可使用uploader.updateDNDOfInputValue()方法，来刷新预览区的缩略图。（如AJAX交互更新了input中的值之后，需要刷新预览区）。
* 使用方案一：PHP预置值到input的value后输出HTML代码即可。
* 使用方案二：在前端页面，使用ajax读取数据后，将取得的url赋值进对应的input，然后调用uploader.updateDNDOfInputValue方法，刷新预览区。


注：核心上传插件为[webUploader](http://fex.baidu.com/webuploader/).

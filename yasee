// ==UserScript==
// @icon            https://appstatic.yaseok.com/static/src/images/favicon.ico
// @name            亚瑟解析器
// @namespace       [url=https://fulibus.net/[/url]
// @author          fuliba
// @description     播放视频
// @include            *yasee5.com/video-*
// @require         http://cdn.bootcss.com/jquery/1.8.3/jquery.min.js
// @version         0.0.1
// @grant           GM_addStyle
// ==/UserScript==
(function() {
    'use strict';

  //获取解析网址
      var m3u8=m3u8_url;
        m3u8=m3u8.replace("[domain_dan]","hone.yyhdyl.com")
        m3u8=m3u8.replace("[domain_fourth]","head2.yyhdyl.com")
        m3u8=m3u8.replace("[domain_shuang]","htwo.yyhdyl.com")
        m3u8=m3u8.replace("[domain_three]","head.yyhdyl.com")
    //创建按钮 位置
    var button1= "<td><a style='width: 60px; margin-left: 5px; margin-bottom: 10px; background: rgb(180, 99, 0); border: 1px solid rgb(180, 99, 0); color: white;'  href='http://youxiji.org/tools/play.php?url="+encodeURIComponent(m3u8)+"' target='_Blank'>";
    var button2="</a></td>" ;
    var button;
    var adress= $("#realviewnum");
    var m_div="<tr id='div_id' ></tr>"
    adress.after(m_div);
    var x=$("#div_id");
  //获取子地址并添加按钮
    $.get(m3u8,function(data,status){
        //alert("Data: " + data + "nStatus: " + status);
        //
        if (data.indexOf('720p') !== -1) {
            button = button1.replace("hls.m3u8","hls-720p.m3u8")+"720p"+button2;
            x.append(button);
            }
        if (data.indexOf('480p') !== -1) {
              button =  button1.replace("hls.m3u8","hls-480p.m3u8")+"480p"+button2;
                x.append(button);
            }
        if (data.indexOf('360p') !== -1) {
          button =  button1.replace("hls.m3u8","hls-360p.m3u8")+"360p"+button2;
          x.append(button);
            }
        if (data.indexOf('240p') !== -1) {
          button =  button1.replace("hls.m3u8","hls-240p.m3u8")+"320p"+button2;
          x.append(button);
            }   

      
    });
   
    
})();

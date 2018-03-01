# xcx_dom_menu_1
no
 // 事件驱动内容获取
 <view class="nal">
    <text data-text="内容" bindtap="tabs">内容</text> 
 </view>   
 
 // 通过事件驱动
tabs: function(e){
  console.log(e.currentTarget.dataset.text)
 }
 
 //wxml
 <view class="list-wrapper">
      <view class="list-top">
         <view data-num="1" class="list-menu list-menu1 {{_num==1?'cur':''}}" bindtap="menuClick">头条</view>
         <view data-num="2" class="list-menu list-menu2 {{_num==2?'cur':''}}" bindtap="menuClick">活动</view>
         <view data-num="3" class="list-menu list-menu3 {{_num==3?'cur':''}}" bindtap="menuClick">公告</view>
      </view>
</view>
//js
menuClick:function(e){
      this.setData({
         _num:e.target.dataset.num
      })
  },

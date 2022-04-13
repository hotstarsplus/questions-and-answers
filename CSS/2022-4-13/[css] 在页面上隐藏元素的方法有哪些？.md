# [css] 在页面上隐藏元素的方法有哪些？

**占位**:
visibility: hidden; //页面会渲染只是不显示
margin-left: -100%;
opacity: 0; //看不见，但是会占据空间,不透明度。
transform: scale(0);

**不占位:**
display: none;  //页面不会渲染
width: 0; height: 0; overflow: hidden; //切掉

**仅对块内文本元素:**
text-indent: -9999px;
font-size: 0;

**利用 position （absolute 的情况下）**
left/right/top/bottom: 9999px/-9999px 让元素在视区外
z-index: -9999 放到最底层，同一位置可以让其他元素把这个给遮掉

### 满屏单页面适配问题的解决方案

起因：在做一些H5营销案例的时候，因为大多数的H5都是单页面满屏的。曾经采取的方案也比较简单，无论元素的大小，还是字体以及元素的位置布局，都是使用一套rem单位。

所有元素都使用一套rem单位的优点在于所有元素都可以对照着设计稿，在不同的设备下都等比的缩放。

但是，因为各设备屏幕的宽高比都是不一样的，而此时如果我们布局中存在某些元素是贴在页面的底部边缘的话，去到某些设备下可能会导致这些元素被挤下去了，挤到了屏幕的边缘外。需要拖拽滚动条才能正常的看到底部元素。

这对于我们的这种满屏的H5案例肯定是不能接受的。

#### 解决方案

目前想到的解决方案比较简单，配合rem单位以及vh单位。

在元素的大小布局上，我们可以使用rem来进行设值。而具体到某个元素的高度定位，则转换为使用vh单位布局。这样就可以保证在不同的设备下，既能让元素正常的缩放，同时又可以保证页面可以正常的显示所有的内容。

#### 实践

rem以及vh单位的换算可以通过scss转换，不需要手动换值。

字体方面找到一篇玉伯的文章，里面提到字体不要使用rem单位，因为会转换到一些奇怪的px最终导致字体效果奇怪。他推荐字体直接使用px单位。

另外就是vh单位可能会存在兼容性的问题，具体还有待测试。


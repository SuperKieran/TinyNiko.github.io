# seccon ctf 2018

比赛的时候只做了两道apk的re的题目，关键是两道都没做出来，感觉自己很没有耐心。两道题都是u3d的题目。一道是dll ，一道是il2cpp

# block.apk
这题的界面上有一个flag在旋转，但是中间部分被一个块挡住了，无法看到原始的flag，想法就是让这个块变成透明，这样就可以看到flag了，或者把flag提取出来，然后用工具查看里面的内容。块透明这个涉及到较深的知识，我没有选择去做。于是就去用工具提取flag。首先用dnspy看了一下代码，没什么重要信息。然后用unity studio 也尝试了一下，没有办法。后面想用uabe,但是打开的时候，缺少dll，我就懒得搞，看了writeup之后发现，用这个工具就可以解决。。。简直气死我了。后来看了别的writeup，发现还有一个工具交unity unpacker，功能非常强大，但是不知道为啥他的资源解开以后flag是有点小问题的，这个我也没有想明白。修复了uabe 之后，找到那个块，把这个资源移除就可以看到flag。


# shooter.apk
这题是il2cpp ,众所周知这个有个工具叫il2cppdump ,可以把类什么的dump下来，但是不知道为啥我用这个工具无法dump出来，所以就放弃了。看了writeup之后发现这题竟然还有sql注入什么。。。。
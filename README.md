# Minecraft机制剖析

专栏地址：https://www.bilibili.com/read/readlist/rl337273

在专栏的最开始，我要先感谢Mojang写出了这么有趣的游戏，从没有别的游戏能像Minecraft一样有这么多有意思的机制来让玩家不遗余力地探索。除了红石之外，游戏机制也成了一门学问，倘若不亲自来拜读一下Mojang的源码，上帝也不知道一些神秘的特性是如何产生的，咱或许也会人云亦云地听信一些口口相传的过时甚至错误的信息。

这个专栏打算从源码的角度说明Minecraft中的各类机制，本来只是想作为个人对于Minecraft各类机制的学习笔记，以此来提升自己的姿势水平，不过我觉得将其记录成一篇篇专栏中的文章要比走马观花般在代码编辑器中浏览要有效率地多，如果大家能与我一同从中学习到一些内容，那自然是相当不错的。不过，若文章中有任何错误，请立即向我指出，对于一些没有解释清楚的内容，也请在评论与我一起探讨。

我参考的源码使用的是[DecompilerMC](https://github.com/hube12/DecompilerMC])使用官方提供的混淆表反编译出的Minecraft代码，使用的Minecraft版本均为写文章/看代码时最新版Minecraft Java版，并会在篇首注明版本。 文章的结构大致会由文字描述、调用关系、伪代码、流程图及一些图片构成，因为是从源码角度探索，所以文字描述和代码部分会占较多篇幅，我也会尝试将逻辑描述地尽可能清晰，举一些实际游戏中的例子来说明。伪代码均从反编译的源码中摘取，不改变其中逻辑，并做出大量简化，省略大多数对逻辑不造成影响的参数，并添加巨量注释。另外，代码块的开头也会注明该文件的路径和行数，并梳理出这些函数的调用关系，方便去参考实际上反编译的源码。

那么想说的话就差不多了，就等我慢慢完善专栏中内容吧~
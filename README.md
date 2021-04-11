# YuanShenLauncher
原神官服B服一键启动，无需手动配置，省去了下2个服的力气

【背景故事】
由于首先入坑的是B服的原神，没法跟官服的朋友玩。被迫无奈买了个原神官服的号，B服的号玩了挺久又不想放弃，导致每次都要手动切换2个服的config.ini配置，比较烦人，因此就搞了个一键启动B服和官服的启动器。

【原理】
修改Genshin Impact\Genshin Impact Game中的config.ini即可实现切换服务器，channel=1表示官服，channel=14表示B服，因此只要做个启动器点击对应服务器的入口的同时修改channel的值就可以实现一键换服的功能。采用Python的tkinter窗体框架写的启动器。

【怎么用】
上传的Project内有已经编译好的启动器，在dist文件夹内。直接将编译好的原神启动器.exe放在游戏根目录(如:C:\Genshin Impact)下就行，然后双击这个启动器就可以看到选择服务器的界面。如果提示启动失败则表示位置放的不对。
注：如果自己编译，记得修改编译后的exe文件的名字，原本名字是Launcher.exe会与根目录下的官方的Launcher.exe重名。

【特性】
启动器的界面![image](https://user-images.githubusercontent.com/30500819/114296711-4fac2b80-9adf-11eb-9591-fb9a61d11e4c.png)
启动器背景会自动设置为官方启动器最新的背景图片。

无需自己添加config.ini，会自动检测是否存在condfig.ini，若没有对应的config.ini，则会自动生成一个。

缺点是不能做到不用官方启动器更新游戏，每次更新游戏必须使用官方的启动器先更新再使用此启动器一键换服。根目录下可能会影响到官方启动器的config.ini，因为游戏启动的配置文件和官方启动器的配置文件都叫config.ini，而使用此启动器则必须在启动器所在的目录下有config.ini，会导致2个不同的配置信息写在同一个文件内。至少我测试没啥问题，用起来还是照样用。

【面临的困难】
1.我并没有精通Python，因此可能各位大佬看完代码会觉得是很垃圾。
2.无法做到自动搜索游戏目录，不能做到自动配置，现在的自动配置是依靠扔到游戏根目录下实现，会导致config.ini冲突。手动避免的办法就是手动在源代码中添加根目录，这样就无需放在根目录下。希望有大佬能够给我点指教。
3.无法做到自动更新，没有任何思路想如何将自动更新的功能加入到这个启动器中。
4.本人无艺术水平，UI看起来非常古老，做不出炫酷的效果，还请大佬能够给我的点指教。

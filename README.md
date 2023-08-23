# Investigation-on-Real-time-SDF-Generation-and-Utilizing-SDF-for-Collision-Detection

`VFX` `Signed Distance Fields` `Visual Effects Graphs` `Compute Shader` `Collision` `Boolean`

## Overview
Investigation on Real-time SDF Generation and Utilizing SDF for Collision Detection

为了实现连续且实时的布尔,以及物理计算中的软体实时变形和破碎模拟.
我们拟调研和验证一种基于符号距离函数的碰撞和布尔方式来代替原本的基于网格的显示表达方案.

不幸的是,经过了为期几天的调研,以失败告终.但是其中的经验也弥足珍贵,我有必要记录下来,为其他方向的预研比如软组织渲染提供一些思路.

我主要调研了模型网格实时生成符号距离函数的方式和性能表现,以及符号距离函数通过各种方式(比如cube marching)来实时生成网格的方式.
考虑到实时生成网格后,还需要实时计算法线和纹理等,是一个更具挑战的工作,所以我放弃了sdf经过运算处理后重新生成网格的路线.我使用VFX来处理sdf,
通过粒子渲染来达到一个更好的效果呈现.

接下来我将从几个方面来介绍我的研究:

- 网格实时计算sdf及其性能表现
- sdf实时生成网格以及性能表现
- 粒子和sdf的碰撞
- sdf之间的运算
- 






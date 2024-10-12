# Live2D MODEL

[Live2D 看板娘插件](https://github.com/lrplrplrp/live2d) 上使用的后端模型

自[https://github.com/Akilarlxh/live2d_api](https://github.com/Akilarlxh/live2d_api)修改而来，去掉了PHP API调用，修改了配置结构

## 使用

>   model_list.json
```json
{
  "models": [
    {
      "url":"https://raw.bgithub.xyz/lrplrplrp/live2d_api/master/model/genshin/BCSZ1.1/BCSZ1.1.model3.json",
      "url说明":"模型的结构文件,2.0及以下为 model.json 或 index.json ，3.0以上为 model3.json 结尾",
      "tipsUrl":"./waifu-tips-BCSZ.json",
      "tipsUrl说明":"单模型文本文件地址，若为空，则使用load.js中配置的地址。",
      "config":{
        "x":0,
        "x说明":"模型的横轴偏移，默认为0",
        "y":0,
        "y说明":"模型的纵轴偏移，默认为0",
        "scaleX":1.8,
        "scaleX说明":"模型的横轴缩放，默认为1",
        "scaleY":1.8,
        "scaleY说明":"模型的纵轴缩放，默认为1"
      }
    }
  ]
}
```
-   模型文本文件配置
-   由于文件过长，这里只简单解释下节点分类
-   [messages-模型的特殊情况下的交互](./waifu-tips.json#L2)
-   [mouseover-鼠标悬浮在某些元素上时的交互](./waifu-tips.json#L22)
-   [click-鼠标点击某些元素时的交互](./waifu-tips.json#L313)
-   [timer-满足特定时间时的交互](./waifu-tips.json#L329)
>   waifu-tips-XXX.json
-   为了交互更生动，重新设计了waifu-tips.json的结构，可以在交互的时候触发动作和表情，并为动作添加了文本，但因为每个模型的动作和表情命名并不一样，所以需要单独配置一个文件
-   [waifu-tips-BCSZ.json](./model/genshin/BCSZ1.1/waifu-tips-BCSZ.json#L21)
```json
"selector": "#waifu-tool .fa-paper-plane",
		"interaction":{
			"text": ["要不要来玩飞机大战？", "这个按钮上写着「不要点击」。", "怎么，你想来和我玩个游戏？", "听说这样可以蹦迪！"],
        	"motion":"Start"
		}
```
-   [waifu-tips-BCSZ.json](./model/genshin/BCSZ1.1/waifu-tips-BCSZ.json#L30)
```json
"motion":{
		"Tap早上好":"早，嗯?怎么一副无精打采的样子，没有睡好吗?哎呀，昨晚是去做什么坏事了么?",
		"Tap中午好":"嗯~伤脑筋，中午吃些什么呢?油豆腐吃腻了，想吃点清淡的。话说好久没见到社奉行家的小姑娘了，我们不如就去吃她做的点心吧。",
		"Tap晚上好":"今夜的月光如此清亮，不做些什么真是浪费。随我一同去月下漫步吧，不许拒绝。"
	}
```

## 版权声明

> (>▽<) 都看到这了，点个 Star 吧 ~

**API 内所有模型 版权均属于原作者，仅供研究学习，不得用于商业用途**  

MIT © LRPLRPLRP

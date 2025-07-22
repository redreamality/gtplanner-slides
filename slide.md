---
theme: ./
# title: GTPlanner开源发布会
info: |
  ## GTPlanner开源发布会（思辨版）

  核心基调: 朴实而深刻。没有过分的渲染，而是通过层层剖析，引发听众对工具、创造与系统本质的思考。

  感易智能团队出品
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
layout: section-divider
---

# GTPlanner

## The Agent Builder 核心规划引擎
<!-- 
<div class="pt-12">
<span class="text-sm opacity-75">感易智能</span>
</div> -->

<!--
演讲者说: (语气平静，语速稍慢) "大家好。今天，我们不发布一款产品，而是想和各位探讨一个问题，并分享我们为了解答这个问题，所迈出的第一步。这一步，我们称之为GTPlanner。"
-->

---
layout: two-column
title: "思想，与工具的形态"
---

::left::
<img src="/pictures/image_02.png" alt="思想与工具的矛盾" />

::right::
## 当思想的深度超越了工具的表达能力，创造便成为一种挣扎

- 工具与思想的关系：一个永恒的矛盾
- 历史规律：思想深度超越工具形态时的挣扎
- 当下困境：
  - 我们都是领域思想者
  - 复杂模型与洞见难以固化
  - 现有创造范式如"石锤"般笨拙

<!--
演讲者说: "我们一直在思考一个问题：工具与思想的关系。在人类历史中，当思想的深度，超越了当时工具所能承载的形态时，创造便成为一种充满阻力的挣扎。今天，我们每个人都是自己领域的思想者，我们脑中有无数复杂的模型和洞见。但将这些无形的思想，固化为有形的、可执行的工具时，我们发现，我们手中的'石锤'——也就是现有的创造范式——显得过于笨拙了。"
-->

---
layout: two-column
title: "回到构建的本质"
---

::left::
<img src="/pictures/image_03.png" alt="第一性原理信息图" />

::right::
<div class="space-y-6">
<div class="bg-gray-50 p-6 rounded-lg">
<h3 class="text-xl font-bold mb-4">核心公式</h3>
<div class="space-y-2 text-lg">
<div><strong>程序</strong> = 算法 + 数据结构</div>
<div class="text-blue-600"><strong>Agent</strong> = 流程 (Flow) + 上下文 (Context)</div>
</div>
</div>

<div class="bg-gray-50 p-6 rounded-lg">
<h3 class="text-xl font-bold mb-4">上下文四要素</h3>
<ul class="space-y-2 text-left">
<li>任务 (Task) - 做什么</li>
<li>工具 (Tools) - 用什么</li>
<li>参考文件 (Reference) - 参考什么</li>
<li>输出格式 (Format) - 得到什么</li>
</ul>
</div>
</div>

<!--
演讲者说: "为了理解我们手中的'石锤'，我们选择回到事物的起点。计算机科学给了我们一个非常质朴的公式：程序 = 算法 + 数据结构。这个洞见至今没有过时。在今天，我们谈论的Agent，本质上也是如此。所谓的'算法'，无非是定义一个'流程'，它由顺序、分支和循环这些基本动作构成。而所谓的'数据结构'，在大模型的语境下，就是为这个流程的每一步，提供精确的'上下文'。上下文回答了四个基本问题：做什么（任务），用什么（工具），参考什么（知识），以及最终要得到什么（格式）。所以，构建一个Agent的本质，并不是什么神秘的魔法，而是设计一个合理的流程，并为之准备好恰当的上下文。仅此而已。"
-->

---
layout: section-divider
title: ""
---

## Part 1: 回到起点

---
layout: two-column
title: "从创造「工具」到创造「可能性」"
---

::left::
<img src="/pictures/image_04.png" alt="可能性之树" />

::right::
## The Agent Builder

我们不旨在交付一个现成的工具。

**我们旨在构建一个能够生成工具的系统。**

这个系统，我们称之为 **The Agent Builder**。

<div class="p-6 bg-blue-50 rounded-lg mt-6">
理解了本质，我们的探索方向也变得清晰。我们发现，交付一个现成的、一次性的工具，价值是有限的。因为它只是一个"事物"。而一个能够持续生成、演化新工具的"系统"，才真正蕴含着"可能性"。
</div>

<!--
演讲者说: "理解了本质，我们的探索方向也变得清晰。我们发现，交付一个现成的、一次性的工具，价值是有限的。因为它只是一个'事物'。而一个能够持续生成、演化新工具的'系统'，才真正蕴含着'可能性'。我们把这个探索方向，命名为 The Agent Builder。它不是一个产品，而是我们构建的一个思想框架，一个持续生长的系统。"
-->

---
layout: two-column
title: "系统，而非工具"
---

::left::

<div class="flex items-center justify-center h-full">
<img src="/pictures/image_05.png" alt="系统与工具的对比" class="w-full max-w-md h-auto object-contain" />
</div>

::right::

<div class="flex flex-col justify-center h-full space-y-4">

<div class="grid grid-cols-2 gap-3">
<div class="text-center p-3 bg-red-50 rounded-lg border-l-4 border-red-500">
<h3 class="text-base font-bold mb-1 text-red-700">工具</h3>
<div class="text-red-600 font-semibold mb-2 text-xs">价值在使用中消耗</div>
<ul class="text-left space-y-0.5 text-gray-700 text-xs">
<li>• 一次性价值交付</li>
<li>• 无法内化个人知识</li>
<li>• 通用但不深入</li>
</ul>
</div>

<div class="text-center p-3 bg-green-50 rounded-lg border-l-4 border-green-500">
<h3 class="text-base font-bold mb-1 text-green-700">系统</h3>
<div class="text-green-600 font-semibold mb-2 text-xs">价值在构建中沉淀</div>
<ul class="text-left space-y-0.5 text-gray-700 text-xs">
<li>• 时间的复利效应</li>
<li>• 内化独特知识体系</li>
<li>• 成为思想的延伸</li>
</ul>
</div>
</div>

<div class="p-3 bg-blue-50 rounded-lg border border-blue-200">
<p class="text-center text-gray-700 font-medium text-xs leading-relaxed">
一个通用的工具无法内化你独特的知识体系，<br/>
而一个由你亲手构建的系统可以。
</p>
</div>

<div class="text-center">
<div class="inline-flex items-center space-x-2 px-4 py-2 bg-gray-100 rounded-full">
<span class="text-xs text-gray-600">构建 > 使用</span>
<span class="text-sm">🔄</span>
<span class="text-xs text-gray-600">沉淀 > 消耗</span>
</div>
</div>

</div>

<!--
演讲者说: "这里需要澄清一个重要的区别。工具，哪怕是再精美的工具，它的价值都在你使用它的那一刻被消耗。而系统，它的价值恰恰相反，在你构建、维护、迭代它的过程中，不断地累积和沉淀。我们称之为'时间的复利'。更重要的是，任何一个外部的、通用的工具，都无法真正理解和内化你个人独特的知识体系和思考方式。而一个由你亲手构建的系统可以。它最终会成为你思想的延伸。"
-->

---
layout: two-column
title: "为思想者，而非（传统）开发者"
---

::left::
<div class="flex items-center justify-center h-full">
<img src="/pictures/image_06.png" alt="思想的冰山" class="w-full max-w-sm h-auto object-contain" />
</div>

::right::
<div class="flex flex-col justify-center h-full space-y-6">

<div class="grid grid-cols-1 gap-3 mb-4">
<div class="p-4 bg-blue-50 rounded-lg border-l-4 border-blue-500">
<h3 class="text-lg font-bold mb-2 text-blue-700">水面之上</h3>
<p class="text-blue-600 font-semibold text-sm">通用需求</p>
<p class="text-gray-600 mt-1 text-xs">显性的、共通的需求</p>
</div>

<div class="p-4 bg-purple-50 rounded-lg border-l-4 border-purple-500">
<h3 class="text-lg font-bold mb-2 text-purple-700">水面之下</h3>
<p class="text-purple-600 font-semibold text-sm">个性化知识</p>
<p class="text-gray-600 mt-1 text-xs">各领域专家的隐性知识</p>
</div>
</div>

<div class="p-4 bg-gray-50 rounded-lg border border-gray-200">
<p class="text-gray-700 font-medium text-center leading-relaxed text-sm">
我们的关注点，是水面下那座巨大的冰山——<br/>
那些存在于各个领域专家头脑中的，<br/>
隐性、个性化的知识。
</p>
</div>

<div class="flex justify-center space-x-6 mt-3">
<span class="text-2xl">⚖️</span>
<span class="text-2xl">🩺</span>
<span class="text-2xl">📊</span>
<span class="text-2xl">🔬</span>
<span class="text-2xl">🎨</span>
</div>

</div>

<!--
演讲者说: "我们的另一个澄清是：我们服务的对象。我们服务的，不是传统意义上的开发者，而是那些在各个领域中进行着深度思考的'思想者'。如果把所有需求比作一座冰山，水面上的是少数共通的、显性的需求，而水面下，是巨大而沉默的、属于每个人的个性化知识和经验。现有的开发者工具，在服务水面之上的世界时做得非常出色。而我们，则希望探索如何服务水面之下的广阔世界。"
-->

---
layout: section-divider
title: ""
---

## Part 2: 我们的探索与实践

---
layout: two-column
title: "回到原点：GTPlanner"
---

::left::

<div class="flex flex-col justify-center h-full space-y-8">

<div class="text-center">
<h2 class="text-lg font-bold mb-3 text-gray-800">回顾：Agent = 流程 (Flow) + 上下文 (Context)</h2>
<p class="text-sm text-gray-600">GTPlanner 尝试回答3个基本问题</p>
</div>

<div class="grid grid-cols-1 gap-4">
<div class="text-center p-4 bg-blue-50 rounded-lg border-l-4 border-blue-500">
<div class="text-2xl mb-3">💬</div>
<h3 class="text-base font-bold mb-2 text-blue-700">1. 澄清需求</h3>
<p class="text-gray-600 text-sm">你的真实意图是什么？</p>
</div>

<div class="text-center p-4 bg-green-50 rounded-lg border-l-4 border-green-500">
<div class="text-2xl mb-3">🔧</div>
<h3 class="text-base font-bold mb-2 text-green-700">2. 梳理资源</h3>
<p class="text-gray-600 text-sm">实现它，需要哪些已知和未知？</p>
</div>

<div class="text-center p-4 bg-purple-50 rounded-lg border-l-4 border-purple-500">
<div class="text-2xl mb-3">📋</div>
<h3 class="text-base font-bold mb-2 text-purple-700">3. 生成规划</h3>
<p class="text-gray-600 text-sm">第一步的行动路径是什么？</p>
</div>
</div>

</div>

::right::

<div class="flex flex-col justify-center h-full space-y-6">

<div class="flex items-center justify-center">
<img src="/pictures/image_07.png" alt="GTPlanner的三件事" class="w-full max-w-xs h-auto object-contain" />
</div>

<div class="p-4 bg-gray-50 rounded-lg border border-gray-200">
<p class="text-center text-gray-700 italic leading-relaxed text-sm">
我们试图回归构建的本质，让创造的过程摆脱对复杂框架的依赖，<br/>
回到对"流程"的思考和对"上下文"的组织。
</p>
</div>

</div>

<!--
演讲者说: "明确了这些，再来看我们今天开源的主角：GTPlanner。它非常简单，它就是我们为了实践上述思考，所迈出的第一步。回到第一性原理，GTPlanner只尝试去回答三个基本问题：第一，通过对话，帮助你澄清自己最真实的意图是什么。第二，基于这个意图，帮你梳理实现它需要哪些已知的和未知的资源。第三，为你规划出第一步可行的行动路径。所以，如大家所见，GTPlanner所做的，就是回归构建的本质。我们希望创造的过程，能摆脱对特定、复杂框架的依赖，回到对'流程'的纯粹思考，和对'上下文'的精心组织。"
-->

---
layout: title-content
title: "理论的实践"
---

<div class="flex items-center justify-center h-full">
<div class="w-full max-w-5xl">
<div class="text-center mb-8">
<h2 class="text-2xl font-bold mb-4">眼见为实</h2>
<p class="text-lg text-gray-600">这些思考并非空想，我们已经将这套原则应用于具体场景</p>
<p class="text-lg text-gray-600">[视频placeholder]</p>
</div>
</div>
</div>

<!--
演讲者说: "这些思考并非空想。在内部，我们已经将这套原则应用于一些具体的场景。例如金融投研和医疗报告的解读。这些实践帮助我们验证、也修正了我们的想法。它们证明了，回归本质的规划，在真实世界中是可行且有价值的。"
-->

---
layout: section-divider
title: ""
---

## Part 3: 邀请与结语

---
layout: two-column
title: "为何开源"
---

::left::
<img src="/pictures/image_09.png" alt="未完成的地图" />

::right::
**我们绘制的，只是一张草图。**

真正的世界地图，需要所有探索者共同完成。

**开源，是我们承认自身局限性的体现，也是我们对集体智慧的信念。**

<!-- <div class="mt-8 p-6 bg-gray-50 rounded-lg">
我们深知，我们目前所做的，最多只是在一张巨大的、空白的地图上，标记出了几个我们认为可靠的出发点。而要绘制出完整的世界，需要所有方向的探索者共同努力。
</div> -->

<!--
演讲者说: "我们深知，我们目前所做的，最多只是在一张巨大的、空白的地图上，标记出了几个我们认为可靠的出发点。而要绘制出完整的世界，需要所有方向的探索者共同努力。因此，开源对我们来说是一个必然的选择。它首先代表了我们对自身局限性的承认，其次，也代表了我们对集体智慧最深刻的信念。"
-->

---
layout: title-content
title: "如何同行"
---

<div class="flex items-center justify-center h-full">
<div class="w-full max-w-5xl">
<div class="text-center mb-6">
<h2 class="text-lg font-bold mb-3">如果我们的思考能引起你的共鸣</h2>
<p class="text-sm text-gray-600">我们期待以三种方式同行</p>
</div>

<div class="grid grid-cols-3 gap-6">
<div class="text-center p-4 bg-white rounded-lg shadow-lg border border-gray-200 hover:shadow-xl transition-shadow">
<div class="text-3xl mb-3">🔧</div>
<h3 class="text-lg font-bold mb-2 text-blue-700">Tools</h3>
<p class="text-gray-600 mb-3 font-medium text-sm">打造更强的武器库</p>
<ul class="text-left space-y-1 text-gray-600 text-sm">
<li>• VS Code插件</li>
<li>• 生态集成</li>
<li>• 更多高质量工具集</li>
</ul>
</div>

<div class="text-center p-4 bg-white rounded-lg shadow-lg border border-gray-200 hover:shadow-xl transition-shadow">
<div class="text-3xl mb-3">🎯</div>
<h3 class="text-lg font-bold mb-2 text-green-700">Benchmarks</h3>
<p class="text-gray-600 mb-3 font-medium text-sm">定义"好"的标准</p>
<ul class="text-left space-y-1 text-gray-600 text-sm">
<li>• 评估数据集</li>
<li>• 评测方法</li>
<li>• 度量标准</li>
</ul>
</div>

<div class="text-center p-4 bg-white rounded-lg shadow-lg border border-gray-200 hover:shadow-xl transition-shadow">
<div class="text-3xl mb-3">🏆</div>
<h3 class="text-lg font-bold mb-2 text-purple-700">Showcases</h3>
<p class="text-gray-600 mb-3 font-medium text-sm">分享您的创造</p>
<ul class="text-left space-y-1 text-gray-600 text-sm">
<li>• 应用案例</li>
<li>• 实践教程</li>
<li>• 分享视频</li>
</ul>
</div>
</div>

</div>
</div>

<!--
演讲者说: "如果我们的思考能引起你的共鸣，我们期待以三种具体的方式同行。第一，是'打造更强的武器库'。帮助我们一起，为思想者提供更趁手的工具，让它更贴合真实的工作流。第二，是'定义"好"的标准'。帮助我们共同定义，到底什么才算是一个'好的规划'，建立起客观的评测基准与度量方法。第三，也是最重要的，是'分享您的创造'。将你的实践与洞见，通过案例、教程等方式沉淀下来，照亮我们都还未曾探索过的领域。我们相信，这些具体的贡献，将共同构成我们前行的道路。"
-->

---
layout: title-content
title: "关于我们"
---

<div class="flex items-center justify-center h-full">
<div class="text-center">
<div class="mb-8">
<h2 class="text-3xl font-bold mb-6">感易智能</h2>
<div class="w-32 h-32 mx-auto mb-6 bg-gray-200 rounded-full flex items-center justify-center">
<span class="text-4xl">🏢</span>
</div>
</div>

<div class="max-w-3xl mx-auto">
<blockquote class="text-xl text-gray-700 italic mb-8 leading-relaxed">
        "我们过去的经验，没有给我们所有答案，<br/>
        但教会了我们该问什么问题。"
</blockquote>

<div class="p-6 bg-gray-50 rounded-lg">
<p class="text-gray-600">
          我们是感易智能团队。过去数年在企业服务领域的实践，没有给我们所有问题的答案，但它确实教会了我们，应该去问哪些真正重要的问题。GTPlanner，就是我们对这些问题，提出的第一个解答。
</p>
</div>

<div class="mt-8 text-sm text-gray-500">
<p>源于实践，回归本质</p>
</div>
</div>
</div>
</div>

<!--
演讲者说: "关于我们自己，我想说的只有一句。我们是'感易智能'团队。过去数年在企业服务领域的实践，没有给我们所有问题的答案，但它确实教会了我们，应该去问哪些真正重要的问题。GTPlanner，就是我们对这些问题，提出的第一个解答。"
-->

---
layout: title-content
title: "期待交流"
---

<div class="flex items-center justify-center h-full">
<div class="text-center w-full max-w-5xl">
<h2 class="text-lg font-bold mb-6">加入我们的社区</h2>

<div class="grid grid-cols-4 gap-4 mb-6">
<div class="p-4 bg-gray-900 text-white rounded-lg shadow-lg hover:shadow-xl transition-shadow">
<div class="text-3xl mb-3">📱</div>
<h3 class="text-base font-bold mb-2">GitHub</h3>
<div class="w-16 h-16 mx-auto bg-white rounded flex items-center justify-center">
<span class="text-xs text-gray-500">QR Code</span>
</div>
</div>

<div class="p-4 bg-indigo-600 text-white rounded-lg shadow-lg hover:shadow-xl transition-shadow">
<div class="text-3xl mb-3">💬</div>
<h3 class="text-base font-bold mb-2">Discord</h3>
<div class="w-16 h-16 mx-auto bg-white rounded flex items-center justify-center">
<span class="text-xs text-gray-500">QR Code</span>
</div>
</div>

<div class="p-4 bg-green-600 text-white rounded-lg shadow-lg hover:shadow-xl transition-shadow">
<div class="text-3xl mb-3">📱</div>
<h3 class="text-base font-bold mb-2">微信群</h3>
<div class="w-16 h-16 mx-auto bg-white rounded flex items-center justify-center">
<span class="text-xs text-gray-500">QR Code</span>
</div>
</div>

<div class="p-4 bg-blue-600 text-white rounded-lg shadow-lg hover:shadow-xl transition-shadow">
<div class="text-3xl mb-3">🌐</div>
<h3 class="text-base font-bold mb-2">官网</h3>
<div class="w-16 h-16 mx-auto bg-white rounded flex items-center justify-center">
<span class="text-xs text-gray-500">QR Code</span>
</div>
</div>
</div>

<div class="mt-6">
<p class="text-lg font-semibold text-gray-800">谢谢大家</p>
</div>
</div>
</div>

<!--
演讲者说: (语气恢复平静，诚恳) "必须坦诚，我们今天所分享的一切，都处于一个非常早期的阶段。无论是GTPlanner还是它背后的The Agent Builder，都更像是一个哲学原型，而非一个成熟产品。关于未来，我们还有一些关于'本地优先'、'区块链'的初步构想，但那都还很遥远。所以，今天更像是一次思考的分享，一次真诚的邀请。真心感谢各位的耐心和包容。如果今天的分享，有哪些地方你认为存在谬误，或者遗漏了重要的视角，我们非常渴望能听到你的批评和见解。因为我们相信，建设性的批评，是比赞美更有价值的礼物。请随时加入我们的社区，我们期待在那里，与各位继续这场探讨。谢谢大家。"
-->
# 黃金墓室守衛．阿努比斯：製作死者之鑰

## Step 1: 查看任務與位置圖 @fullscreen

阿努比斯守在黃金墓室的出口。  
請使用黃金方塊製作「死者之鑰」。  
`■` 要放黃金方塊，`·` 不用放方塊。  

`高度 6｜· ■ ■ ■ ·`  
`高度 5｜■ · · · ■`  
`高度 4｜■ · · · ■`  
`高度 3｜· ■ ■ ■ ·`  
`高度 2｜■ ■ ■ ■ ■`  
`高度 1｜· · ■ · ·`  
`高度 0｜· · ■ · ·`  
`左右位置｜-2 -1 0 1 2`  

所有方塊都放在前後位置 `3`。  
完成圖案後，才能前往下一道關卡。  
打開聊天欄，輸入 `ankh`。  
這個指令會叫程式開始工作。

```blocks
player.onChat("ankh", function () {
})
```

## Step 2: 放出最上方的金色橫條

加入「填滿方塊」積木。  
`GOLD_BLOCK` 代表黃金方塊。  
高度都是 `6`，會放在第 6 格高的地方。  
從左右位置 `-1` 放到 `1`，會出現 3 格寬的橫條。  
`Replace` 會把這個範圍換成黃金方塊。

```blocks
player.onChat("ankh", function () {
    blocks.fill(
    GOLD_BLOCK,
    pos(-1, 6, 3),
    pos(1, 6, 3),
    FillOperation.Replace
    )
})
```

## Step 3: 接上左邊的短線

再加入一個「填滿方塊」積木。  
左右位置都是 `-2`，表示放在左邊。  
高度從 `4` 到 `5`，表示要放 2 格高。  
畫面上會出現左邊的金色短線。  
對照位置圖，看看左邊是不是有 2 格黃金方塊。

```blocks
player.onChat("ankh", function () {
    blocks.fill(
    GOLD_BLOCK,
    pos(-1, 6, 3),
    pos(1, 6, 3),
    FillOperation.Replace
    )
    blocks.fill(
    GOLD_BLOCK,
    pos(-2, 4, 3),
    pos(-2, 5, 3),
    FillOperation.Replace
    )
})
```

## Step 4: 接上右邊的短線

加入右邊的金色短線。  
左右位置都是 `2`，表示放在右邊。  
高度從 `4` 到 `5`，也會放出 2 格。  
畫面上的左右兩邊會一樣高。  
對照位置圖，看看兩邊是不是排得整整齊齊。

```blocks
player.onChat("ankh", function () {
    blocks.fill(
    GOLD_BLOCK,
    pos(-1, 6, 3),
    pos(1, 6, 3),
    FillOperation.Replace
    )
    blocks.fill(
    GOLD_BLOCK,
    pos(-2, 4, 3),
    pos(-2, 5, 3),
    FillOperation.Replace
    )
    blocks.fill(
    GOLD_BLOCK,
    pos(2, 4, 3),
    pos(2, 5, 3),
    FillOperation.Replace
    )
})
```

## Step 5: 封住中間的缺口

在第 `3` 格高的位置放一條橫線。  
橫線從左右位置 `-1` 排到 `1`。  
這個範圍會放出 3 個黃金方塊。  
畫面上的金色框會連接起來。  
對照位置圖，看看鑰匙上方的形狀是不是完成了。

```blocks
player.onChat("ankh", function () {
    blocks.fill(
    GOLD_BLOCK,
    pos(-1, 6, 3),
    pos(1, 6, 3),
    FillOperation.Replace
    )
    blocks.fill(
    GOLD_BLOCK,
    pos(-2, 4, 3),
    pos(-2, 5, 3),
    FillOperation.Replace
    )
    blocks.fill(
    GOLD_BLOCK,
    pos(2, 4, 3),
    pos(2, 5, 3),
    FillOperation.Replace
    )
    blocks.fill(
    GOLD_BLOCK,
    pos(-1, 3, 3),
    pos(1, 3, 3),
    FillOperation.Replace
    )
})
```

## Step 6: 放上寬寬的握把

在第 `2` 格高的位置加入一條橫線。  
橫線從左右位置 `-2` 排到 `2`。  
畫面上會出現 5 格寬的金色橫條。  
這條橫線像死者之鑰寬寬的握把。  
對照位置圖，確認這是圖案最寬的一排。

```blocks
player.onChat("ankh", function () {
    blocks.fill(
    GOLD_BLOCK,
    pos(-1, 6, 3),
    pos(1, 6, 3),
    FillOperation.Replace
    )
    blocks.fill(
    GOLD_BLOCK,
    pos(-2, 4, 3),
    pos(-2, 5, 3),
    FillOperation.Replace
    )
    blocks.fill(
    GOLD_BLOCK,
    pos(2, 4, 3),
    pos(2, 5, 3),
    FillOperation.Replace
    )
    blocks.fill(
    GOLD_BLOCK,
    pos(-1, 3, 3),
    pos(1, 3, 3),
    FillOperation.Replace
    )
    blocks.fill(
    GOLD_BLOCK,
    pos(-2, 2, 3),
    pos(2, 2, 3),
    FillOperation.Replace
    )
})
```

## Step 7: 完成死者之鑰

在正中央放上最後一條直線。  
左右位置是 `0`，表示放在正中央。  
高度從 `0` 到 `1`，會放出 2 格高的金色直線。  
打開聊天欄並輸入 `ankh`。  
完整的死者之鑰就會出現在黃金墓室中。

```blocks
player.onChat("ankh", function () {
    blocks.fill(
    GOLD_BLOCK,
    pos(-1, 6, 3),
    pos(1, 6, 3),
    FillOperation.Replace
    )
    blocks.fill(
    GOLD_BLOCK,
    pos(-2, 4, 3),
    pos(-2, 5, 3),
    FillOperation.Replace
    )
    blocks.fill(
    GOLD_BLOCK,
    pos(2, 4, 3),
    pos(2, 5, 3),
    FillOperation.Replace
    )
    blocks.fill(
    GOLD_BLOCK,
    pos(-1, 3, 3),
    pos(1, 3, 3),
    FillOperation.Replace
    )
    blocks.fill(
    GOLD_BLOCK,
    pos(-2, 2, 3),
    pos(2, 2, 3),
    FillOperation.Replace
    )
    blocks.fill(
    GOLD_BLOCK,
    pos(0, 0, 3),
    pos(0, 1, 3),
    FillOperation.Replace
    )
})
```


> Open this page at [https://junming0106.github.io/minecraft_001/](https://junming0106.github.io/minecraft_001/)

## Use as Extension

This repository can be added as an **extension** in MakeCode.

* open [https://minecraft.makecode.com/](https://minecraft.makecode.com/)
* click on **New Project**
* click on **Extensions** under the gearwheel menu
* search for **https://github.com/junming0106/minecraft_001** and import

## Edit this project

To edit this repository in MakeCode.

* open [https://minecraft.makecode.com/](https://minecraft.makecode.com/)
* click on **Import** then click on **Import URL**
* paste **https://github.com/junming0106/minecraft_001** and click import

#### Metadata (used for search, rendering)

* for PXT/minecraft
<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>

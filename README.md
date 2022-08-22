# 紹介
今まで私が自分で勉強した物です。一部は自分で変えてみました。その変えた物を紹介します。

目次:
* [Calulator](#Calulator)
* [portfolio](#portfolio)
---
## Calulator
計算器は[こちら](https://kanhi.tistory.com/2)を参考にしました。元々は二乗を求める方法はなかったが、自分で追加してみました。

元の計算器:

![2](https://user-images.githubusercontent.com/109051985/183335086-b0491d4f-bb78-43c6-beba-556dc9913fb0.PNG)


修正本:

`html`にこのコードを追加
```js
<button data-type="operator" class ="squared">^</button>
```
`css`に追加及び修正
```js
.squared {
    background: orange;
}   //追加

button:nth-child(4n+3), button:last-child  {    //child(4n+2) -> child(4n+3)
    background-color: orange;
}
```
![1](https://user-images.githubusercontent.com/109051985/183335171-3fc916aa-ceed-4d92-a49e-487d4fbd7842.PNG)

`js`に追加及び修正
```js
compute() {
        if (this.operatorCheck) return
        this.displayContent = eval(this.displayContent
            .replace('\u00D7', '*')
            .replace('\u00F7', '/')
            .replace('\u005E', '**')    //追加
        )
        this.equalsCheck = true
    }
```

hello world

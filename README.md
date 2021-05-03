# React

## section6 CSS-stylingについて学習

### 75 クラス名を動的に付け外し

<details><summary>stateに応じてクラス名を付けるには？</summary>

```jsx
<div className={`form-control ${!isValid ? 'invalid` : ''}`}>

```
</details>

---

### 74 インラインスタイル

<details><Summary>機能改善：　Add Goalボタン</Summary>

> ⚠️ 未入力でも追加されてしまう問題

 |-> 追加できないようにする

 |-> 追加できないことをフィードバック -> タイトル赤文字入力欄背景色付く

 |-> 文字入力し始めたら、フィードバック解除

> CSSインライン書き方注意点

```jsx
<label style={{ backgroundColor: 'red' }}>
```

キー：　CSSプロパティとは違う書き方

バリュー：　文字列

</details>

---
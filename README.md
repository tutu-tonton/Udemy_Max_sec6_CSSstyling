# React

## section6 CSS-stylingについて学習

### 74 インラインスタイル

<details><Summary>機能改善：　Add Goalボタン</Summary>

 ⚠️ 未入力でも追加されてしまう問題

 |-> 追加できないようにする

 |-> 追加できないことをフィードバック -> タイトル赤文字入力欄背景色付く

 |-> 文字入力し始めたら、フィードバック解除

</details>

<details><summary>CSSインライン書き方注意点</summary>

```jsx
<label style={{ backgroundColor: 'red' }}>
```

キー：　CSSプロパティとは違う書き方

バリュー：　文字列

</details>

---

### 75 クラス名を動的に付け外し

<details><summary>stateに応じてクラス名を付けるには？</summary>

```jsx
<div className={`form-control ${!isValid ? 'invalid` : ''}`}>

```

</details>

---

### 76 styled-components

ボタンのスタイルをstyled-componentsを使用

<details><summary>書き方</summary>

```javascript
const Button = styled.button`
  font: ,
  &:hover { }
`;
```

</details>

---

### 77 styled-componentsにpropsを渡して、動的にスタイリング

<details><summary>styledComponentsにprops渡す</summary>

```react
const FormControl = styled.div`
  & input {
    background: ${(props) => (props.invalid ? '' : '' )};
  }
`;

```

```jsx

<FormControl invalid={!isValid}></FormControl>

```

</details>

---

### 78 mediaQuery書き方

---

### 79 CSS module使い方

<details><summary>ファイル名どう書く？</summary>

`Button.module.css`

</details>

<details><summary>インポートの仕方</summary>

`import styles from './xxx'`

</details>

<details><summary>JSX書き方</summary>

```javascript

<button className={styles.button}></button>

```

</details>

---

### 80 CSS moduleの動的スタイル適用

```javascript

<div className={`${styles['form-control']} ${!isValid && styles.invalid}`}>


```

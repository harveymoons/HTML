# HTML
###### (HyperText Markup Language) self-study
---
###### autocomplete off / `input` tag
```html
<input autocomplete="off" type="text" name="address"/>
```
###### form submit
```html
<a class="btnLogin btnBlue" onclick="this.form.submit()">Log-In</a>
```
[Ref.] https://stackoverflow.com/questions/7340300/a-tag-as-a-submit-button/7340340  
  
###### form reset
```html
<form>
  <div class="conDiv9"><input type="text" class="input03 wdt140px" placeholder="field01"></div>
  <div class="conDiv9"><input type="text" class="input03 wdt140px" placeholder="field02"></div>
  <div class="conDiv9"><input type="text" class="input03 wdt140px" placeholder="field03"></div>
  <a href="#" onclick="this.parentElement.reset()"><img src="/static/images/btn_delete.gif"></a>
</form>
```
###### data attribute
```html
<td><div type="text" th:text="${row.COL_TITLE}" data-columns="COL_NAME"></div></td>
<td><input type="text" class="input03 wdt230px" data-columns="COND_VAL"/></td>
<td><input type="text" class="input03 wdt230px" data-columns="VAL_MAX" th:name="${row.COL_NAME}" disabled/></td>
```
```js
function getDataColumns() {
	
	const dataArr = [];
	
	document.querySelectorAll("tbody input[type=checkbox]:checked").forEach(item => {
		
		const row = item.parentElement.parentElement;
		
		dataArr.push({
			RULE_NAME: row.querySelector("[data-columns='RULE_NAME']").value,
			COL_NAME : row.querySelector("[data-columns='COL_NAME']").textContent,
			COND_TYPE: row.querySelector("[data-columns='COND_TYPE']").value,
			COND_VAL : row.querySelector("[data-columns='COND_VAL']").value,
			VAL_MAX  : row.querySelector("[data-columns='VAL_MAX']").value,
		});
	});
	
}
```
[Ref.] [data attribute MDN](https://developer.mozilla.org/ko/docs/Learn/HTML/Howto/%EB%8D%B0%EC%9D%B4%ED%84%B0_%EC%86%8D%EC%84%B1_%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0)  
###### how to click event on disabled select tag
```js
<span onclick="alert('mission success!')">
    <select disabled></select>
</span>
```
  
###### href="#id-name"
```html
<li><a aria-controls="email" aria-expanded="true" data-toggle="tab" href="#email">E-mail</a></li>

<div class="chart tab-pane" id="email" style="position: relative; min-height: 300px;">
    <div th:include="html/member/inner/email/list"></div>
</div>
```

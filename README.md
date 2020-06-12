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

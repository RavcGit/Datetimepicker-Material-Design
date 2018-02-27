# Datetimepicker-Material-Design
Utilizado como base o Datetimepicker da [XDSOFT](https://xdsoft.net/jqplugins/datetimepicker/).

## Requirimentos
Atualmente esse plugin tem como requirimento para funcionar os seguintes componentes:
- [Bootstrap 4.0+](http://getbootstrap.com/), layout de estrutura foi totalmente usada em cima do Bootstrap 4.
  - CSS:
  ```html
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.3/css/bootstrap.min.css" integrity="sha384-Zug+QiDoJOrZ5t4lssLdxGhVrurbmBWopoEl+M6BdEfwnCJZtKxi1KgxUyJq13dy" crossorigin="anonymous">
  ```
  - Javascript:
  ```html
  <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
  <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.3/js/bootstrap.min.js" integrity="sha384-a5N7Y/aK3qNeh15eJKGWxsqtnX/wWdSZSKp+81YjTmS15nvnvxKHuzaWwXHDli+4" crossorigin="anonymous"></script>
  ```
- [jQuery 3.3+](https://jquery.com/), funções de javascript foram implementadas com o jquery.
  - Javascript:
  ```html
  <script src="https://code.jquery.com/jquery-3.2.1.min.js" integrity="sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=" crossorigin="anonymous"></script>
  ```
## Começando a utilizar

No HTML podemos implementar os seguintes exemplos que iremos testar:
```html
<!-- Input somente com visualização da Data -->
<div class="input-group mb-3">
  <input id="datepicker" type="text" class="form-control" placeholder="Datetime" aria-label="Datetime" aria-describedby="basic-addon1">
</div>

<!-- Input somente com visualização da Hora -->
<div class="input-group mb-3">
  <input id="timepicker" type="text" class="form-control" placeholder="Datetime" aria-label="Datetime" aria-describedby="basic-addon1">
</div>

<!-- Input somente com visualização da Data inline -->
<div class="input-group mb-3">
  <input id="datepicker-inline" type="text" class="form-control" placeholder="Datetime" aria-label="Datetime" aria-describedby="basic-addon1">
</div>

<!-- Input somente com visualização da Hora inline -->
<div class="input-group mb-3">
  <input id="timepicker-inline" type="text" class="form-control" placeholder="Datetime" aria-label="Datetime" aria-describedby="basic-addon1">
</div>

<!-- Input com visualização da Data/hora -->
<div class="input-group mb-3">
  <input id="datetimepicker" type="text" class="form-control" placeholder="Datetime" aria-label="Datetime" aria-describedby="basic-addon1">
</div>
```
E para inicializar o plugin utilizamos o seguinte Jquery:
```js
jQuery('#datepicker').datetimepicker({
  timepicker:false
});
jQuery('#timepicker').datetimepicker({
  datepicker:false
});
jQuery('#datepicker-inline').datetimepicker({
  inline:true,
  timepicker:false
});
jQuery('#timepicker-inline').datetimepicker({
  inline:true,
  datepicker:false
});
jQuery('#datetimepicker').datetimepicker({
  timepicker:true,
  datepicker:true
});
```


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
  timepicker:false, // Oculta o Timepicker
  format: 'd/m/Y' // Formato da data do input, usando o 'd/m/Y' ele não irá mostrar a hroa atual junto.
});
jQuery('#timepicker').datetimepicker({
  datepicker:false, // Oculta o Datepicker
  format: 'H:i', // Colocando uma formatação no input você remove alguns bugs onde ele pega os minutos aleatórios. 
  allowTimes:['07:00','07:30','08:00','08:30','09:00','09:30','19:00','20:00'] // Intervalos de tempo que irão aparecer no timepicker
});
jQuery('#datepicker-inline').datetimepicker({
  inline:true, // Inline obriga o picker ficar ativo e oculta o input.
  timepicker:false,
  format: 'd/m/Y'
});
jQuery('#timepicker-inline').datetimepicker({
  inline:true,
  datepicker:false,
  format: 'H:i',
  allowTimes:['07:00','07:30','08:00','08:30','09:00','09:30','19:00','20:00']
});
jQuery('#datetimepicker').datetimepicker({
  timepicker:true,
  datepicker:true,
  format: 'd/m/Y H:i' // A função 'format' é usada para o input todo, se quiser formatar somente a hora terá que usar o 'formatTime' e para formatar somente a data terá que usar o 'formatDate'.
});
```


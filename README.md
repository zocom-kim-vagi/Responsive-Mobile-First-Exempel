# Responsive-Mobile-First-Exempel


Här kommer exempel hur du bygger Mobile First Responsive

<!DOCTYPE html>
<html>
<head>
<style>  

/* Här är det mobilens style som kommer först */

.grid-container {
  display: grid;
  grid-template-columns: auto auto auto auto;

  background-color: #aaaaaa;
  padding: 10px;
}
.grid-container > div {
  background-color: rgba(255, 255, 255, 0.8);
  border: 1px solid black;
  text-align: center;
  font-size: 30px;
  grid-column:1/4;
}
div .aside{
display:none;
}

/* Här görs lite ändringar om det är en desktop */
  
@media only screen and (min-width: 600px) {
  div .split{
      grid-column:1/3;
      grid-row:4/5;

    }
  div .split2{
      grid-column:3/4;
      grid-row:4/5;
    }
  div .aside{
      display:block;
      grid-row:1/6;
      grid-column:4/5;
  }
} 
  
</style>
</head>
<body>

<h2>Responsiv Sida, Mobile first</h2>

<p></p>

<div class="grid-container">
  <div>Header</div>
  <div class="nav"> Här kommer navigeringslänkar </div>
  <div class="aside">aside</div>  
  <div><h1>Stora nyheten</h1></div>
  <div class="split"> <h3>News</h3></div>
  <div class="split2"><h3>News 2</h3></div>
  <div>footer</div>

</div>
</body>
</html>

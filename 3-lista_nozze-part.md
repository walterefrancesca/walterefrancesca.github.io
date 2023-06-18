---
layout: partecipazione
title: Lista Nozze
description: Aiutaci a creare ricordi indimenticabili
image: assets/images/lista-nozze.png
nav-menu: false
show_tile: false
---


<div id="scoped-content">

<style>
ul {
  list-style-type: none;
}

li {
  /* display: inline-block; */
}

input[type=radio][id^="myCheckbox"] {
  display: none;
}

label {
  /* border: 1px solid #fff; */
  padding: 10px 0px;
  display: block;
  position: relative;
  margin: 10px;
  cursor: pointer;
}

label:before {
  background-color: white;
  color: white;
  content: " ";
  display: block;
  border-radius: 50%;
  border: 1px solid grey;
  position: absolute;
  top: -5px;
  left: -5px;
  width: 25px;
  height: 25px;
  text-align: center;
  line-height: 28px;
  transition-duration: 0.4s;
  transform: scale(0);
}

label img {
  height: 300px;
  width: 500px;
  transition-duration: 0.2s;
  transform-origin: 50% 50%;
  border-radius: 2%;
  object-fit: cover;
}

:checked + label {
  /* border-color: #ddd; */
}

:checked + label:before {
  content: "✓";
  background-color: grey;
  transform: scale(1);
}

:checked + label img {
  transform: scale(0.9);
  box-shadow: 0 0 5px #333;
  z-index: -1;
}

ul, li, label {
    padding-left: 0.0em;
    margin: 0em;
}
</style>

<ul>
  <li>
    <input type="radio" id="myCheckbox1" name="regalo" value="viaggio"/>
    <label for="myCheckbox1">
    <h4>Aiutateci ad organizzare un viaggio indimenticabile</h4>
    <img src="assets/images/viaggio_di_nozze.jpeg" /></label>
  </li>
  <li>


    <input type="radio" id="myCheckbox2" name="regalo" value="casa"/>
    <label for="myCheckbox2">
    <h4>Aiutateci a costruire una casa da sogno</h4>
    <img src="assets/images/Castello-di-Neuschwastein.jpg" /></label>
  </li>
  <li>

    <input type="radio" id="myCheckbox3" name="regalo" value="idea"/>
    <label for="myCheckbox3">
    <h4>Liberate la vostra creatività, e proponete a cosa destinare il vostro regalo</h4>
    <img src="assets/images/idea_regalo.jpg" /></label>
  </li>
</ul>


<script src="https://www.google.com/recaptcha/api.js"></script>
<script>
function myFunction(){
document.getElementById("add_message").innerHTML =
'<div class="table-wrapper"> <table> <thead> <tr> <th>Name</th> <th>Description</th> </tr> </thead> <tbody> <tr> <td>BIC/SWIFT</td> <td>UNCRITM140V</td> </tr> <tr> <td>IBAN</td> <td>IT93J0200841301000010660301</td> </tr> <tr> <td>Intestato a</td> <td>Vito Walter Anelli</td> </tr> <tr> <td>Causale</td> <td id="bnk_text">Regalo per il Matrimonio di Walter e Francesca</td> </tr> </tbody> </table> </div>';
};
</script>


<script>
  if (document.querySelector('input[name="regalo"]')) {
  document.querySelectorAll('input[name="regalo"]').forEach((elem) => {
    elem.addEventListener("click", giftMessage);
  });
  }

  function giftMessage() {
    let choice = document.querySelector('input[name="regalo"]:checked').value;
    if (!choice) {
      return;
    }
    myFunction();
    if (choice === 'viaggio') {
      document.getElementById("bnk_text").textContent = 'Regalo per il Matrimonio di Walter e Francesca - Contributo Viaggio di Nozze';
    } else if (choice === 'casa') {
      document.getElementById("bnk_text").textContent = 'Regalo per il Matrimonio di Walter e Francesca - Contributo per la Casa';
    } else if (choice === 'idea') {
      document.getElementById("bnk_text").textContent = 'Regalo per il Matrimonio di Walter e Francesca - Contributo per ...';
    } else {
      document.getElementById("bnk_text").textContent = 'Regalo per il Matrimonio di Walter e Francesca';
    }
  }
</script>



<button onclick="myFunction()"
        class="g-recaptcha"
        data-sitekey="6LfukwIlAAAAAHEhwjp6bn-Brei5HsdjQvweoISt"
        data-callback='onSubmit'
        data-action='submit'
        style="margin-bottom:2em;">Mostra i dettagli bancari</button>
<div id='add_message'></div>

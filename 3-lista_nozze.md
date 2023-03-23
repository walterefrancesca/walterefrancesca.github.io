---
layout: post
title: Lista Nozze
description: Aiutaci a creare ricordi indimenticabili
image: assets/images/lista-nozze.png
nav-menu: true
---


<script src="https://www.google.com/recaptcha/api.js"></script>
<script>
function myFunction(){
document.getElementById("add_message").innerHTML =
'<div class="table-wrapper"> <table> <thead> <tr> <th>Name</th> <th>Description</th> </tr> </thead> <tbody> <tr> <td>BIC/SWIFT</td> <td>UNCRITM140V</td> </tr> <tr> <td>IBAN</td> <td>IT93J0200841301000010660301</td> </tr> <tr> <td>Intestato a</td> <td>Vito Walter Anelli</td> </tr> <tr> <td>Causale</td> <td>Regalo per il Matrimonio di Walter e Francesca</td> </tr> </tbody> </table> </div>';
};
</script>

<button onclick="myFunction()"
        class="g-recaptcha"
        data-sitekey="6LfukwIlAAAAAHEhwjp6bn-Brei5HsdjQvweoISt"
        data-callback='onSubmit'
        data-action='submit'>Mostra i dettagli del conto corrente</button>
<div id='add_message'></div>

<!--
<div class="table-wrapper">
	<table>
		<thead>
			<tr>
				<th>Name</th>
				<th>Description</th>
			</tr>
		</thead>
		<tbody>
			<tr>
				<td>BIC</td>
				<td>XXYY</td>
			</tr>
			<tr>
				<td>SWIFT</td>
				<td>SWC-SERT</td>
			</tr>
			<tr>
				<td>IBAN</td>
				<td>000 000 000 000 000 000 </td>
			</tr>
			<tr>
				<td>Intestato a</td>
				<td>Vito Walter Anelli</td>
			</tr>
			<tr>
				<td>Causale</td>
				<td>Matrimonio Walter e Francesca</td>
			</tr>
		</tbody>
	</table>
</div>
-->

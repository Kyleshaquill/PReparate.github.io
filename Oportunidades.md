---
layout: default
title: Oportunidades
---

<section class="text-center text-light py-5"
style="background: linear-gradient(135deg,#2b6cb0,#0a2540);">

<div class="container py-5">

<h1 class="display-3 fw-bold">
Oportunidades en STEM
</h1>

<p class="lead">
Programas, internships y oportunidades para estudiantes de Puerto Rico.
</p>

</div>
</section>


<section class="py-5">

<div class="container">

<!-- SEARCH BAR -->

<div class="row mb-4">

<div class="col-md-6 mx-auto">

<input
type="text"
id="searchInput"
class="form-control"
placeholder="Buscar oportunidad..."
onkeyup="searchTable()">

</div>

</div>


<!-- TABLE -->

<table class="table table-striped" id="opportunitiesTable">

<thead>

<tr>
<th>Programa</th>
<th>Tipo de Oportunidad</th>
<th>Área</th>
<th> País</th>
<th>Link</th>
</tr>

</thead>

<tbody>

<tr>
<td>JPL Internship</td>
<td>Internado</td>
<td>Ciencias Planetarias</td>
<td>USA</td>
<td>
<a href="https://www.jpl.nasa.gov/edu/internships/" target="_blank">
Ver
</a>
</td>
</tr>

<tr>
<td>NSF REU Programs</td>
<td>Internado / Grant</td>
<td>Investigacion / Multiple Areas</td>
<td>USA / Internacional</td>
<td>
<a href="https://www.nsf.gov/funding/initiatives/reu/search" target="_blank">
Ver
</a>
</td>
</tr>

<tr>
<td>Google Summer of Code</td>
<td>Programa de desarrollo de software</td>
<td>Computación / Software</td>
<td>USA (En linea)</td>
<td>
<a href="https://summerofcode.withgoogle.com/" target="_blank">
Ver
</a>
</td>
</tr>

</tbody>

</table>

</div>

</section>


<script>

function searchTable() {

let input = document.getElementById("searchInput");
let filter = input.value.toLowerCase();
let table = document.getElementById("opportunitiesTable");
let tr = table.getElementsByTagName("tr");

for (let i = 1; i < tr.length; i++) {

let rowText = tr[i].textContent.toLowerCase();

if (rowText.indexOf(filter) > -1) {
tr[i].style.display = "";
} else {
tr[i].style.display = "none";
}

}

}

</script>

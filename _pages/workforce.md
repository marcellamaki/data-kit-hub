---
title: Workforce
layout: base
permalink: /workforce/
hero:
  text: Workforce Challenges
  subtext: Datasets on workers, businesses, jobs, credentials, and more, recommended by government experts for solving key workforce challenges.
  tag: Theme
  image: /assets/images/hero/workforce.png
pageScript: |
  $(function searchDatasets() {
    console.log("i'm searching!")
    var input, filter, table, tr, td, i, txtValue;
    input = document.getElementById("myInput");
    console.log(input)
    filter = input.value.toUpperCase();
    table = document.getElementById("topics");
    tr = table.getElementsByClassName("datasets__card");

    for (i = 0; i < tr.length; i++) {
      td = tr[i].getElementsByClassName("datasets__card-title")[0];
      if (td) {
        txtValue = td.textContent || td.innerText;
        if (txtValue.toUpperCase().indexOf(filter) > -1) {
          tr[i].style.display = "";
        } else {
          tr[i].style.display = "none";
        }
      }
    }

    for (i = 0; i < tr.length; i++) {
      td = tr[i].getElementsByClassName("datasets__card-subtitle")[0];
      if (td) {
        txtValue = td.textContent || td.innerText;
        if (txtValue.toUpperCase().indexOf(filter) > -1) {
          tr[i].style.display = "";
        } else {
          tr[i].style.display = "none";
        }
      }
    }

    for (i = 0; i < tr.length; i++) {
      td = tr[i].getElementsByClassName("datasets__card-description")[0];
      if (td) {
        txtValue = td.textContent || td.innerText;
        if (txtValue.toUpperCase().indexOf(filter) > -1) {
          tr[i].style.display = "";
        } else {
          tr[i].style.display = "none";
        }
      }
    }

  }
  })
---

{% include hero.html %}
{% include datasets/workforce.html %}

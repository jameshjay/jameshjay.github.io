---
layout: default
title: Notion - Calculate days remaining
nav_order: 
has_children:  
parent: Productivity Software
grand_parent: Miscellaneous
description: "Notion - calculate the remaining number of days"
permalink: /calculate-days-remaining/
image: 
author: James H. Jay
---

### Productivity Software
{: .no_toc }

Productivity
{: .label .label-red }

<h1><center> Notion | Calculate days remaining</center></h1> 

---

<div class="videoWrapper">
    <iframe width="672" height="378" src="https://www.youtube.com/embed/6EyeFAAHdhM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

## Formula: <br>
Try this formula instead! (It will add: # days remaining & # of days overdue): <br>
<blockquote><code>empty(prop("Due Date")) ? "" : concat(format(abs(dateBetween(prop("Due Date"), now(), "days")) + 1), format((dateBetween(prop("Due Date"), now(), "days") + 1 <= 0) ? " days overdue" : ((dateBetween(prop("Due Date"), now(), "days") + 1 > 0) ? " days remaining" : "")))
</code></blockquote>

<br>

---

<h1><center> Latest Productivity Software: </center></h1>
<div class="row">
    <div class="column_grid">
        <a href="/calculate-days-remaining">
            <img border="0" alt="img" src="/assets/images/cards/box5.png" width="230" height="450">
        </a>
    </div>
    <div class="column_grid">
        <a href="/convert-into-inline">
            <img border="0" alt="img" src="/assets/images/cards/box6.png" width="230" height="450">
        </a>
    </div>
    <div class="column_grid">
        <a href="/favorite-features">
            <img border="0" alt="img" src="/assets/images/cards/box7.png" width="230" height="450">
        </a>
    </div>      
</div>
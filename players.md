---
layout: page
title: Players
---

Here is the current state of play in our ongoing game of Nomic:

<table>
<thead>
 <tr>
  <th>Name</th>
  <th>Group</th>
  <th>Points</th>
  <th>Penalties</th>
  <th>Balance</th>
 </tr>
</thead>
<tbody>
{% assign toplist = site.data.players | sort: "points" | reverse %}
{% for player in toplist %}
 <tr>
  <td>{{ player.name }}</td>
  <td>{{ player.group }}</td>
  <td>{{ player.points }}</td>
  <td>{{ player.penalties }}</td>
  <td>{{ player.points - player.penalties }}</td>
 </tr>
{% endfor %}
</tbody>
</table>

---
title: People
permalink: /people/
---

{% assign people_sorted = site.people | sort: 'joined' %}
{% assign role_array = "pi|postdoc|gradstudent|researchstaff|visiting|others|alumni" | split: "|" %}

{% for role in role_array %}

{% assign people_in_role = people_sorted | where: 'position', role %}

<!-- Skip section if there's nobody -->
{% if people_in_role.size == 0 %}
  {% continue %}
{% endif %}

<div class="pos_header">
{% if role == 'postdoc' %}
<h3>Postdoctoral Fellows</h3>
 {% elsif role == 'pi' %}
<h3>Principal Investigator</h3>
 {% elsif role == 'gradstudent' %}
<h3>Students</h3>
 {% elsif role == 'researchstaff' %}
<h3>Research Staff</h3>
 {% elsif role == 'visiting' %}
<h3>Visiting Scholars</h3>
 {% elsif role == 'others' %}
<h3>Student Collaborators</h3>
 {% elsif role == 'alumni' %}
<h3>Alumni</h3>
{% endif %}
</div>

{% if role != 'alumni' %}
<div class="content list people">
  {% for profile in people_sorted %}
    {% if profile.position contains role %}
      <div class="list-item-people">
        <p class="list-post-title">
          {% if profile.avatar %}
            <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="{{site.baseurl}}/images/people/{{profile.avatar}}"></a>
          {% else %}
            <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="http://evansheline.com/wp-content/uploads/2011/02/facebook-Storm-Trooper.jpg"></a>
          {% endif %} 
          <a class="name" href="{{ site.baseurl }}{{ profile.url }}" style="font-weight: bold;">{{ profile.name }}</a><br>
          <!-- <a class="scholar" href="https://scholar.google.com/citations?user={{ profile.scholar }}&hl="  style="font-size: smaller;">Google Scholar</a> -->
        </p>
      </div>    
    {% endif %}
  {% endfor %}
</div>
<hr>

{% else %}

<h3>Alumni</h3>
<br>

| Who are they | When were they here | Where they went |
| :------------- |:-------------| :-----------|
| [Tianrui Guan](https://tianruiguan.phd/) | M.S. (2019-2020) | Ph.D., University of Maryland, College Park |


{% endif %}
{% endfor %}

### Active Collaborators

Here are some cool people in fields that interest us. **note:** This list is in no way complete. We have a lot of collaborators -- if you've collaborated with us and want a link here, let us know!

**IIIT Hyderabad:**
- [Ravi Kiran Sarvadevabhatla - Dept of Computer Science](https://ravika.github.io/)

**University of Maryland, College Park:**
- [Dinesh Manocha - Dept of Computer Science](https://www.cs.umd.edu/~dm/)

**University of Texas at Austin:**
- [Joydeep Biswas - Dept of Computer Science](https://www.joydeepb.com/)
- [Peter Stone - Dept of Computer Science](https://www.cs.utexas.edu/~pstone/)
- [Vrushabh Zinage - Dept of Aerospace Engineering](https://vrushabh27.github.io/vrushabh_zinage/)
- [Efstathios Bakolas - Dept of Aerospace Engineering](https://sites.utexas.edu/ebakolas/)

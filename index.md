---
#
# By default, content added below the "---" mark will appear in the home page
# between the top bar and the list of recent posts.
# To change the home page layout, edit the _layouts/home.html file.
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
#
layout: page
---

#![Zackory Erickskon](assets/images/Zackory_pr2.jpg)

I am a Postdoctoral Research Fellow in the Department of Neurology at Children's Hospital of Philadelphia, advised by Dr. Arjun Yodh, Dr. Wesley Baker, and Dr. Jennifer Lynch. My research focuses on translating diffuse optical spectroscopies for monitoring brain health. 

Previously, I received my PhD in Biomedical Engineering at Georgia Tech advised by Dr. Erin M. Buckley 

---

### News

  * Awarded AHA Postdoctoral Fellowship For "Diffuse Optics for Noninvasive Estimation of Cerebral Venous Oxygenation in Children with Congenital Heart Disease", 2025 - 2026
  * Serve as area chair at SPIE Photonics West, 2025
  * Serve as Poster Judge at Britan Chance Symposium, 2024
  * Awarded AHA Predoctoral Fellowship for "Improving", 2023 - 2024
  * Best paper finalist, "", 202
---

### Contact

**Email**: [zhaoh2@chop.edu](mailto:zhaoh2@chop.edu)

#**Office**: [Newell-Simon Hall](https://map.concept3d.com/?id=192#!m/15786) 4627

**Address**  
Carnegie Mellon University  
Robotics Institute  
5000 Forbes Ave  
Pittsburgh, PA 15213 USA


---


<h4><a href="https://scholar.google.com/citations?user=wElkTtIAAAAJ&hl=en">Google Scholar</a></h4>

<script>
function showhide(d) {
  var x = document.getElementById(d);
  if (x.style.display === "none") {
    x.style.display = "block";
  } else {
    x.style.display = "none";
  }
}
</script>

<table cellpadding="10" width="100%">
{% for pub in site.data.publications %}
    {% assign authors = {{pub.authors}} | split: ", " %}
    <tr>
        <td width="200" height="100">
            <img src="{{pub.image}}" img width="250">
        </td>
        <td><h6><a href="{{pub.pdf}}">{{pub.title}}</a></h6>
            <div style="line-height:50%;">
                <br>
            </div>
            <div style="font-size:medium">
                {% for author in authors %}
                    {% if forloop.index == authors.size %}
                        <nobr>{{ author }}</nobr>
                    {% else %}
                        <nobr>{{ author }},</nobr>
                    {% endif %}
                {% endfor %}<br>
                <em>{{pub.venue}}</em>, {{pub.year}}
                {% if pub.awards %}
                    <b> {{pub.awards}}</b>
                {% endif %}
                <br>
            </div>
            <div style="line-height:50%;">
                <br>
            </div>
            <div style="font-size:small">
                <em>
                    {% if pub.pdf %}
                        <a href="{{pub.pdf}}">[PDF]</a>
                    {% endif %}
                    {% if pub.projectpage %}
                        <a href="{{pub.projectpage}}">[Project Page]</a>
                    {% endif %}
                    {% if pub.code %}
                        <a href="{{pub.code}}">[Code]</a>
                    {% endif %}
                    {% if pub.bibtex %}
                        <a href="javascript:showhide('bib{{pub.id}}')">[Bibtex]</a>
                    {% endif %}
                    {% if pub.abstract %}
                        <a href="javascript:showhide('abs{{pub.id}}')">[Abstract]</a>
                    {% endif %}
                    {% if pub.video %}
                        <a href="{{pub.video}}">[Video]</a>
                    {% endif %}
                </em>
                <div id="bib{{pub.id}}" style="display:none">
                    <br>
                    <blockquote>
                        <div style="white-space: pre-wrap;">{{pub.bibtex}}</div>
                    </blockquote>
                </div>
                <div id="abs{{pub.id}}" style="display:none">
                    <br>
                    {{pub.abstract}}
                </div>
            </div>
            <br>
        </td>
    </tr>
{% endfor %}
</table>

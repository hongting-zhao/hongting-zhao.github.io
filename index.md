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
  * Serve as Poster Judge at Britan Chance , 2025
  * Best Paper Award, [Independence in the Home: A Wearable Interface for a Person with Quadriplegia to Teleoperate a Mobile Manipulator](https://sites.google.com/view/hat2-teleop/), at ACM/IEEE International Conference on Human-Robot Interaction (HRI), 2024
  * Organizing RSS 2024 workshop on [Learning for Assistive Robotics](https://sites.google.com/view/rss2024-assistive-robotics/home-page)
  * Organizing ICRA 2024 workshop on Exploring Role Allocation in Human-Robot Co-Manipulation
  * Virtual Experience Chair for Conference on Robot Learning (CoRL) 2023
  * Area Chair for CoRL 2023
  * Organizing RO-MAN 2023 special session on Human-Agent/Robot Interaction in Healthcare and Medicine
  * Organizing ICRA 2023 workshop on [Emerging paradigms for assistive robotic manipulation: from research labs to the real world](http://sirslab.diism.unisi.it/WorkshopManipulation/index.html)
  * Chair at IROS 2022 session on Art and Entertainment and Manipulation
  * Co-chair at ICRA 2022 session on Physical HRI
  * Area Chair for CoRL 2022
  * Associate Editor for RO-MAN 2022 
  * Organizing IROS 2022 workshop [Proximity Perception - Towards Next-Generation Multi-Modal Sensing in Soft Structures](https://proxelsandtaxels.org/en/)
  * Invited talk at RSS 2022 workshop on [Close Proximity Human-Robot Collaboration](https://sites.google.com/colorado.edu/rss-22-close-proximity-hrc/)
  * Invited talk at IROS 2021 workshop on [Proximity Perception in Robotics](https://www.proxelsandtaxels.org/en/)
  * Organizing an ICRA 2021 workshop [Learning for Caregiving Robots](https://sites.gatech.edu/learning-caregiving-icra2021/)
  * Invited talk at ICRA 2021 workshop on [Representing and Manipulating Deformable Objects](https://deformable-workshop.github.io/icra2021/)

---

### Contact

**Email**: [zackory@cmu.edu](mailto:zackory@cmu.edu)

**Office**: [Newell-Simon Hall](https://map.concept3d.com/?id=192#!m/15786) 4627

**Address**  
Carnegie Mellon University  
Robotics Institute  
5000 Forbes Ave  
Pittsburgh, PA 15213 USA

---

### Teaching

Spring 2025: [16-467: Human-Robot Interaction](https://zackory.com/16467-25/)  
Fall 2024: [16-741: Mechanics of Manipulation](https://zackory.com/16741-24/)  
Spring 2024: [16-762: Mobile Manipulation](https://zackory.com/mm2024/)  
Fall 2023: [16-741: Mechanics of Manipulation](https://zackory.com/16741-23/)  
Spring 2023: [16-887: Robotic Caregivers and Intelligent Physical Collaboration](https://zackory.com/rc2023/)  
Fall 2022: [16-741: Mechanics of Manipulation](https://zackory.com/16741-22/)  
Spring 2022: [16-887: Robotic Caregivers and Intelligent Physical Collaboration](https://zackory.com/rc2022/)  
Spring 2021: [BMED 4833/8813 - Robotic Caregivers](https://sites.gatech.edu/robotic-caregivers/2021-spring/)  
Spring 2020: [BMED 4803/8813 - Robotic Caregivers](https://sites.gatech.edu/robotic-caregivers/2020-spring/)  

---

### Extra links
You can find a recording of my Robotics PhD Defense at Georgia Tech here: [https://youtu.be/3DYv8SlaP2w](https://youtu.be/3DYv8SlaP2w)

In 2016, I participated in the 4th Heidelberg Laureate Forum. Here are [some photos from the 4th HLF](https://zackory.com/hlf4/).



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

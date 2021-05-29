---
layout: default
---

## Short Bio

With over 15 years of experience in Virtualization technologies I am currently
working on the lower-level parts of the stack to attack issues related to
performance, scalability, power-efficiency and security in hypervisors. Since
2015 I have been affiliated with UK & EU firms, building & architecting
solutions for efficient execution of workloads in the Cloud and at the Edge.  I
have been involved in many parts of the systems software stack, including
device drivers, memory management, network/block layers etc. 

Previously, I was a Post-doc at <a
href="http://research.cslab.ece.ntua.gr/">CSLab</a>, <a
href="https://www.ntua.gr">NTUA</a>, working on bridging the gap between common HPC
practices and virtualization. My research interests include I/O Virtualization,
systems software for high-performance I/O in virtualized environments, systems
support for heterogeneous platforms, communication architectures for clusters,
and scalable storage architectures based on clusters. 

I hold a Diploma in Engineering (2006) from <a
href="https://www.ece.ntua.gr">ECE, NTUA</a> and a PhD in Computer Engineering
(2013) from <a href="https://www.ntua.gr">NTUA</a>.

I have been involved in the academic research community for quite some time,
serving as TPC member or external referee for various CS-related conferences
and scientific journals. Since 2011, I co-organize the <a
href="https://vhpc.org">VHPC workshop series</a>, held in conjunction with
Europar, SC, and ISC.


## Work experience

<ul class="related-posts">


{% assign blog_posts = site.posts | where: 'bio', true %}
{% for post in blog_posts %}
    {%- assign date_format = site.minima.date_format | default: '%b %Y' -%}
<img class="work-picture" src="img/{{ post.image }}">
    <li class="main-page-list">
        <h4>

       <!-- <a href="{{ site.baseurl }}{{ post.url }}">-->
            <span>{{ post.company }} - {{ post.title }}</span>
             <div style="text-align: left; font-weight:lighter; font-size:70%;">
                <i>{{ post.date | date: "%b %Y" }}  &nbsp; {%- if post.date_end -%} &#8211; &nbsp;{{ post.date_end | date: date_format }} {%- endif -%}
		</i>
            </div>

            <small>{{ post.content }}</small>

        <!-- </a> -->
        </h4>

    </li>
    {% if forloop.last %}</ul>{% endif %}
{% endfor %}

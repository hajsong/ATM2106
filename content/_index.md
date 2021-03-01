---
title: "ATM2106"
---
<h1 style="background: url(images/img1banner.jpg);
           color: white;">
Atmospheric and Oceanic Circulation
</h1>

#### Course Description

The atmosphere and ocean control the earth climate system by transporting energy, heat, momentum and gas, as well as exchanging them across two components. Atmospheric and Oceanic Circulation (ATM2106) course aims to understand the circulation of the air and sea, and the climate system as a whole. This course will use both classical type of lectures and the state-of-the-art computer programming language such as Python to enhance the learning experience.

#### Instructor

* [Hajoon Song](http://airsea.yonsei.ac.kr/group/hajoonsong//#anchor)
* Office : Science Hall #544
* email : hajsong@yonsei.ac.kr
* telephone : 02-2123-2579

#### Teaching assistant
+ [Donghyuk Kim](http://airsea.yonsei.ac.kr/group/dhkim/#anchor)
+ Office : Science Hall #532
+ email : donghyuk95@yonsei.ac.kr

#### Class
+ Science Hall #523
+ Lecture : Tue 16:00 - 17:50, Thu 14:00 - 14:50
+ TA lecture : Thu 15:00 - 15:50

#### Office hours
Both Donghyuk and Hajoon will be happy to have office hours by appointment. Please email us!

#### Target students
This course is appropriate for students in the sophomore or junior year who want to gain basic knowledge about the circulation in atmosphere and ocean and the interactions between two bodies.

#### The objective
Upon the completion of this course, students will grasp the concept of atmospheric and oceanic circulations in the rotating earth. Then students will explain the current climate patterns and contemporary climate phenomena using the learnings from the classes. This descriptive course also provides an introduction to upper-level classes in the Department of Atmospheric Sciences.

#### Prerequisite
None, but the background in math and sciences is recommended.

#### Grading
+ Homework : 30%
+ Midterm : 30%
+ Final exam (or project) : 30%
+ Attendance and participation : 10%

#### Textbook
**Atmosphere, Ocean, and Climate Dynamics**
by John Marshall and R. Alan Plumb
<a href="http://marshallplumb.mit.edu" target="_blank">
<img style="width:200px;" src="http://marshallplumb.mit.edu/wp-content/uploads/2017/05/2017-05-17_3-52-08.png"></a>

<div class="row">
  <div class="col-xs-12 col-md-6">
    <div id="piechart"></div>
    <script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
    <script type="text/javascript">
    // Load google charts
    google.charts.load('current', {'packages':['corechart']});
    google.charts.setOnLoadCallback(drawChart);

    // Draw the chart and set the chart values
    function drawChart() {
      var data = google.visualization.arrayToDataTable([
      ['분류', '명'],
      ['국내외 연구소 및 대학 연구원', 8],
      ['국내외 대학원', 26],
      ['정부기관 및 공공기관', 11],
      ['관련 산업', 3],
      ['공군', 2]
    ]);

      // Optional; add a title and set the width and height of the chart
      var options = {'title':'최근 10년간 석사 졸업생 진로', 'width':400, 'height':300, chartArea:{left:10,top:20,width:'75%',height:'100%'},legend:'right', titleTextStyle:{fontSize:14}};

      // Display the chart inside the <div> element with id="piechart"
      var chart = new google.visualization.PieChart(document.getElementById('piechart'));
      chart.draw(data, options);
    }
    </script></div>
  <div class="col-xs-12 col-md-6">
    <div id="piechart1"></div>
    <script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
    <script type="text/javascript">
    // Load google charts
    google.charts.load('current', {'packages':['corechart']});
    google.charts.setOnLoadCallback(drawChart);

    // Draw the chart and set the chart values
    function drawChart() {
      var data = google.visualization.arrayToDataTable([
      ['분류', '명'],
      ['국내 연구소 및 대학 연구원', 21],
      ['해외 연구소 및 대학 연구원', 14],
      ['교수', 3],
      ['정부기관 및 공공기관', 10]
    ]);

      // Optional; add a title and set the width and height of the chart
      var options = {'title':'최근 10년간 박사 졸업생 진로', 'width':400, 'height':300, chartArea:{left:10,top:20,width:'75%',height:'100%'}, legend:'right', titleTextStyle:{fontSize:14}};

      // Display the chart inside the <div> element with id="piechart"
      var chart = new google.visualization.PieChart(document.getElementById('piechart1'));
      chart.draw(data, options);
    }
    </script></div>
</div>

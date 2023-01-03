---
layout: post
title: SOUTHEAST MACHINERY CO., LTD. (Project Management System)
subtitle: National Cheng Kung University Undergraduate Capstone Project
categories: Work-Demo
tags: [Microsoft Project, VBA, Project Managment] 
---


## Abstract 
In our capstone project, we took Southeast Machinery Company as an example to discuss the optimization and control of make-to-order production process. In order to improve the manufacturing process of their plastic extruders, our team introduced Microsoft Project to their company and developed an internal project management system
by Project VBA. Eventually, we conducted a survey which based on SUS (system usability scale) for understanding user experience and for further modification.

## Introduction

### About Southern Machinery 
SOUTHEAST MACHINERY is fully capable of supplying a range of plastic extrusion machinery, would like blown film machine, waste recycling making machine and drinking straw making machine.

### Problem Description 

<table>
 <tr>
	<td>Time</td>
	<td>Did not define standard manufacturing process<br>Did not track suppliers’ delivery process</td>
 </tr>
 <tr>
	<td>Cost</td>
	<td>Lack of bill of material to calculate cost<br>Quotation often based on past selling experience</td>
 </tr>
 <tr>
	<td>Performance</td>
	<td>Poor information flow within the company</td>
 </tr>
</table>

### Procedure
1. Interviewed managers to discover process defections
2. Defined reducing manufacturing time as the main problem
3. Created the bill of materials, decomposed manufacturing process, and defined cost
4. Utilized Microsoft Project for basic project management functions
5. Constructed an internal system for extended and customized project management functions
6. Tested the system and taught company's faculty how to operate
7. Conducted survey for user experience and made improvement

## Method
### Overview
- **Workflow Improvement**
	- Task process tracking
	- Data and reports aggregation
	- Abnormal work reports
	
<pre></pre>

- **Project Management**
<table>
 <tr>
  <th>Time Management</th>
  <th>Cost Management</th>
  <th>Performance Management</th>	 	
 </tr>
 <tr>
  <td>Task Duration<br>Activity-on-Node<br>Network Diagram<br>Gantt Chart</td>
  <td>Estimated Cost<br>Actual Cost<br>Wage</td>
  <td>Planning versus Execution<br>Performance Measurement Reports</td>
 </tr>
 <tr>
  <td colspan="3">Utilized schedule index: ACWP, BCWP, BCWS, CV</td>
 </tr>
</table>

- **Gap Model of Serive**	
	- **Gap 2**: Build accurate planning for outsoucing items
	- **Gap 3**: Increase the number of confirmations when executing the project to prevent unexpected accidents and accelerate the communication with suppliers
	- **Gap 5**: Gain a deeper understanding of customer needs and let the product be closer to their needs

### Microsoft Project
After interviewing managers to know their business processes, we broke down their processes to a task list, and therefore generated a network diagram and Gantt chart.
- **Task List**
![microsoft project](/assets/images/Undergrad Capstone Project/Microsoft Project.png "microsoft project")
<pre></pre>
- **Gantt Chart**
![gantt chart](/assets/images/Undergrad Capstone Project/Gantt Chart.png "Gantt chart")
<pre></pre>
- **Network Diagram**
![network diagram](/assets/images/Undergrad Capstone Project/Network Diagram.png "network diagram")

### System Development 
Apart from using basic Microsoft Project functions, our team also developed an internal system via Project VBA to assist Southern Machinery in customizing its own functions. With the system we developed, the company can launch its initial schedule, then control, and record the progress and the cost. After the whole manufacturing process, the manager can use this system to visualize data and generate relevant reports. The following images are the system of each business process.
- **Design Process**
![design process](/assets/images/Undergrad Capstone Project/Design.png "design process")
<pre></pre>
- **Outsourcing Process**
![outsourcing process](/assets/images/Undergrad Capstone Project/Outsourcing.png "outsourcing process")
<pre></pre>
- **Assembly Process**
![assembly process 1](/assets/images/Undergrad Capstone Project/Assembly 1.png "assembly process 1")
![assembly process 2](/assets/images/Undergrad Capstone Project/Assembly 2.png "assembly process 2")
![assembly process 3](/assets/images/Undergrad Capstone Project/Assembly 3.png "assembly process 3")
<pre></pre>
- **Testing Process**
![testing process 1](/assets/images/Undergrad Capstone Project/Testing 1.png "testing process 1")
![testing process 2](/assets/images/Undergrad Capstone Project/Testing 2.png "testing process 2")

### User Testing
At the end of system development, we launched a survey with google form which based on SUS in order to understand their user experience.
![user experience](/assets/images/Undergrad Capstone Project/User Experience.png "user experience")
From the responses we got, we could know:
1. Southern Machinery is willing to implement our system in the manufacturing process in the future.
2. Southern Machinery has difficulty quickly understanding how to use this system. Our team, therefore, wrote a user manual for them.

## Result and Discussion
1. In this stage, we just implement three phase plastic extruder manufacturing process in this system. We recommend Southern Machinery can also implement their other products.
2. After analyzing the task list in the Microsoft project, and inspecting the business process by our system, we decreased the total manufacturing by approximately 15%.
3. Our team only optimized the assembly process because of the limited data Southern Machinery could give. We suggested Southern Machinery can also optimize their supply chain.	

<style>
#about-southern-machinery, #problem-description, #procedure	{
	margin: 25px 0px 5px;	
}

#overview{
	margin: 25px 0px 5px;
}

p{
	text-align: justify;
}
</style>
# CGMCCSCBudget
---
title: "CGBudget"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```


Medicaid MCCSC
Total Medcidad Reimbursements = $569,026
```{r}
med = 610.91
perct = .16*.25
enrollTwo = 854 + 782 + 828 + 840 + 836 + 755 + 805 + 930
enrollThree = enrollTwo + 801 + 923
enrollFour = enrollTwo + 848 + 824
yearTwo = perct*enrollTwo*med
yearThree = perct*enrollThree*med
yearFour = perct*enrollFour*med; yearFour
total = yearTwo + yearThree + yearFour

# https://eddataexpress.ed.gov/data-element-explorer.cfm/tab/map/deid/5/
# https://compass.doe.in.gov/dashboard/enrollment.aspx?type=corp&id=5740
```
med = The amount of extra unrestricted funds that a district receives per student.

perct = .16 of Indiana students have IEP's.  Given the strong correlation between academic and SEL outcomes we are assuming that about .25 of those IEP students will identified as needing to include an SEL problem in their IEP making their SEL services eligible for Mediciad reminbursement.

enrollTwo = This is the student populations for the grades that will be included in the second year of the program where universal assessments will be conducted (7th, 9th, and 1st through 6th)

enrollThree = The student population for grades that will be included in the universal assessment for year three (Students in year two plus grades 8th and 10th)

enrollFour = The student population for grades that will be included in the universal assessment for year three (Students in year two and three plus grades 11th and 12th)

yearTwo = The amount of funding we would receive from Medicaid in year two

yearThree = Same as yearTwo, but with the numbers for year three

yearFour = Same yearThree, but with the numbers for year four

total = Is the four total amount we can expect to see in Medicaid rembursements


Installation - Buy in: Conference
Total conference cost = $22,800
```{r}
num.guest.speak = 4
cost.guest.speak = 1000
total.guest.speak = num.guest.speak*cost.guest.speak
food = 500
num.staff = 4
cost.staff = 20
hours = 15
total.staff = num.staff*cost.staff*hours
years = 4
total.con = (total.guest.speak+total.staff+food)*years; total.con
```
num.guest.speak = number of guest speakers
cost.guest.speak = cost for each of the guest speakers
num.staff = the number of staff that will support the event
cost.staff = hourly rate for staff
food = food for event
hours = number of hours each staff member will work
num.staff = number of staff to clean up after and to manage the event
years = number of years the event will take place


Installation - Buy in: Town halls
Total Town Hall Costs = $3,600
```{r}
food = 300
num.staff = 3
cost.staff = 20
hours = 10
years = 4
total.town = (food+num.staff*cost.staff*hours)*years; total.town

```


Installation - Buy in: climate survey
Total cost of climate survey = $3,200
```{r}
num.staff = 1
hours = 20
cost.staff = 20
times  = 2
years = 4
total.climate = num.staff*hours*cost.staff*times*years; total.climate
```
times =  is the number of times we conduct the survey which will be twice per year for the pre and post climate survey.


Installation - Buy in: interviews / focus groups
Total cost of focus groups = $1,500
```{r}
staff = 5
hours.fg = 75
cost.staff = 15
total.focus =  staff*hours*cost.staff; total.focus 
```
hours.fg  = We are anticipating about 25 one foucs groups over the course of the implementation grant.  We are expecting one our of prepartion for each of the focus groups and one hour of analysis for each of them as well. 



Installation - Management: school based implementation teams
```{r}
num.staff = 7
schools = 6
hours = 30
cost.staff = 15
years = 4
total.teams = num.staff*schools.dis*hours*cost.staff*years; total.teams
```
Need to provide stipends to staff that are on the school and district teams

schools = number of schools that will receive the stipends five three middle and two high schools

Installation - Management: initial training
```{r}
num.progams = 5
cost.prog = 3000
food = 500
staff = 100
stipend = 50
total.it = num.progams*cost.prog+staff*stipend; total.it
```
trainer = the person who will adminstering the training.
partic = the number of participants
staff = the staff that will be working the event

SANDY WASHBURN swashbur@indiana.edu can provide training for PBIS and Second Steps program.
Boys town = http://www.boystowntraining.org/well-managed-schools.html

Maybe for strong teens and SSIS SEL PARCS needs to become experts and provide the training?


Installation - Management: coaching elem
```{r}
num.classes = 20 
num.hours = 30
cost.staff = 20
total.coel = num.classes*num.hours*cost.staff; total.coel
```
el.num.coaches = number of coaches for the elemenatry schools.  Two coaches for the three programs (Well managed schools, PBIS, and Second steps)

num.classes = number of classrooms implementing the programs



Installation - Management: coaching middle high
```{r}
num.hours = 40*30
cost.staff = 20
total.comh = num.hours*cost.staff; total.coel
```
num.hours = Total number of hours needed is 40 classess and 20 hours per classroom


Initial Implementation: SSIS program
```{r}
cost.per.class = 268
classes =  40
years = 4
total.ssis = cost.per.class*classes*years;total.ssis

```
This is an operating expensive need to get one year total 

Initial Implemenation: Panorama
```{r}
cost.per.student = 1.5
num.students = 5500
years = 4
total.pan = cost.per.student*num.students*years; total.pan
```
This is an operating expensive need to get one year total 


Interventionists (Tier 2 and 3 support)
```{r}
num.students = .20*1100
hours = 30
cost.staff = 20
total.interven = num.students*hours*cost.staff; total.interven
```
num.students = number of students that will need to served

Assuming that we eventually serve 20% of the population with intensive services at least once.


This is an operating expensive need to get one year total 

Evaluation
```{r}

```
PARCS in conjunction with CEEP with provide the first two years of the evaluation for free and then CEEP will pick up the cost after the first two years.

Total Cost
```{r}
data.frame()
```




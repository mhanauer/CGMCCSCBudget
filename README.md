---
title: "MCCSC Lilly Budget"
output:
  word_document: default
  html_document: default
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```
Total Cost for Building Business Skills for the Future Program
Total Cost: $974,774


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



Installation - Management: School based implementation teams stipends
Total cost for stipends =  $75,600
```{r}
num.staff = 7
schools = 6
hours = 30
cost.staff = 15
years = 4
total.teams = num.staff*schools*hours*cost.staff*years; total.teams
```
Need to provide stipends to staff that are on the school and district teams

schools = number of schools that will receive the stipends five three middle and two high schools

Installation - Management: Training for SEL Coordinator
Total training costs for SEL Coordinator: $16,000
```{r}
num.progams = 5
cost.prog = 3000
food = 500
travel = 500
total.it = num.progams*cost.prog+food+travel; total.it
```
cost.prog = Need to figure out what it will cost to train someone in all the programs (PBIS, Well Managed Schools, Second Step, SSIS SEL, Strong Teens)

Installation - Management: Stipends for staff training for elementary
Total stipends for elementary staff: $33,824
```{r}
num.staff = 14*8*2 
num.hours.yearly.train = 4*4
num.hours.coach = num.staff*9
cost.staff = 15
total.coel = num.hours.coach*cost.staff + num.staff*num.hours.yearly.train; total.coel
```
num.classes = There are 14 elementary schools with grades Pre-K through 6th and about two teachers per grade

num.hours.yearly.train = Each staff will receive four hours of training over four years as a their yearly training.

num.hours = This is the number of hours each staff member will spend in training so one hour per month



Installation - Management: Stipends for staff training for middle and high school
Total stipends for middle and high staff: $46,875
```{r}
num.staff.mid = 15*3
num.staff.high = 20*4
num.hours.coach = (num.staff.high+num.staff.mid)*9
num.hours.yearly.train = 4*4*(num.staff.mid+num.staff.high)
cost.staff = 15
total.comh = num.hours.coach*cost.staff + num.hours.yearly.train*cost.staff; total.comh
```
num.staff.mid = There are about 15 teachers who would receive training across 3 middle schools
num.staff.high = There are about 20 teachers who would receive training across 2 middle schools

SEL Coordinator
Total SEL Coordinator: $260,000
```{r}
cost = 65000
years = 4
total.selcor = cost*years; total.selcor
```


Initial Implementation: SSIS SEL program
Total cost of SSIS SEL: $48,240
```{r}
cost.per.class = 268
classes =  45
years = 4
total.ssis = cost.per.class*classes*years;total.ssis

```
This is an operating expensive 

Initial Implemenation: Panorama
Total Cost Panorama: $34,929
```{r}
cost.per.student = 1.5
enrollTwo = 854 + 782 + 828 + 840 + 836 + 755 + 805 + 930
enrollThree = enrollTwo + 801 + 923
enrollFour = enrollTwo + 848 + 824
totalenroll = sum(enrollTwo, enrollThree, enrollFour)
total.pan = cost.per.student*totalenroll; total.pan
```
Here we are using the enroll scheme as with Mediciad where we are rolling out the universal assessments. 

This is an operating expensive need to get one year total 


Interventionists (Tier 2 and 3 support)
```{r}
hours = 15
enrollTwo = (854 + 782 + 828 + 840 + 836 + 755 + 805 + 930)*.15
enrollThree = (enrollTwo + 801 + 923)*.15
enrollFour = (enrollTwo + 848 + 824)*.15
totalenroll = sum(enrollTwo, enrollThree, enrollFour)
cost.staff = 15
total.interven = totalenroll*hours*cost.staff; total.interven
```
hours = this is the number hours we anticpate each interventionist working with the student.

.15 is multiplied by each enrollment, because that is the percentage of students we anticpate to serve each year.

This is an operating expensive need to get one year total 

Evaluation
Total Evaluation: $22,700
```{r}
focusGroups = 3
outputAnalyses = 2
outcomeAnalyses = 2
finalReports = 2
hours = 10*(focusGroups+outputAnalyses+outcomeAnalyses+finalReports)
costStaff = 15
overSight = 5000
totalEval = hours*costStaff*2 +(overSight*4); totalEval
```
PARCS in conjunction with CEEP with provide the first two years of the evaluation for free and then CEEP will pick up the cost after the first two years.

outputAnalyses = Analyses related to the outputs that will be measured

hours = We anticpate about 10 hours for each project

overSight = For John Hitchcock to review and oversee the evaluation each year. 

Total Cost for Building Business Skills for the Future Program
Total Cost: $974,774
```{r}
totalCosts = data.frame(total.con, total.town, total.climate, total.focus, total.teams, total.it, total.coel, total.comh, total.selcor, total.ssis, total.pan, total.interven, totalEval)
totalCostsSum = rowSums(totalCosts); totalCostsSum
```




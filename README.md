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
Total Cost: $1,042,348


Medicaid MCCSC
Total Medcidad Reimbursements = $569,026
```{r}
med = 610.91
perct = .16*.15
enrollTwo = 288 + 798 + 854 + 782 + 828 + 840 + 836 + 755 + 805 + 930
enrollThree = enrollTwo + 801 + 923
enrollFour = enrollThree + 848 + 824
yearTwo = perct*enrollTwo*med
yearThree = perct*enrollThree*med
yearFour = perct*enrollFour*med; yearFour
total = yearTwo + yearThree + yearFour

# https://eddataexpress.ed.gov/data-element-explorer.cfm/tab/map/deid/5/
# https://compass.doe.in.gov/dashboard/enrollment.aspx?type=corp&id=5740
```
med = The amount of extra unrestricted funds that a district receives per student.

In this model I am assuming that kids who have an IEP with SEL will have it each year.  I am assuming that about 2.4% new IEP's will be present each for the population that is being assesed.  The new screeners will produce 2.4%

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
num.guest.speak = 2
cost.guest.speak = 5000

total.guest.speak = num.guest.speak*cost.guest.speak
food = 500
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
```{r}
people = 300
costPerson = 10
years = 4
total.town = people*costPerson*years; total.town

```
years = only have a town halls as a method for increasing buy in.  So only three years, because we are rolling out the program in three stages (7th, 9th, and Elementary, 8th and 10th, 11th and 12th)

Buy in: climate survey (PARCS provides)
```{r}
num.staff = 1
hours = 20
cost.staff = 20
times  = 2
years = 3
total.climate = num.staff*hours*cost.staff*times*years; total.climate
```
times =  is the number of times we conduct the survey which will be twice per year for the pre and post climate survey.

years = only have a climate survey as a method for evaluating buy in.  So only three years, because we are rolling out the program in three stages (7th, 9th, and Elementary, 8th and 10th, 11th and 12th)

Installation - Buy in: interviews / focus groups
Total cost of focus groups = $1,500
```{r}
numFGs = 10
hours.fg = 4
years = 4
cost.staff = 15
yearlyCost = numFGs*hours.fg*cost.staff
total.focus =  numFGs*hours.fg*cost.staff*years; total.focus 
```



Installation - Management: School based implementation teams stipends
Total cost for stipends =  $75,600
```{r}
num.staff = 7
schools = 6
hours = 9*3
cost.staff = 20
years = 4
total.teams = num.staff*schools*hours*cost.staff*years; total.teams
```
Need to provide stipends to staff that are on the school and district teams

9 comes from the number of months

schools = number of schools that will receive the stipends five three middle and two high schools

Installation - Management: Training for SEL Coordinator
# Don't think we need this anymore find a person who knows these programs.
```{r}
num.progams = 5
cost.prog = 3000
food = 500
travel = 500
total.it = num.progams*cost.prog+food+travel; total.it
```
cost.prog = Need to figure out what it will cost to train someone in all the programs (PBIS, Well Managed Schools, Second Step, SSIS SEL, Strong Teens)

Installation - Management: Stipends for staff training from coaches for elementary
```{r}
num.staff = 14*8*2 
num.hours.yearly.train = 4*num.staff
num.hours.coach = num.staff*9
cost.staff = 15
total.trel = num.hours.coach*cost.staff + num.hours.yearly.train*cost.staff; total.trel
```
num.classes = There are 14 elementary schools with grades Pre-K through 6th and about two teachers per grade

num.hours.yearly.train = Each staff will receive four hours of training over four years as a their yearly training.

num.hours = This is the number of hours each staff member will spend in training so one hour per month

To get the cost of yearly stipends for trainings, add the second half of the total equations for ele and mid and high.

Installation - Management: Stipends for staff training from coaches for middle and high school
```{r}
highStaff = 20
middleStaff = 15
initial = 4
cost = 15

yearTwoStaff = highStaff+middleStaff
totalYearTwoPD = yearTwoStaff*initial*cost
  
yearThreeStaff = highStaff+middleStaff
totalYearThreePD = yearThreeStaff*initial*cost

yearFourStaff = highStaff*2
totalYearFourPD = yearFourStaff*initial*cost


```
num.staff.mid = There are about 15 teachers who would receive training across 3 middle schools
num.staff.high = There are about 30 (twice as many grades) teachers who would receive training across 2 middle schools

SEL Coordinator
Total SEL Coordinator: $260,000
```{r}
cost = 65000
years = 4
total.selcor = cost*years; total.selcor
```


Initial Implementation: SSIS SEL program
```{r}
cost.per.class = 268/ 25
classesYearTwo = 930 + 805
classesYearThree = classesYearTwo + 801
ssisYearTwo = cost.per.class*classesYearTwo
ssisYearThree = ssisYearTwo + cost.per.class*classesYearThree
ssisYearFour = ssisYearThree
total.ssis = round(ssisYearTwo+ssisYearThree+ssisYearFour);total.ssis
```
classesYearTwo = We will only be serving about 

This is an operating expensive 

Aperture education
```{r}
cost.per.student = 3.5
enrollTwo = 288 + 798 + 854 + 782 + 828 + 840 + 836 + 755 + 805 + 930
totalYearTwo = enrollTwo*cost.per.student

enrollThree = enrollTwo + 801
totalYearThree = enrollThree*cost.per.student

enrollFour = enrollThree + 848 + 824
totalYearFour = enrollFour*cost.per.student

years = 4
total.pan = cost.per.student*enroll*years; total.pan
```
enrollTwo = This will be pre-k through 6th, because we are using the universal screener for all the elementary students.

enrollThree  = enrollTwo + the 10th graders, because SSIS SEL no longer applies to 10th graders.

enrollFour = enrollThree + the 11th and 12th graders, because there stuff is being rolled out.

This is an operating expensive need to get one year total 

Coaches elementary
```{r}
num.staff = 14*8*2 
num.hours.coach = num.staff*20
cost.staff = round((55859/(52*40)))
total.coel = num.hours.coach*cost.staff; total.coel
```


num.classes = There are 14 elementary schools with grades Pre-K through 6th and about two teachers per grade

num.hours = This is the number of hours each each coach will spend training so hour per month training and one hour per month

Coaches for staff training from coaches for middle and high school

Total Coaching for middle and high staff: $33,750
```{r}
num.staff.mid = 15
num.staff.high = 30
numberHoursCoaching = 20
cost.staff = round((55859/(52*40)))

yearTwoCosts = (num.staff.mid+num.staff.high)*numberHoursCoaching*cost.staff
yearThreeCosts = (num.staff.mid+num.staff.high)*numberHoursCoaching*cost.staff
yearFourCosts = (num.staff.high*2)*numberHoursCoaching*cost.staff

```
Strong Teens Book
```{r}
book = 32
```
Only need one book, because the SEL coordinator will create trainings from the book.

Divide the num.hours.coach by three, because you want to estimate the hours over three years for the budget.

cost.staff = http://www1.salary.com/IN/Social-Worker-MSW-salary.html 

total.comh = Need to divide total.comh by three, because we need to estimate the yearly cost, 


Interventionists (Tier 2 and 3 support)
Total Interventionists costs: $405,506.2
```{r}
hours = 21
cost.staff = 15
tierTwo = .05
tierThree =  .025 
enrollTwoTwo = round(((288 + 798 + 854 + 782 + 828 + 840 + 836 + 755 + 805 + 930)*tierTwo)/5)
enrollTwoThree = round(((288 + 798 + 854 + 782 + 828 + 840 + 836 + 755 + 805 + 930)*tierThree))
enrollTwoTwoCosts = enrollTwoTwo*hours*cost.staff
enrollTwoThreeCosts = enrollTwoThree*cost.staff*hours
yearTwoCosts = enrollTwoThreeCosts+enrollTwoTwoCosts

enrollThreeTwo = round(enrollTwoTwo + ((801 + 923)*tierTwo / 5))
enrollThreeThree = round(enrollTwoThree + (801 + 923)*tierThree)
# If you wanted to add a reduction in 5% you would take enrollTwo * .95
enrollThreeTwoCosts = enrollThreeTwo*hours*cost.staff
enrollThreeThreeCosts = enrollThreeThree*hours*cost.staff
yearThreeCosts = enrollThreeTwoCosts + enrollThreeThreeCosts

enrollFourTwo = round(enrollThreeTwo + ((848 + 824)*tierTwo / 5))
enrollFourThree = round(enrollThreeThree + (848 + 824)*tierThree)
# If you wanted to add a reduction in 5% you would take enrollTwo * .95
enrollFourTwoCosts = enrollFourTwo*hours*cost.staff
enrollThreeThreeCosts = enrollFourThree*hours*cost.staff
yearFourCosts = enrollFourTwoCosts + enrollThreeThreeCosts

# Getting the number of hours worked here
enrollTwoTwoHours = enrollTwoTwo*hours
enrollTwoThreeHours = enrollTwoThree*hours
totalTwoHours = round(enrollTwoTwoHours+enrollTwoThreeHours)

enrollThreeTwoHours =  enrollThreeTwo*hours
enrollThreeThreeHours = enrollThreeThree*hours
totalThreeHours = round(enrollThreeTwoHours+enrollThreeThreeHours)

enrollFourTwoHours = enrollFourTwo*hours
enrollFourThreeHours = enrollFourThree*hours
totalFourHours = round(enrollFourTwoHours+enrollFourThreeHours)

total.interven = yearFourCosts + yearThreeCosts + yearTwoCosts; total.interven
```
This is assuming no help from anyone at MCCSC.

enrollTwoTwo = .10 of the population will be small groups of five students; however, referral system is only about 50% accuracte.  The 2.5% percent will be intensive tier three services.

Remember that you are dividing by 5, because for tier two services you are providing groups of five services.

enrollTwoThree= .05 of the population will be intensive one on one services.

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
totalEval = hours*costStaff +(overSight); totalEval
```
PARCS in conjunction with CEEP with provide the first two years of the evaluation for free and then CEEP will pick up the cost after the first two years.

outputAnalyses = Analyses related to the outputs that will be measured

hours = We anticpate about 10 hours for each project

overSight = For John Hitchcock to review and oversee the evaluation each year. 

Total Cost for Building Business Skills for the Future Program
Total Cost: $1,042,348
```{r}
totalCosts = data.frame(total.con, total.town, total.climate, total.focus, total.teams, total.it, total.coel, total.comh, total.selcor, total.ssis, total.pan, total.interven, totalEval, total.trel, total.trmh)
totalCostsSum = rowSums(totalCosts); totalCostsSum
```




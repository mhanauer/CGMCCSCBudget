---
title: "MCCSC Lilly Budget"
output:
  word_document: default
  html_document: default
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

Aimsweb Behavior
```{r}
preK = 288; k = 798; first = 854; second = 782; third = 828; fourth = 840; fifth  = 836; sixth = 755; seventh = 805; eighth  = 801; ninth = 930; tenth = 923; eleventh = 848; twelfth = 824

cost.per.student = 1

enrollOne = sum(preK,k, first, second, third, fourth, fifth, sixth, seventh, ninth)
totalYearOne = enrollTwo*cost.per.student

enrollTwo = sum(preK,k, first, second, third, fourth, fifth, sixth, seventh, ninth)
totalYearTwo = enrollTwo*cost.per.student

enrollThree = enrollTwo + eighth + tenth
totalYearThree = enrollThree*cost.per.student

enrollFour = enrollThree + eleventh 
totalYearFour = enrollFour*cost.per.student

```
enrollTwo = This will be pre-k through 6th, because we are using the universal screener for all the elementary students.

enrollThree  = enrollTwo + the 10th graders, because SSIS SEL no longer applies to 10th graders.

enrollFour = enrollThree + the 11th and 12th graders, because there stuff is being rolled out.

This is an operating expensive need to get one year total 

Interventionists (Tier 2 and 3 support)
```{r}
hours = 21
cost.staff = 15
tierTwo = .05
tierThree =  .025
preK = 288; k = 798; first = 854; second = 782; third = 828; fourth = 840; fifth  = 836; sixth = 755; seventh = 805; eighth  = 801; ninth = 930; tenth = 923; eleventh = 848; twelfth = 824    
enrollTwoTwo = round(((sum(preK,k, first, second, third, fourth, fifth, sixth, seventh, ninth))*tierTwo)/5)
enrollTwoThree = round(sum(preK,k, first, second, third, fourth, fifth, sixth, seventh, ninth)*tierThree)

yearThreeEnroll = preK +k  + first + second + third + fourth + fifth + sixth + seventh + ninth+ eighth+ tenth

enrollTwoTwoCosts = enrollTwoTwo*hours*cost.staff
enrollTwoThreeCosts = enrollTwoThree*cost.staff*hours
yearTwoCosts = enrollTwoThreeCosts+enrollTwoTwoCosts

enrollThreeTwo = round(enrollTwoTwo + (eighth  + tenth)*tierTwo / 5)
enrollThreeThree = round(enrollTwoThree + (eighth  + tenth)*tierThree)
enrollThreeTwoCosts = enrollThreeTwo*hours*cost.staff
enrollThreeThreeCosts = enrollThreeThree*hours*cost.staff
yearThreeCosts = enrollThreeTwoCosts + enrollThreeThreeCosts

# Remember that you will still be serving tier two students in year three students in year four, but not year two and three tier students, because they have been phased out. 
enrollFourTwo = round(((eighth + tenth + eleventh)*tierTwo / 5))
enrollFourThree = round((eighth + tenth + eleventh)*tierThree)
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
```
Assuming that you will only see the reductions in tier two students at the end of year three therefore, costs won't go down until year four.

This is assuming no help from anyone at MCCSC.

enrollTwoTwo = .10 of the population will be small groups of five students; however, referral system is only about 50% accuracte.  The 2.5% percent will be intensive tier three services.

Remember that you are dividing by 5, because for tier two services you are providing groups of five services.

enrollTwoThree= .05 of the population will be intensive one on one services.

hours = this is the number hours we anticpate each interventionist working with the student.

.15 is multiplied by each enrollment, because that is the percentage of students we anticpate to serve each year.

This is an operating expensive need to get one year total 


Medicaid MCCSC Plan 1 
```{r}
med = 610.91
perct = .16*.15
preK = 288; k = 798; first = 854; second = 782; third = 828; fourth = 840; fifth  = 836; sixth = 755; seventh = 805; eighth  = 801; ninth = 930; tenth = 923; eleventh = 848; twelfth = 824 
enrollTwo = round(preK + k + first + seventh + ninth)
enrollThree = round(enrollTwo + second + third + fourth + eighth + tenth)
enrollFour = round(enrollThree + fifth + sixth + eleventh + twelfth)
yearTwo = round(round(perct*enrollTwo)*med)
yearThree = round(round(perct*enrollThree)*med)
yearFour = round(round(perct*enrollFour)*med)
total = round(yearTwo + yearThree + yearFour)

# https://eddataexpress.ed.gov/data-element-explorer.cfm/tab/map/deid/5/
# https://compass.doe.in.gov/dashboard/enrollment.aspx?type=corp&id=5740
```
You added the round around perct and enrollment to make the numbers match the budget narrative.

med = The amount of extra unrestricted funds that a district receives per student.

iep =  1752 / 10925; iep = https://nces.ed.gov/ccd/districtsearch/district_detail.asp?Search=1&details=1&City=Bloomington&State=18&DistrictType=1&DistrictType=2&DistrictType=3&DistrictType=4&DistrictType=5&DistrictType=6&DistrictType=7&DistrictType=8&NumOfStudentsRange=more&NumOfSchoolsRange=more&ID2=1800630

famSizeTwo = 3384*12
famSizeThree = 4255*12
famSizeFour = 5125*12
famSizeFive = 5996*12
famSizeAverage = mean(famSizeTwo, famSizeThree, famSizeFour, famSizeFive)



In this model I am assuming that kids who have an IEP with SEL will have it each year.  I am assuming that about 2.4% new IEP's will be present each for the population that is being assesed.  The new screeners will produce 2.4%

Teacher referral systems only get about half of students, but we have a stronger teacher referral systems and we have social workers who also look at IEP students for social issues and parents involved in the referral system therefore we are only anctipating that we have missed about 15% of the IEP students who need 

enrollTwo = This is the student populations for the grades that will be included in the second year of the program where universal assessments will be conducted (7th, 9th, and 1st through 6th)

enrollThree = The student population for grades that will be included in the universal assessment for year three (Students in year two plus grades 8th and 10th)

enrollFour = The student population for grades that will be included in the universal assessment for year three (Students in year two and three plus grades 11th and 12th)

yearTwo = The amount of funding we would receive from Medicaid in year two

yearThree = Same as yearTwo, but with the numbers for year three

yearFour = Same yearThree, but with the numbers for year four

total = Is the four total amount we can expect to see in Medicaid rembursements


Medicaid PLan 2
```{r}
preK = 288; k = 798; first = 854; second = 782; third = 828; fourth = 840; fifth  = 836; sixth = 755; seventh = 805; eighth  = 801; ninth = 930; tenth = 923; eleventh = 848; twelfth = 824 

totalEnroll = 11200

yearTwoEnrollPercnt = round(sum(preK,k, first, second, third, fourth, fifth, sixth, seventh, ninth)/totalEnroll,2)

yearThreeEnrollPercnt = round(sum(eighth, tenth)/totalEnroll,2)

yearFourEnrollPercnt = round(eleventh / totalEnroll,2)

#Assuming that they stay on Medicaid and that we are eventually screening everyone 
medicaid2017 = 51213.02*2
medicaid2017Half = 51213.02

yearTwoMed = round(medicaid2017Half*yearTwoEnrollPercnt)
  
yearThreeMed = round(yearTwoMed + medicaid2017Half*yearThreeEnrollPercnt)

# Here we are assuming that we have phased out year so only include new kids from year three no year two
yearFourMed = round(medicaid2017Half*yearThreeEnrollPercnt + medicaid2017Half*yearFourEnrollPercnt)

totalMedicaid = sum(yearTwoMed, yearThreeMed, yearThreeMed) 

#Assuming that they are off of Medicaid after a year screening everyone 
medicaid2017 = 51213.02*2
medicaid2017Half = 51213.02

yearlyMed =medicaid2017Half/3

totalMedicaid = yearlyMed*3

yearTwoMed = medicaid2017Half*yearTwoEnrollPercnt
  
yearThreeMed = medicaid2017Half*yearThreeEnrollPercnt

yearFourMed = medicaid2017Half*yearFourEnrollPercnt

totalMedicaid = sum(yearTwoMed, yearThreeMed, yearThreeMed) 
```
#Assuming that they stay on Medicaid and that we are eventually screening everyone 

Medicaid revenue was $51,213.02 in the first half of 2016-2017 school year.  I am assuming it will be the same in the second half therefore it is doubled.

If we are rolling out the program across the district and expecting that we have caught about 50% of the needy students, then we can assume that we will bring in half that $51213.02 each year.  I am assuming the kids are staying on Medicaid so I am taking the total increase from the year before and add in the percentage of the students being rolled out, because that is the increase we will see in the next year.

#Assuming that they are off of Medicaid after a year screening everyone 
Here we are assuming that new kids are off after one year so the increase is just medicaid2017Half/3 each year. 

#Assuming that they stay on Medicaid throughout the grant and that we don't screen 10-12 graders.
First we need to get the percentage of students in each roll out so that we can estimate what percentage of the population will receive the programs each year.  Then we can take that percentage of times the increase which is medicaid2017Half/3.  We need the percentage of the total population, because we are no longer serving the whole district and medicaid2017Half/3 assuming that the whole district is divided by 1/3.  So we need to take medicaid2017Half * the percentage of the population that is actually being served.  Because we are assuming that students remain in Medicaid in this model we add the previous year to current amount.     


Installation - Buy in: Conference
```{r}
num.guest.speak = 1
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


Installation - Buy in: interviews / focus groups
Total cost of focus groups = $1,500
```{r}
numFGs = 4*6
hours.fg = 4
cost.staff = 15

fgCosts = numFGs*hours.fg*cost.staff

analHours = 10
analCosts = analHours*numFGs*cost.staff

trans = 2*60*numFGs

food = 30
foodCosts = food*numFGs

years = 3

total.focus = (fgCosts+analCosts+trans+foodCosts) *years; total.focus 
```
numFGS = There are four stakeholder groups and we will conduct 6 focus groups with each stakeholder. 
food = two pizzas at $15 a piece

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


Installation - Management: Implementation teams stipends

```{r}
num.staff = 5
schools = 19
hours = 9*3
cost.staff = 20
total.teams = num.staff*schools*hours*cost.staff; total.teams
```

Second Step
```{r}
kFifth= 2259/6
classes = 390 + 113
totalSS = kFifth*classes
```
390 elementary teachers and 113 middle school teachers

kFifth = k through fifth comes in a bundle costing $2,259.  So I divide that by 6, because there are 6 grades included in the package.  Assuming I can get this rates for the other grades

I am going to assume that if we order the bundle, we can get the sixth grade included at the price

Need to provide stipends to staff that are on the school and district teams

9 comes from the number of months

schools = number of schools that will receive the stipends five three middle and two high schools

Installation - Management: Stipends for staff training from
```{r}
staff = 482+380
cost = 20
hours = 4
totalStip = round(staff*cost*hours)
```
There are 715 general education teachers at MCCSC.  Given that we are rolling out the program to approximently 1/3 of the teacher each year. 


SEL Coordinator and Facing History and Ourselves Coordinator
```{r}
cost = 65000*1.4
years = 4
total.selcor = cost*years; total.selcor
```
cost = $65,000 a year plus 40% cost of benefits.


Initial Implementation: SSIS SEL program
```{r}
cost.per.student = 268/ 25
classesYearTwo = 930 + 805
classesYearThree = classesYearTwo + 801
ssisYearTwo = cost.per.class*classesYearTwo
ssisYearThree = ssisYearTwo + cost.per.student *classesYearThree
ssisYearFour = ssisYearThree
total.ssis = round(ssisYearTwo+ssisYearThree+ssisYearFour);total.ssis
```
cost.per.student = program costs $268 per class and it serves up to 25 students.

classesYearTwo = We will only be serving about 

This is an operating expensive 



Divide the num.hours.coach by three, because you want to estimate the hours over three years for the budget.

cost.staff = http://www1.salary.com/IN/Social-Worker-MSW-salary.html 

total.comh = Need to divide total.comh by three, because we need to estimate the yearly cost, 


Evaluation
```{r}
confSurvey = 5*15*2

dataEntry = 30*15*2

focusGroups = 10*4*15*2

dataAnalysis = 45*30*2

overSight = 5000*2

finalReports = 30*15*2

pizza = 30*10*2

contentAnalysis = 10*10*15*2

trans = 2*60*10*2

yearOneTwo = focusGroups+overSight+contentAnalysis+pizza+trans 

teachersYears2and3 = 556

cost = 15

times = 2

fidelity = teachers*cost*times

yearThreeFourEval = confSurvey+dataEntry+focusGroups+dataAnalysis+overSight+finalReports+contentAnalysis+pizza+trans+fidelity
```
Times 2, because we are estimating the costs for two years at a time.

Focus groups will take approximentaly 4 hours per each  


PARCS in conjunction with CEEP with provide the first two years of the evaluation for free and then CEEP will pick up the cost after the first two years.

outputAnalyses = Analyses related to the outputs that will be measured

hours = We anticpate about 10 hours for each project

overSight = For John Hitchcock to review and oversee the evaluation each year. 

PARCS
```{r}
students = 2
weeks = 32
hours = 20
wage = 32.88
student = round(students*weeks*hours*wage)

rebecca = round(43*15*52)

anna = 35000
matt = 15000

yearOne = anna+matt+rebecca+student
yearTwo = matt+rebecca+student
yearThree = rebecca+student
yearFour = yearThree
```
2 students *32 weeks in the college school year *20 hours per week *4 years of implementation grant =  5,120 total hours
wage = http://www.healthcarewages.org/school-psychologist-salary/states/

MCCSC Staff Support
```{r}
sc = 20
scSalary = 47255
sw = 17
swSalary = 55859
sp = 5.6
spSalary = 32.88*52*40
bs = 2
bsSalary = 33862
perct = .05
allStaff = round((sc*scSalary+sw*swSalary+sc*scSalary+bs*bsSalary)*perct)



```
20 Master’s level school counselors 1 for every 500 students
	17 social workers  1: for every 647 students
	5.6 school psychologists 1 for every 1964 students
2 Behavior specialists	
scSalary = http://www.school-counselor.org/indiana-school-counselor.html#context/api/listings/prefilter

bsSalary = https://www.glassdoor.com/Salaries/behavior-specialist-salary-SRCH_KO0,19.htm


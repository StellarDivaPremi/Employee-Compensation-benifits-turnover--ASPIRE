# Employee-Compensation-benifits-turnover--ASPIRE

ASPIRE FACILITY MANAGEMENT PROJECT ON HR ANALYTICS

Project Title	 Employee turnover Prediction
Skills take away From This Project	Data Wrangling, EDA, Visualisations ,Dashboard
Domain	HR Analytics

Doing HR Analytics for Turnover Rate for Aspire Facility Management services
Calculating employee turnover: The problem

In Aspire Facility management services, the attrition and Hiring rate are very fast paced duE to bluE collared employees changing jobs often due to various reasons.

The management wanted a report on how attrition was happening and reason for it and how to stop it by knowing the attrition rate or turnover rate every year(per quarter).

As those familiar with this topic might know, there is currently no ‘right’ way to calculate turnover. A quick Google search will show multiple websites using different formulas. The same happens at the professional bodies.

The American National Standards Institute (ANSI), an institute dedicated to facilitating consensus standards, uses a different definition than the International Organization for Standardization (ISO). The turnover formula proposed by ISO also poses some ambiguity and can be explained (and thus calculated) in more than one way.
It is easy to understand why HR practitioners will get confused when it comes to this topic. Besides the technical difficulties of calculating the total number of employees and the ones who quit – a topic we won’t get into in this article – there is the challenge of calculating the turnover rate. Having a clear formula will help tremendously.
In order to answer the question how to calculate an employee turnover rate, we first need to define what we mean by employee turnover.
Employee: ANSI defines an employee as an individual ‘that received any payroll payment during the pay period that includes the 12th day of the month’. Additionally, we would like to add that an Employee cannot be a new Hire due as explained in the coming section.
Turnover: Leaving the organization due to dismissal, attrition, and other reasons. These people will not be on the payroll during the next period.
Turnover rate: The percentage of Employees leaving in a given period of time.
How to calculate the employee turnover rate
The definition of ‘Employee’ may feel a bit unnecessary but is justified. Let me give an example to explain this.
At the start of a quarter, there were 100 employees. During this quarter, 5 employees left, and 10 joined. At the end of this period, there are 105 people working in the organization. Calculate turnover for this quarter.
The question now is, do we include everyone in our turnover rate denominator, or do we only include the existing employees (thereby excluding hires)?
This stresses the importance of making a clear distinction between Employees, Hires, and Terminations. These are three different groups with three different metrics. Hires are people who joined the company during the given period – and they should be treated as such as we have a separate set of metrics for them.
To illustrate this, hires are part of the hiring rate for the period. In case of early departure, they are included in a 90-day turnover metric, and in the 1st Year Turnover Rate. So, we should make a clear distinction between our hires and employees.
When we look back at our example, we see that we had 100 employees, five terminations, and ten hires. This means that the turnover in our example above is 5%, as five out of a hundred left the company.
This brings us to the turnover rate formula that we recommend for use.
 
This approach is in line with the description given in ISO 30414, a universal norm for Human Capital Reporting published in 2018, which takes the total number of leavers over a given period and divides it by the total number of people in the organization.
The annual turnover rate formula is then formulated as follows
 
Alternative approaches to calculating turnover
Although we recommend the turnover rate formula above, we do think it is useful to discuss a commonly discussed, alternative way of calculating employee turnover – one we do not agree with.
This approach is predominantly championed by ANSI and can also be found on multiple places on the internet. It proposes that the turnover rate equals the # Terminations divided by the average # of employees for each of the 12 months in the designated annual period.
 
This alternative turnover rate formula poses two problems. Let’s go over these one by one.
1. According to the ANSI definition, employees would include both existing employees and hires. It mixes both the hiring numbers and rates and the turnover numbers. This leads to an ‘impure’ calculation. Consider the following example that we set over a 3-month period of time for simplicity reasons.
 Months	January	February	March
Original Employee pool	100	90	80
Terminations per month	10	10	10
New Hires per month	20	20	20
Total employees	100	110	120

We see that every month 10 employees leave, while every month 20 new hires join. According to this alternative calculation, which would take the average number of employees as the denominator, there are 30 terminations and on average 110 employees: (100+110+120)/3. This makes the turnover rate 30/110 = 27%.
Our proposed method shows a different number. 30 Terminations / 100 Employees at the start of the period = 30%.
The difference is that the first formula is diluted by Hires. This is why we propose to split Hires and Employees into two distinct categories to come up with a purer number. As mentioned before, Hires have their own set of metrics, including 90-day turnover and 1st year turnover.
Once we are done with the turnover metric calculation, we can analyze the data. Usually this is done through some sort of multivariate statistical analysis to see if there is any strong cause-and-effect relationship between the predictors of turnover and the dependent variable.
Mixing hires and terminations in a rate calculation might muddy the interpretability. One potential way to deal with this might be to include a predictor which accounts for this factor but the importance of keeping the analysis in mind is true regardless.
2. Our second concern is that this alternative approach allows for a changing denominator within the calculation time period. This poses another problem. A simpler example to illustrate this.
 Months	January	February	March
Original Employee pool	100	90	80
Terminations per month	10	10	10

As you can see, every month, 10 people leave. The ANSI formula would propose to average the number of employees in the denominator, resulting in a turnover rate of
 
Our proposed method shows a different number. 30 Terminations / 100 Employees at the start of the period = 30%. The 3-month turnover rate is therefore 30%. This also makes sense as 30 out of a 100 people we started with left.
3. There is also a very practical side to this story. The data we are working with in these examples, will come from a data pool or data warehouse. The dashboards and reports that are created based on this input data, need to comply with the practicalities of the system and measurements.
First of all, most of us will want to slice and dice our data. When it comes to the changing denominator we discussed earlier, our metric should make sense at all levels of disaggregation. This means that the formula must render a meaningful calculation at the individual level as well. Take this example of a single employee quitting. The time period selected is a 2-month period.
 	January	February
Original Employee pool	1	0
Terminations per month	1	0

Here the alternative approach would come up with the following formula
In our dashboard or HR report, we don’t want to have a reported 200% turnover when we make such a specific selection. This will be impossible to explain to a business partner or line manager.
 
In addition, we report on both our existing population and on our recruits. This is another argument to separate Employees from Hires, as both have their dedicated dashboard.


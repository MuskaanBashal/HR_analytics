# HR_analytics
Analysis on the various factors affecting the attrition rate of the company.
## Problem Statement
This dashboard helps the company understand their employees better. It helps the company know if their employees are satisfied with their job role. Through different key areas, they get to know their improvement area, & thus they can improve their services by identifying these area. It also lets them know the average attrition rate in departments and job roles, thus since by using this dashboard they have identified this problem, they can further work on factors responsible for these high attrition rate.

Since, number of neutral/dissatisfied employees (almost 16.2 %), thus in all they must work on improving their services.

### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "EmpID", "Attrition", "Department" and "JobRole" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present except column named "YearsWithCurrManager".
- Step 5 : In the report view, under the view tab, theme was selected.
- Step 6 : Various visualization were created based on the "AgeGroup","Attrition","Department","EducationField","Gender", "SalarySlab" and "JobRole". 
- Step 7 : Visual filters (Slicers) were added for one field named "Department".
- Step 8 : Multiple KPIs(Key Performance Indicator) were created to provide crucial information such as Total Employees, Attrition number and rate, Average age of employees, Avereage monthly salary and Average years at the company.

Using visual level filter from the filters pane, basic filtering was used & null values were unselected for consideration into average calculation.
           
Although, by default, while calculating average, blank values are ignored.
- Step 9 : A bar chart was also added to the report design area representing the average age of employees in the company. While creating this visual, a new column was created to group the age into Age-Groups for better understanding.
  
In our dataset, Some parameters were assigned value 0, representing those parameters are not applicable for some employees.

All these values have been ignored while calculating average rating for each of the parameters mentioned above.

- Step 10 : In the report view, one text box was added to the canvas, where the heading of the dashboard is mentioned.
 
- Step 11 : Calculated column was created in which, employees were grouped into various age groups.

for creating new column following DAX expression was written;
       
        Age Group = 
        if(Age[Age]<=25, "18-25",

        if(Age[Age]<=35, "26-35",
        
        if(Age[Age]<=46, "36-46",
        
        if(Age[Age]<=55, "46-55 (75 included)",
        
        "55+")))
        
Snap of new calculated column ,
https://github.com/MuskaanBashal/HR_analytics/blob/f99ae6a472960a806ed1963916d57f177ae3e8db/Age-group.jpg

Observations

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

**Total Employees:** 1416 - The total number of employees in the organization.
**Attrition**: 229 - The total number of employees who have left the company.
**Attrition Rate**: 16.2% - The percentage of employees who have left the company.
**Average Age**: 37 - The average age of the employees.
**Average Monthly Salary**: 6.5K - The average monthly salary of the employees.
**Average Years at Company**: 7 - The average number of years employees stay at the company.

Following inferences can be drawn from the dashboard;
           
**Attrition by Education**
Life Sciences: 38% - The percentage of employees with a Life Sciences background who have left.
Medical: 25% - The percentage of employees with a Medical background who have left.
Technical Degree: 14% - The percentage of employees with a Technical Degree who have left.
Marketing: 13% - The percentage of employees with a Marketing background who have left.
Other: 5% - The percentage of employees with other educational backgrounds who have left.

**Attrition by Age**
26-35 years: 111 employees - The highest number of employees who left fall in this age group.
18-25 years: 43 employees
36-45 years: 41 employees
46-55 years: 26 employees
55+ years: 8 employees

**Attrition by Gender**
Male: 145 employees
Female: 84 employees

**Attrition by Job Role**
Sales Representative: 33 employees
Sales Executive: 55 employees
Research Scientist: 44 employees
Laboratory Technician: 60 employees
Human Resources: 12 employees

**Attrition by Departments**
Research & Development: 127 employees - The highest attrition is in this department.
Sales: 90 employees
Human Resources: 12 employees

**Attrition by Salary**
Up to 5k: 69% - The majority of attrition occurs among employees with a salary up to 5k.
5k-10k: 20.96%
10k-15k: 7.68%
15k+: The least attrition happens in this salary range.

**Attrition by Years at Company**
The highest attrition happens at the 1-year mark with 57 employees leaving.

**Useful Insights:**
**Insight 1: High Attrition Among 26-35 Year Olds**
Observation: The highest attrition is among employees aged 26-35 (111 employees).
Strategy:
Career Development: Implement more robust career development and advancement opportunities tailored for this age group, as they are likely seeking growth and progression in their careers.
Mentorship Programs: Establish mentorship programs where younger employees can be guided and supported by more experienced staff.
Work-Life Balance: Offer flexible working hours and remote work options to cater to their potential family and personal life needs.

**Insight 2: High Attrition in Research & Development Department**
Observation: The Research & Development department has the highest attrition (127 employees).
Strategy:
Job Satisfaction: Conduct surveys and focus groups to understand specific issues within this department, such as workload, job satisfaction, or management practices.
Professional Growth: Invest in continuous training and professional development programs to keep employees engaged and up-to-date with the latest industry trends.
Recognition and Rewards: Implement recognition and reward systems to appreciate the hard work and achievements of the employees in this department.

**Insight 3: Attrition by Education**
Observation: Employees with a Life Sciences background have the highest attrition (38%).
Strategy:
Targeted Engagement: Develop engagement programs specifically for employees with a Life Sciences background, focusing on their career aspirations and professional growth.
Tailored Development Programs: Offer specialized training and development programs to ensure they see a clear path to growth within the company.

**Insight 4: Attrition by Salary**
Observation: The majority of attrition is among employees earning up to 5k (69%).
Strategy:
Competitive Compensation: Review and adjust compensation packages to ensure they are competitive within the industry.
Benefits and Perks: Enhance non-monetary benefits such as health insurance, wellness programs, and other perks that can improve job satisfaction.
Performance Bonuses: Introduce performance-based bonuses and incentives to reward and retain high-performing employees.

**Insight 5: High Attrition Among Sales Executives and Laboratory Technicians**
Observation: High attrition among Sales Executives (55) and Laboratory Technicians (60).
Strategy:
Sales Executives:
Training and Support: Provide continuous sales training and adequate support to help them meet their targets and reduce job stress.
Clear Career Path: Define clear career progression paths to motivate and retain them.
Laboratory Technicians:
Work Environment: Improve the work environment by ensuring adequate resources and reducing work-related stress.
Job Security: Enhance job security by offering long-term contracts or permanent positions.

**Insight 6: Gender-Specific Attrition**
Observation: Higher attrition among male employees (145) compared to female employees (84).
Strategy:
Inclusive Policies: Develop policies and practices that support both genders equally, such as parental leave, flexible working arrangements, and gender diversity programs.
Focus Groups: Conduct focus groups to understand the specific needs and challenges faced by male employees and address them appropriately.

**Insight 7: Early Tenure Attrition**
Observation: High attrition at the 1-year mark (57 employees).
Strategy:
Onboarding Programs: Enhance the onboarding process to ensure new hires are well-integrated and supported during their first year.
Probation Reviews: Implement regular check-ins and performance reviews during the first year to address any issues early on.
Buddy System: Introduce a buddy system where new employees are paired with experienced staff to help them acclimate to the company culture and processes.


By addressing these insights with targeted strategies, the company can improve employee retention, reduce attrition rates, and create a more engaged and satisfied workforce.


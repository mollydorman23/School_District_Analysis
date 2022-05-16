# School_District_Analysis

## Analysis Overview:
The purpose of this project is to review standardized test performance data, for high schools within a specific school district, in order to highlight the following information:
* Top 5 and bottom 5 performing schools, based on the overall passing rate
* The average math score received by students in each grade level at each school
* The average reading score received by students in each grade level at each school
* School performance based on the budget per student
* School performance based on the school size 
* School performance based on the type of school

After we completed our initial analysis of the data, we got additional information that the scores for 9th graders at one specific high school (Thomas High School [THS]) were likely inaccurate and needed to be omitted in order to re-run the analysis and preserve the integrity of our conclusions.
- - - -
## Results:

Overall, since this data set is so large, removing reading and math scores for 9th graders at one of the 15 high schools did not significantly impact the aggregate data, but it had a large impact on the Thomas High School data.

### How is the district summary affected?

The disctrict summary test scores very slightly decreased when we removed the THS 9th grade scores. See the original data below:
<img width="936" alt="OG District Summary" src="https://user-images.githubusercontent.com/103781847/168492790-3b595086-13a7-43fb-8b0e-1a219c37abcc.png">

And here is the adjusted data:
<img width="950" alt="New District Summary" src="https://user-images.githubusercontent.com/103781847/168492830-e3f82186-1cdb-4dfa-b10c-530eb7bf68cb.png">

### How is the school summary affected?

The school summary for Thomas High School was significantly impacted by removing the 9th grade test scores. We saw their overall passing rate drop by about 26 points. See the original school summary followed by the adjusted summary:
<img width="998" alt="OG Just THS" src="https://user-images.githubusercontent.com/103781847/168492958-b5cc17bf-185b-4ec6-aa31-93317900f4a5.png">

<img width="1010" alt="NEW Just THS" src="https://user-images.githubusercontent.com/103781847/168492963-41a1363b-c0ae-4c6f-ab31-b73926903aad.png">

### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?

In the original analysis, THS was the 2nd ranked school based on their overall passing rate. By removing THS scores for 9th graders, they drop to the 8th spot overall.
<img width="1000" alt="OG Overall Passing Rankings" src="https://user-images.githubusercontent.com/103781847/168493514-cd98ef15-4f81-4808-a02e-949655bea799.png">

VS the adjusted analysis:
<img width="997" alt="NEW Overall Passing Rankings" src="https://user-images.githubusercontent.com/103781847/168493529-af3a45f1-8efa-4073-ae2c-27f6147eed3c.png">

### How does replacing the ninth-grade scores affect the following:

#### 1. Math and reading scores by grade: 

Now we see “nan” as the value for 9th grade math and reading scores from THS, instead of the original values of 83.6% (math) and 83.7% (reading). See the updated Math and Reading data frames by grade below:

Math Scores:

<img width="760" alt="NEW Math scores by grade" src="https://user-images.githubusercontent.com/103781847/168493632-f5f264ab-571a-46ea-b660-0d4115c0fffa.png">

Reading Scores:

<img width="835" alt="NEW Reading scores by grade" src="https://user-images.githubusercontent.com/103781847/168493651-0919aab3-2a3b-4b96-b5d6-c78f0946b634.png">

#### 2. Scores by school spending: 

We really only see a change in the spending bucket that THS falls into ($631-$645), since that is the only bucket that had scores removed.

Original Scores:

<img width="837" alt="OG Spending Ranges" src="https://user-images.githubusercontent.com/103781847/168493755-820d0cb6-3e65-43f2-8de3-df409697f869.png">

Adjusted Scores:

<img width="812" alt="New Spending Ranges" src="https://user-images.githubusercontent.com/103781847/168493794-4ecbec96-7e49-4302-96d5-deec297265b4.png">

#### 2. Scores by school size: 

There is a very small difference in scores by school size for Medium schools with the THS 9th graders backed out:

Original data:

<img width="758" alt="OG Scores by size" src="https://user-images.githubusercontent.com/103781847/168494254-719278c9-9a03-400f-84d5-d726c5fde047.png">

Adjusted data:

<img width="773" alt="NEW NEW Scores by size" src="https://user-images.githubusercontent.com/103781847/168494840-6d88b02c-7e24-490e-8bb2-688203d2fb62.png">

#### 2. Scores by school type: 

Similarly to the previous observation, there is a very small difference in scores by school type for charter schools with the THS 9th graders backed out:

Original data:

<img width="718" alt="OG Type Summary" src="https://user-images.githubusercontent.com/103781847/168495023-e23ecc13-6956-4cc3-ba44-eb0f4236f85f.png">

Adjusted data:

<img width="712" alt="NEW NEW Type Summary" src="https://user-images.githubusercontent.com/103781847/168495057-479ab372-8b51-492d-80b9-3b40d3412da6.png">

- - - -

## Summary: 

Below, I've summarized four changes in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs:

1. There was a very  slight decrease in the overall passing percentage for the district after removing scores for the THS 9th graders; the passing percentage decreased from 65.17% to 64.86%.
2. There was a dramatic decrease in the overall passing percentage for THS students; the passing percentage dropped from 90.95% to 65.08%.
3. THS dropped from #2 for their overall passing percentage to #8 out of 15 total high schools.
4. There was only slight movement when we looked at the test scores by per capita spending, size and type, and only for the buckets that THS fell into, since those were the only scores that had any changes made to them. For example, in the $631-645 per capita spending bucket, which is the spending range that THS lives in, the overall passing percentage decreased from 62.86% to 62.78%.

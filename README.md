# School_District_Analysis

### Project Overview 

This project was to clean standardized test data and student school funding data then analyze it to allow insights to be drawn from the showcasing of trends amongst the school data. Two list's in csv format were provided with school data and student exam data. The data was cleaned and sorted into one larger data frame which led to further related charts.

The data was sorted and analyzed using a python 3.7 environment on jupyter notebook as well as using pandas.

* The first chart provided the general district summary

* The second chart provided Data for each school amongst all their grades 

* The third and fourth charts visualize the highest and lowest performing schools

* The fifth and sixths charts were for the average math and reading scores for each school amongst their different grades

*The seventh chart displayed student standardized test scores based on the range of which funding per student fell into

*The last two charts also display test score averages based on school size and type of school

### Challenge

The project came with a challenge, where with suspicion of academic dishonesty test grades for the ninth graders of Thomas High School their grades had to be replaced with NaN values, and analysis had to be redone from there.

student_data_df.loc[(student_data_df["school_name"] == "Thomas High School") 
                    & (student_data_df["grade"] == "9th"),"reading_score"] = np.nan

This is a snippet of the code displaying the change of the 9th grader grades to NaN for those of Thomas High School, the code for changing math was very similar.

This causes some changes in the overall summary which have to be accounted for. 

* The district summary loses 461 total students in its count and all average test values have dropped with the passing rates slightly falling as well.

*The per school summary is only slightly affected as well. 

*Putting NaN values in place of the ninth graders scores originally largely affected Thomas High School dropping their average scores and passing rates significantly, to adjust for so the average scores of the 10th to 12th graders were isolated and used as representation for the whole school.

Before NaN 

![image](https://user-images.githubusercontent.com/85713568/136753522-c83729be-bc45-465c-92a9-9d9ce51b41ba.png)


After NaN

![image](https://user-images.githubusercontent.com/85713568/136753618-727557f2-e82f-4993-8a0a-1e6343703772.png)

Thomas High School adjusted values 

![image](https://user-images.githubusercontent.com/85713568/136753664-cf5593d5-ffbe-496d-9786-1a7080642dbc.png)



* the adjustment for NaN values in the ninth grade left Thomas High School to have a NaN value for their 9th grade math and reading scores. 

* Scores by school spending were not drastically change as well as scores by school size and scores by school type.


### Summary 

In the analysis when the grades were first changed to NaN for the ninth graders of Thomas High School

* The % Passing Math fell from 93.27% to 66.9% 
* The % Passing Reading fell from 97.3% to 69.66%  
* The % Overall Passing fell from 91% to 65.1% 
* It can be seen that these values dramatically fell when NaN values were replaced for the ninth grader scores as it reduced the arithmetic means. Until adjustments replacing averages including the ninth grade were filtered out. 

Overall by % overall passing in the school district the top 5 schools were all charter types while the bottom 5 were all district type. Although the charter schools did not have as much average spending per student they were able to push out better student test results. The top 5 schools stood around the Small to Medium School size range while the bottom 5 schools were all large sized schools. Perhaps there may be a deeper correlation between school size and resources available that are not directly affected by the budget which may be something to look further into.


 



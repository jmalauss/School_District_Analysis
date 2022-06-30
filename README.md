# School_District_Analysis

## Overview of the school district analysis
### Purpose

This analysis was performed because the school board suspected academic dishonesty regarding the math and reading scores from ninth-grade, Thomas High School students. The state testing standards warrant the removal of those scores, so Maria asked for our help to replace the scores with new scores calculated by removing the scores from the cohort suspected of academic dishonesty. In other words, we were asked to remove the suspicious scores, repeat the analysis, and address how the changes impacted the analysis. 

## Results
### How is the district summary affected?

The image below demonstrates the change in scores before and after the removal of the THS ninth graders. 

![old_and_replacement_scores](https://github.com/jmalauss/School_District_Analysis/blob/main/Module_4_Challenge_Snips/old_and_replacement_scores.png)

You can see that the scores for Math, Reading and Overall increased. 

### How is the school summary affected?

Before removing the grades of the THS ninth graders, the scores for THS were the following:

![school_summary_before](https://github.com/jmalauss/School_District_Analysis/blob/main/Module_4_Challenge_Snips/school_summary_before.png)

After:

![school_summary_after](https://github.com/jmalauss/School_District_Analysis/blob/main/Module_4_Challenge_Snips/school_summary_after.png)


### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?

Below is the code used to sort the school summary by % Overall Passing. By passing the second line, we are able to see that the adjustment to the scores moved THS into the top 5 performing schools.

```
top_schools = per_school_summary_df.sort_values(['% Overall Passing'], ascending = False)
top_schools.head(5)
```

![thomas_performance_relative_other_schools](https://github.com/jmalauss/School_District_Analysis/blob/main/Module_4_Challenge_Snips/thomas_performance_relative_other_schools.png)


## How does replacing the ninth-grade scores affect the following:
### Math and reading scores by grade

The Percentage of Passing (Math, Reading and Overall) scores increase for ninth graders across all scores when the THS ninth grade scores are removed.

![math_reading_by_grade](https://github.com/jmalauss/School_District_Analysis/blob/main/Module_4_Challenge_Snips/math_reading_by_grade.png)

### Scores by school spending

The spending per student for THS was unchanged after removing the scores of the ninth graders:

![scores_by_spending](https://github.com/jmalauss/School_District_Analysis/blob/main/Module_4_Challenge_Snips/scores_by_spending.png)

### Scores by school size

The size of THS was unchanged after removing the scores of the ninth graders:

![scores_by_size](https://github.com/jmalauss/School_District_Analysis/blob/main/Module_4_Challenge_Snips/scores_by_size.png)

### Scores by school type

Since THS is a Charter school, the % Passing Math, % Passing Reading and % Overall Passing increased with the removal of the THS ninth grade scores. In other words, the percentages for the columns listed above increased for Charter-type schools. 

![scores_by_type](https://github.com/jmalauss/School_District_Analysis/blob/main/Module_4_Challenge_Snips/scores_by_type.png)

## Summary

Changes to the school district analysis after reading and math scores were replaced:

1. Percentages of Passing (Math, Reading and Overall) scores increased at THS
2. Percentages of Passing (Math, Reading and Overall) scores increased for Charter school types
3. THS is considered one of the top performing schools when we remove the ninth grade scores.
4. The Percentage of Passing (Math, Reading and Overall) scores increase for ninth graders across all scores when the THS ninth grade scores are removed.

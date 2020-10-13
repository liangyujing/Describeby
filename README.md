# Some preliminary descriptives for correct and incorrectly solved trials
describeBy(experimental_df$confidence, group=experimental_df$solution_type,mat=FALSE,type=3)
describeBy(experimental_df$RT, group=experimental_df$solution_type,mat=FALSE,type=3)
describeBy(experimental_df$ACC, group=experimental_df$solution_type,mat=FALSE,type=3)

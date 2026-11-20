TASK_09: Eigenvalues and Eigenvectors 
MODIFIED
REAL-WORLD CASE

Problem:
A university wants to analyse students' academic performance across different subjects, such as Mathematics, Programming, Physics and Statistics. The university wants to identify the main patterns in students' performance and determine which combination of subjects contributes most to overall academic variation.

Solution approach:
Represent students' marks in a numerical data matrix.
Calculate the mean mark for each subject.
Centre the data by subtracting the mean marks.
Calculate the covariance matrix.
Compute the eigenvalues and eigenvectors using NumPy.
Identify the dominant eigenvalue and its corresponding eigenvector.
Calculate the percentage of variation explained by the dominant eigenvalue.
Interpret the results to understand the patterns in students' academic performance.

ASSUMPTIONS:

The following assumptions are made in this project:

-The dataset contains marks for eight students.
-Each student has marks in four subjects: Mathematics, Programming, Physics and Statistics.
-All marks are numerical and measured on the same scale, from 0 to 100.
-Each subject is treated as a separate variable.
-The sample marks are assumed to be accurate for demonstration purposes.
-The covariance matrix is used to examine how marks in different subjects vary together.
-The eigenvector associated with the largest eigenvalue represents the principal direction of variation.
-The dataset is only for demonstration and does not represent actual university examination records.

INPUT DATA:

Student    Mathematics   Programming   Physics  Statistics
1            80              85          75         82
2            70              75          65         72
3            90              95          85         92
4            60              65          55         62
5            85              88          80         86
6            75              78          70         76
7            95              98          90         96
8            65              68          60         66


The input data is stored in a NumPy array, where each row represents a student and each column represents a subject.

PROGRAM OUTPUT:

STUDENT PERFORMANCE ANALYSIS
Mean Marks:
Mathematics: 77.50
Programming: 81.50
Physics: 72.50
Statistics: 79.00

Covariance Matrix:
[[150.   147.14 150.   148.57]
 [147.14 145.43 147.14 146.29]
 [150.   147.14 150.   148.57]
 [148.57 146.29 148.57 147.43]]

Eigenvalues:
[592.0989   0.7583   0.      -0.    ]

Dominant Eigenvalue:
592.0989

Dominant Eigenvector:
Mathematics: -0.5031
Programming: -0.4949
Physics: -0.5031
Statistics: -0.4990

Percentage of Variation Explained:
99.87%

Verification Error:
0.0000000000

INTERPRETATION OF RESULTS

The results show that the largest eigenvalue is approximately 592.0989. This means that the first principal component explains approximately 99.87% of the total variation in the students' academic performance.

The dominant eigenvector shows the contribution of each subject to this principal direction.

The absolute values of the eigenvector components are approximately equal. This suggests that Mathematics, Programming, Physics and Statistics contribute almost equally to the main pattern of variation in this particular dataset.

The small verification error confirms that the calculated eigenvalue and eigenvector satisfy the eigenvalue equation:

Av = λv
where:
A represents the covariance matrix.
v represents the eigenvector.
λ represents the eigenvalue.
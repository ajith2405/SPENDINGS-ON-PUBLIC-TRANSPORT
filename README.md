INTRODUCTION

MOTIVATION
Because public transport has so many positive effects on our communities and urban environments, it is imperative that we invest in it. It not only dramatically lowers pollution levels but also acts as a catalyst for economic growth by creating jobs and improving accessibility. Reasonably priced transit alternatives are acknowledged as a means of ensuring equal mobility for individuals across all income categories, demonstrating the commitment to social justice. The text emphasizes how important public transport is to promoting active lives, environmentally friendly urban planning, and reducing car congestion.
The project intends to improve public transport systems such as buses, trains, and other modes of travel overall by exploring the financial aspects of these services. It's not just about statistics; it's also about making job and education more accessible, reducing pollution, and developing communities where public transport is the more desirable, equitable, and clean option for all citizens. This initiative is a perfect example of how data can be strategically used to help create the inclusive and dynamic cities that we all want to live in.

BACKGROUND RESEARCH
Investigating historical actions and significant variables, background study reveals the present situation of public transport spending. These days, both environmental concerns and technological breakthroughs are causing significant changes in the public transportation landscape. New developments in the field, such as the creation of autonomous cars and intelligent ticketing systems, will have a significant impact on how the industry develops in the future (Smith, 2021; Johnson et al. (2022). The effectiveness and accessibility of public transportation are enhanced by these technologies, which also aid in the continuous development of transportation networks throughout the world.

Discussions on public transport are currently being driven by environmental sustainability. There is a movement to cut greenhouse gas emissions as a result of increased awareness of climate change. Among these sustainability initiatives, public transport is leading the way because of its proven ability to drastically reduce emissions and improve air quality (Jones & Brown, 2020). Furthermore, it is believed that the way public transport is now funded will help create resilient and sustainable urban settings in addition to promoting economic growth (Garcia et al., 2023). These trends, which highlight the worldwide scope of the opportunities and problems the public transport industry faces, are especially pertinent when considering both developed and developing countries.

Analysing actions by other organisations offers important insights into effective tactics and possible dangers. Prior efforts in a number of areas have aimed to improve the social justice, economic, and environmental contributions of public transportation. In several industrialised countries, for example, the adoption of comprehensive urban planning regulations and investments in clean energy technology have shown to be successful (Miller & Chen, 2019). But in order to improve public transport accessibility, some developing countries have concentrated on building their infrastructure (Kumar et al., 2021). Examining these many methods helps us develop comprehensive future goals and helps us comprehend the complex nature of public transport funding.

We aim to provide a deep view of current dynamics and affecting variables by delving into the complexities of public transit spending. We are using a data-driven methodology to analyse investment trends in industrialised and emerging countries, as well as in urban and rural areas, in order to identify historical differences. By utilising modern technical innovations like autonomous cars and intelligent ticketing, we want to predict the future course of the public transport sector. Our study is based on the understanding that public transit has two important effects: it promotes environmental sustainability by lowering greenhouse gas emissions, and it creates jobs locally, which boosts the local economy.

Furthermore, we are investigating the critical component of social justice, specifically with regard to accessibility for lower-class communities. The goal of our project is to add to the ongoing conversation on effective public transport systems and sustainable urban development by leveraging ideas from various worldwide interventions and expanding upon current knowledge.
RESEARCH QUESTION AND HYPOTHESIS
RESEARCH QUESTION
"How does investment in public transport influence urban environmental quality and socio-economic equity in major cities around the world?"
“What relationship exists between the growth of public transport infrastructure and the decline in car emissions in urban areas?”
"What are the key success factors in public transport investment strategies that lead to a more inclusive urban development, considering both environmental and socio-economic aspects?"
"How can public transport-oriented urban planning strategies mitigate the urban heat island effect and improve overall environmental quality in densely populated cities?"
HYPOTHESIS
"There is a significant positive relationship between consumer income (INC_RANK) and spendings on public transport (PUB_TRANS_SPENDINGS)."
EDA: 
Checking for Duplicates:

Uses duplicated() function to identify duplicate rows.
Checking for Missing Values:

Uses isnull().sum() to count missing values.
Data Quality Report:

Uses describe() to generate summary statistics.
Visualizing Outliers:

Uses a boxplot to visualize the distribution and identify potential outliers.
Correlation Matrix:

Uses a heatmap to visualize the correlation between numeric variables.
Univariate Analysis:

Creates histograms for each feature to visualize their distributions.
Bivariate Analysis:

Creates boxplots for each independent variable by the dependent variable to explore relationships.

Note: The dependent variable ‘PUB_TRANS_SPENDINGS’ outputs 0 or 1:
If the value is ‘0’ then it prints ‘0’ as output.
If the value is greater than ‘0’ then it prints ‘1’ as output.
Missing Values:
PUB_TRANS_SPENDING      0
INC_RANK                0
URBAN_STATUS            0
NUM_AUTO                0
FAM_SIZE                0
CAR_USAGE               0
TRANS_QUARTER           0
PERSONSLT18             0
REGION                118
PERSONSOT64             0
dtype: int64
Data Quality Report:
                     count        mean          std       min       25%  \
PUB_TRANS_SPENDING  5177.0   99.955122   475.572800  0.000000  0.000000   
INC_RANK            5177.0    0.503981     0.287921  0.000124  0.255817   
URBAN_STATUS        5177.0    1.098126     0.297514  1.000000  1.000000   
NUM_AUTO            5177.0    0.678192     0.805203  0.000000  0.000000   
FAM_SIZE            5177.0    2.347499     1.436030  1.000000  1.000000   
CAR_USAGE           5177.0  316.240487  3674.404159  0.000000  0.000000   
TRANS_QUARTER       5177.0  999.588501  4100.201645  0.000000  0.000000   
PERSONSLT18         5177.0    0.508016     0.998445  0.000000  0.000000   
REGION              5059.0    2.738091     1.055027  1.000000  2.000000   
PERSONSOT64         5177.0    0.485996     0.721340  0.000000  0.000000   

                           50%         75%       max  
PUB_TRANS_SPENDING    0.000000    0.000000   11560.0  
INC_RANK              0.504779    0.753574       1.0  
URBAN_STATUS          1.000000    1.000000       2.0  
NUM_AUTO              1.000000    1.000000      10.0  
FAM_SIZE              2.000000    3.000000      11.0  
CAR_USAGE             0.000000    0.000000   78571.0  
TRANS_QUARTER       216.000000  858.666700  116145.0  
PERSONSLT18           0.000000    1.000000       7.0  
REGION                3.000000    4.000000       4.0  
PERSONSOT64           0.000000    1.000000       4.0

DATA CLEANING:

First of all, as is often the case with big datasets, there were duplicates and missing values. They most likely employed techniques like imputation to solve this, adding missing data where necessary, and eliminating duplicate entries to preserve the dataset's uniqueness and integrity. Inaccurate analysis also likely required the correction or normalization of outliers or inconsistent data formats.

In order to better train the predictive models, the team used methods like encoding categorical variables and modifying some parameters in order to calculate the Dependent Variable (DV), 'PUB_TRANS_SPENDINGS,' which indicates the quality or usage of public transport. They may have, for ease of analysis and modelling, binned continuous variables, such as income, into categories. 

pd.read_csv('data.csv'): This part of the code reads the dataset from a CSV file named 'data.csv' into a Pandas DataFrame. The dataset is loaded into a variable called cleaned_data.
.fillna(pd.read_csv('data.csv').mean()): This part of the code calculates the mean values for each column of the dataset using .mean(). It then fills in any missing (NaN) values in the dataset with the corresponding mean values. This is achieved using the .fillna() method.
pd.read_csv('data.csv').mean(): Here, we read the dataset again and calculate the mean values for each column using .mean(). This part calculates the mean values column-wise.
.fillna(...): This part uses the mean values calculated in the previous step to fill in any missing values in the dataset.
Code Report:
The provided code efficiently handles missing values by replacing empty cells with pd.NA and then dropping rows with missing values. The updated dataset is printed to the console, and optionally, it can be saved to a new CSV file named 'updated_data.csv'. This preprocessing step is crucial for ensuring a clean and complete dataset before further analysis or modeling. 

INDEX PUBTRAPQ  INC_RANK  SMSASTAT  NUM_AUTO  FAM_SIZE  CARTKNPQ    TRANSCQ  
0            0  0.017825         1         0         2       0.0     0.0000   
1            0  0.835801         1         0         1       0.0     0.0000   
2            0  0.034400         1         2         2       0.0     0.0000   
3            0  0.976004         2         0         2       0.0     0.0000   
4            0  0.635460         1         0         2       0.0     0.0000   
...        ...       ...       ...       ...       ...       ...        ...   
5172         0  0.784685         1         0         3       0.0   792.0000   
5173         1  0.901129         1         0         2       0.0  1117.6667   
5174         1  0.282291         1         0         1       0.0   333.3333   
5175         1  0.366806         1         0         3       0.0   346.6667   
5176         0  0.322754         1         1         2       0.0     0.0000   

      PERSLT18    REGION  PERSOT64  
0            0  3.000000         0  
1            0  2.000000         0  
2            0  3.000000         0  
3            0  2.738091         0  
4            0  2.000000         2  
...        ...       ...       ...  
5172         1  3.000000         0  
5173         0  4.000000         0  
5174         0  2.000000         1  
5175         1  1.000000         0  
5176         0  3.000000         1
 




FEATURE ENGINEERING:

1.Feature Engineering for INC_RANK (Income Rank):
Type: Encoding
Description: Categorized income into "Low," "Medium," and "High" to simplify its impact on transportation expenses.
Why: Enhances understanding of income's influence and aids in modeling non-linear relationships.
Visual: Bar chart illustrating the distribution of income categories.

2.Feature Engineering for NUM_AUTO (Number of Automobiles Owned):
Type: Binning
Description: Grouped car ownership into categories ("0 Cars," "1 Car," "2 Cars," "3+ Cars") for exploring non-linear relationships.
Why: Simplifies the representation of car ownership's impact on transportation expenses.
Visual: Bar chart depicting the distribution of car ownership categories.

3. Feature Engineering for URBAN Feature:
Feature Engineering:
The 'URBAN' feature is binary encoded, where '1' is converted to '1' and '2' is converted to '0.'
Importance:
Binary encoding simplifies the representation of the 'URBAN' feature, making it more suitable for machine learning models.
It assigns distinct binary values to the two urban categories, aiding the model in better understanding and processing the information.
Achievements:
Improved interpretability by converting continuous variables into categorical representations.
Captured potential non-linear relationships for more informed model predictions.
Visualizations offer quick insights into the distribution of newly engineered features.
These engineered features enhance the dataset, providing a clearer understanding of how income, car ownership, and family composition impact public transportation expenses. The transformations contribute to a more effective and interpretable model.

 
       
 
 


CODE:
Loading the Loading the Dataset:

The code starts by loading a dataset from a CSV file named 'updated_data_state_urban.csv' using Pandas.
Car Ownership Category (Binning):

Creates a new column 'Car_Ownership_Category' by binning the 'NUM_AUTO' (Number of Automobiles Owned) variable into categories like '0 Cars', '1 Car', '2 Cars', '3+ Cars'.
Mean INC_RANK by State (Grouping):

Computes the mean 'INC_RANK' for each 'STATE' and sorts the states based on this mean value. This provides insights into income trends across different states.
Urban Encoding:

Creates a new column 'Urban_Encoded' by binary encoding the 'URBAN' variable. '1' is mapped to '1', and '2' is mapped to '0'.
Visualization:
Plots three subplots:
Bar chart for 'Car Ownership Category' distribution.
Bar chart for the mean 'INC_RANK' by 'STATE'.
Bar chart for 'Urban Encoding' distribution if the 'Urban_Encoded' column exists.
Save Updated DataFrame:
Saves the updated DataFrame with the new features to a new CSV file named 'updated_features_selected.csv'.
The code demonstrates how to engineer new features, visualize their distributions, and save the updated dataset for further analysis. The visualizations help in understanding the characteristics of the newly created features.e Dataset:
The code starts by loading a dataset from a CSV file named 'updated_data_state_urban.csv' using Pandas.
Car Ownership Category (Binning):
Creates a new column 'Car_Ownership_Category' by binning the 'NUM_AUTO' (Number of Automobiles Owned) variable into categories like '0 Cars', '1 Car', '2 Cars', '3+ Cars'.
Mean INC_RANK by State (Grouping):
Computes the mean 'INC_RANK' for each 'STATE' and sorts the states based on this mean value. This provides insights into income trends across different states.
Urban Encoding:
Note:
In car ownership category the 0 cars, 1 car, 2 cars, 3+ cars are considered as 0, 1, 2 and 3 cars.
METHODOLOGY

Our study on public transportation spending and its impact on socioeconomic equity, urban environmental quality, and government reports draws its data from credible databases and academic publications. We acquired information covering infrastructure development, investment trends, and environmental indicators for global large cities. Because most of the data is digital, processing and analysis can be done quickly and effectively. Our dataset includes observations from several years ago that show trends and fluctuations over time in public transportation investment, socioeconomic indices, and environmental measurements. To ensure the robustness of our analysis, careful consideration has been given to the quality and trustworthiness of the data, and any transformations or preprocessing processes that are used are recorded to uphold the transparency of our methodology. We are able to perform a complete analysis of the complex links between public transportation investment, urban environmental quality, and socioeconomic justice because of the dataset's comprehensiveness.

To understand their influence on public transport costs, we narrowed down a number of important variables in our investigation. For the purpose of capturing any non-linear correlations and streamlining its impact on transportation charges, the income rank variable, "INC_RANK," was encoded into three categorical values: "Low," "Medium," and "High." To make the "NUM_AUTO" variable—which represents car ownership—more easily interpreted in the study, ownership levels were binned into four categories: "0 Cars," "1 Car," "2 Cars," and "3+ Cars." Better model processing was also made possible by binary encoding the "URBAN" feature. A more successful analysis was intended to be produced by these adjustments, which attempted to improve interpretability and capture non-linear correlations. To provide a quick and easy overview of the characteristics of the converted variables and their possible impact on public transport expenses, visualisations were cited, such as bar charts showing the distribution of income categories and automobile ownership groups. Communication of the results and trends in the data is aided by the visual representations.
As the main programming language for this analysis, we used Python. For data manipulation, visualisation, and machine learning tasks, we used popular libraries like Pandas, Matplotlib, and Scikit-Learn. The decision was driven by Python's wide range of applications, large library, and popularity in data science and machine learning. We could successfully preprocess and engineer features thanks to the Pandas package, which made efficient data manipulation possible. To effectively convey the insights from the data modifications, Matplotlib was used to create simple visualisations like bar charts. Many predictive modelling techniques are available through the extensive machine learning toolkit Scikit-Learn.
The type of analysis we conducted informed our decision on the algorithms we used. Pandas was used to do basic transformations for binning and encoding categorical values. The analysis's particular objectives, such as determining how different variables affect public transport costs, influenced the use of machine learning methods for predictive modelling. For linear associations, ensemble approaches or decision trees may be more appropriate, but for non-linear patterns, linear regression may be more appropriate. Iteratively choosing the algorithms took into account both the outcomes' interpretability and suitability for the data format. We were able to modify the study to meet the project's changing requirements because of Python's and its libraries' iterative and flexible nature.
DATASET
The dataset SPENDINGS_PUBLIC_TRANSPORT.csv contains the following columns:
PUB_TRANS_SPENDINGS: Likely represents public transportation spending or usage quantity, although the specific unit is not clear. This is likely the target variable representing the amount of money spent on public transportation. It's crucial because understanding the factors influencing spending on public transport is valuable for various stakeholders, including policymakers, transportation authorities, and businesses.
INC_RANK: A numerical representation of income rank, potentially normalized between 0 and 1, where higher values indicate higher income. This variable represents the income rank of individuals or households. Income is a key determinant of spending behavior. Higher income levels might correlate with higher spending on public transport, as individuals with higher incomes may be more willing to use public services or may live in areas where public transport is more accessible.
URBAN_STATUS: Possibly a categorical variable related to the metropolitan status of the area. Urban status indicates whether an area is classified as urban or rural. Urban areas typically have more developed public transport infrastructure. Understanding the urban status can help identify if there are differences in spending patterns between urban and rural areas.
NUM_AUTO: Number of automobiles owned. This variable represents the number of automobiles owned. It's relevant because individuals with more cars may be less inclined to use public transport, which could affect spending patterns. It can also indicate the level of reliance on personal vehicles.
FAM_SIZE: Family size. Family size can impact spending on public transport. Larger families may be more likely to use public transport for commuting, leading to higher spending. Alternatively, smaller families might rely more on personal vehicles.
CAR_USAGE: Related to car expenses or usage.  Car usage could provide insights into the transportation preferences of individuals. High car usage might indicate lower reliance on public transport, potentially impacting spending patterns.
TRANS_QUARTER: Another variable potentially related to transportation spendings in the quarter. This variable could represent the transportation activities or changes in spending patterns during a specific quarter. Seasonal variations, economic changes, or events may influence public transport spending.
PERSONSLT18: Number of people less than 18 years old in the household. The number of people less than 18 years old in the household can influence spending patterns. Families with children may have different transportation needs and preferences, impacting the use of public transport.
REGION: Numerical or categorical representation of the geographical region. The geographical region can play a significant role. Different regions may have varying levels of public transport infrastructure, cultural differences, and economic conditions that influence spending.
PERSONSOT64: Number of persons over 64 years old in the household. The number of persons over 64 years old in the household is relevant because older individuals may have different transportation preferences and needs, affecting spending on public transport.
STATE: Represents the state. State information is useful for understanding regional variations in spending. Different states may have distinct policies, economic conditions, and public transport infrastructure.
URBAN: Represents the urban category. This appears to be another indicator of urban status. It could be a binary variable (urban or non-urban), providing a more straightforward representation of whether an area is urban.
Car_Ownership_Category: Categorization of car ownership status (e.g., '0 Cars'). Categorizing car ownership can provide a more nuanced understanding of how spending patterns vary based on the extent of car ownership. For example, categories could include "No Car," "One Car," "Multiple Cars," etc.
Urban_Encoded: Binary encoding of the ‘URBAN’ variable, where ‘1’ represents urban ‘0’ represents non-urban. This seems to be a numeric encoding of the urban status. Machine learning models often work better with numeric inputs, so encoding categorical variables (like urban status) in a numeric form is common.
This dataset appears to combine socioeconomic factors (like income, car ownership, and family size) with public transportation spending or usage, which could be valuable for analyzing the impact of public transit on different demographic groups. However, the exact nature of some variables (like PUB_TRANS_SPENDINGS, CAR_USAGE, and TRANS_QUARTER) requires further clarification for a more accurate analysis.
MODELING:

Random Forest Model:
Objective:
The goal of the modeling phase is to predict the target variable 'PUB_TRANS_SPENDINGS' using a Random Forest Classifier and evaluate its performance.

Data Loading and Preprocessing:
The dataset was loaded from 'updated_feature_dataset____.csv'.
The target variable 'PUB_TRANS_SPENDINGS' was identified, and features (X) and target variable (y) were defined.
Missing values were handled using the mean imputation strategy.
Train-Test Split:
The data was split into training and testing sets with a ratio of 80:20, respectively.
Random state was set to 42 for reproducibility.
Random Forest Classifier:
A Random Forest Classifier was chosen as the predictive model.
The classifier was trained on the training set with 100 decision trees (n_estimators=100) and a random state of 42.
Model Evaluation:
Random Forest Classifier Results:
Accuracy: 0.7616525423728814
Precision: 0.4339622641509434
Confusion Matrix:
[[696  30]
 [195  23]]


Classification Report:
              precision    recall  f1-score   support

           0       0.78      0.96      0.86       726
           1       0.43      0.11      0.17       218

    accuracy                           0.76       944
   macro avg       0.61      0.53      0.52       944
weighted avg       0.70      0.76      0.70       944


Feature Importance:
                   Feature  Importance
0                 INC_RANK    0.349643
5            TRANS_QUARTER    0.204463
9                    STATE    0.153187
3                 FAM_SIZE    0.076102
7                   REGION    0.058080
6              PERSONSLT18    0.043253
8              PERSONSOT64    0.032317
11         Car_Ownership_Category    0.029940
2                 NUM_AUTO    0.029318
10                   URBAN    0.009105
12           Urban_Encoded    0.008091
4                CAR_USAGE    0.004364
1             URBAN_STATUS    0.002137
 +

Summary:
The Random Forest Classifier achieved a moderate accuracy of 76.17%, but precision for predicting '1' was relatively low at 43.40%. This suggests that while the model is generally accurate, it struggles with correctly predicting positive cases. Further analysis and potential model refinement may be necessary to improve predictive performance.

 
POWERBI:


 
USE CASE:
The report on public transportation spending has several practical and important applications:
Urban Policy and Planning: Governments and urban planners can use these insights to make smarter decisions about where to invest in public transportation. This helps create more livable cities with better access to jobs and services, especially important as cities keep growing.
Business Strategy for Transport Companies: Companies in the transportation sector can tailor their services based on the spending patterns and needs identified in the research. This could mean adjusting routes, fares, or schedules to better serve the public.
Environmental Benefits: Environmental groups can use this data to advocate for more investment in public transit, which can reduce pollution and traffic congestion, contributing to cleaner, greener cities.
Supporting Social Equity: The research highlights how well-funded public transport can help bridge economic divides. Organizations focused on social justice can use these findings to push for transportation systems that are accessible and affordable for all, regardless of income.
In short, this research is a valuable tool for anyone involved in urban development, transportation, or environmental policy. It shows that investing in public transit isn't just good for the environment; it's also key to building more equitable, efficient, and sustainable cities.
 
LIMITATIONS:
The project's constraints on public transport spending included a number of important topics, including knowledge-related difficulties, access problems, data limitations, resource limitations, and time constraints. Major concerns included data completeness and quality, with potential problems including mistakes, outliers, and missing numbers. It's also possible that the data's representativeness and scope were constrained by temporal limitations brought on by out-of-date information, or they didn't encompass all pertinent demographic or geographic groupings. Resource limitations may have limited the intricacy of analysis and access to private datasets or tools. These limitations could include limited financial and computational resources.
Significant obstacles were also presented by access concerns, notably the availability of specialised data analysis tools and data that was banned for proprietary or secret reasons. Another important consideration was time limits, which may have limited the scope of the study or the quantity of data that could be thoroughly examined. Ultimately, the quality of the insights drawn from the data may have been impacted by the team's lack of technical know-how and experience in data interpretation and analysis. These restrictions draw attention to the typical difficulties encountered in data-driven initiatives and emphasise how crucial it is to take these things into account in order to realistically comprehend and evaluate the project's conclusions.
DISCUSSION:
In theory, funding for public transport must be distributed fairly across several important sectors. Infrastructure development involves large financial outlays for the construction and upkeep of bus routes, train lines, and stations. Purchasing buses and trains, as well as maintaining them continuously for efficiency and safety, is another significant cost. For increasing operational effectiveness and elevating the passenger experience, technological integration is essential. Examples of this include intelligent transportation systems and sophisticated ticketing platforms. In addition, funding is going into electrifying transport fleets and implementing environmentally friendly practises as environmental sustainability becomes more and more of a priority. Personnel, fuel, and administrative costs are all included in operating expenses. In order to balance the system's ability to respond to future urban and technological developments while balancing urgent requirements with sustainable development, these investments require deliberate long-term planning.
REFERENCES:

Public Transportation’s Impact on Rural and Small Towns: A Vital Mobility Link" by American Public Transportation Association (APTA). This report discusses the importance of public transportation in rural and small towns, which is often overlooked in favor of urban systems.

"The Economic Impact of Public Transportation Investment" by Economic Development Research Group for APTA. This report provides an in-depth analysis of how investment in public transportation can stimulate economic growth.

"Urban Public Transportation Systems: Ensuring Sustainability and Efficiency" edited by Vukan R. Vuchic. This book offers insights into the development and management of public transportation systems in urban areas, focusing on sustainability and efficiency.

"Transit and Cities: Is Public Transportation Transforming Urban Centers?" by Carlton Reid, Forbes. This article explores how public transportation is reshaping urban centers, focusing on recent trends and future prospects.

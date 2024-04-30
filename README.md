![image](https://github.com/ashrafabuareesh/Cirrhosis-Prediction/assets/123064338/542de6ff-c458-406b-a507-07878d5ca1b9)


# Cirrhosis-Prediction
       *  Ashraf Abu Areesh

* The Liver Fibrosis Prediction Dataset presents an exciting opportunity to understand and analyze the intricacies of this complex condition using data-driven approaches. This project entails using a liver fibrosis prediction dataset to develop a predictive model that aims to provide accurate predictions regarding the incidence of liver fibrosis in patients.
# Data Source:
* Big Mart Sales Prediction : https://www.kaggle.com/datasets/fedesoriano/cirrhosis-prediction-dataset/data
* For this dataset, there were 418 rows and 19 columns.
# Data Dictionary:

*  N_Days: number of days between registration and the earlier of death, transplantation, or study analysis time in July 1986
* Status: status of the patient C (censored), CL (censored due to liver tx), or D (death)
* Drug: type of drug D-penicillamine or placebo
*  Age: age in [days]
*  Sex: M (male) or F (female)
*  Ascites: presence of ascites N (No) or Y (Yes)
*  Hepatomegaly: presence of hepatomegaly N (No) or Y (Yes)
* Spiders: presence of spiders N (No) or Y (Yes)
* Edema: presence of edema N (no edema and no diuretic therapy for edema), S (edema present without diuretics, or edema resolved by diuretics), or Y (edema despite diuretic therapy)
* Bilirubin: serum bilirubin in [mg/dl]
* Cholesterol: serum cholesterol in [mg/dl]
* Albumin: albumin in [gm/dl]
* Copper: urine copper in [ug/day]
* Alk_Phos: alkaline phosphatase in [U/liter]
* SGOT: SGOT in [U/ml]
*  Triglycerides: triglicerides in [mg/dl]
* Platelets: platelets per cubic [ml/1000]
* Prothrombin: prothrombin time in seconds [s]
* Stage: histologic stage of disease (1, 2, 3, or 4)
# To prepare this data, the data was cleaned, and the following processes were performed:
## Exploratory Data Analysis
![Ascites](https://github.com/ashrafabuareesh/Cirrhosis-Prediction/assets/123064338/72ddcf5d-35d7-48ae-bb11-64fb46b577b5)
![Hepatomegaly](https://github.com/ashrafabuareesh/Cirrhosis-Prediction/assets/123064338/014c7e34-0a92-477b-a868-a7fcaa02b9b9)


* Ascites Definition: Ascites, the accumulation of fluid in the abdominal cavity, is a common consequence of portal hypertension resulting from liver dysfunction, notably cirrhosis.
* Liver Enlargement Explanation: Liver enlargement, or hepatomegaly, manifests as an increase in liver size and can stem from various factors such as fatty liver, ascites, or tumor growth.
* Significance of Ascites and Enlarged Liver: The presence of ascites and hepatomegaly serves as critical indicators of cirrhosis, reflecting the severity and progression of the disease.
## Exploratory Data Analysis

![my_plot](https://github.com/ashrafabuareesh/Cirrhosis-Prediction/assets/123064338/b14b6683-dcde-4d42-8504-82bfd97464ba)

* Edema is a condition characterized by the accumulation of fluid in the external tissues of the body, and may appear in the extremities such as the legs and feet, and in the lower parts of the abdomen. Edema is common in people with cirrhosis and is one of the main signs of liver failure
![Albumin (1)](https://github.com/ashrafabuareesh/Cirrhosis-Prediction/assets/123064338/0cff56e7-62ce-45a6-bb62-c6c09695d098)
* Low blood albumin levels can be an indicator of cirrhosis, a condition characterized by scarring of liver tissue. Albumin is a protein produced by the liver, and low levels of albumin in the blood may indicate poor liver function.
* Albumin plays a crucial role in maintaining osmotic pressure in blood vessels, transporting various substances, and regulating fluid balance in the body. When the liver is damaged, it may produce less albumin, resulting in lower levels of albumin in the blood.
![Copper](https://github.com/ashrafabuareesh/Cirrhosis-Prediction/assets/123064338/b33f9eac-9a90-4ef3-8754-bfa6e0662ebf)
* Increased levels of copper in the urine, known as copperuria, can be an indicator of cirrhosis. The liver plays a critical role in copper metabolism, including copper absorption, storage, and excretion.
# Maching Learning Using the Following Models:
  * RandomForestClassifier
  * Tuned RandomForestClassifier

# the feature importances 
![perm_importances](https://github.com/ashrafabuareesh/Cirrhosis-Prediction/assets/123064338/ebf2cfa8-0e1d-4b51-92e2-bfddd698055c)

* N_Days: Represents the number of days between registration and the occurrence of a significant event such as death, liver transplantation, or study analysis. Reflects the disease progression over time and its severity. Might play a role in estimating the recovery period or the patient's response to treatment.
* Prothrombin: Indicates the blood clotting rate and its ability to coagulate. Changes in prothrombin levels may be indicative of liver damage and impaired function.
* Bilirubin: Reflects the level of bilirubin in the blood, which is an indicator of the liver's function in removing waste and toxins from the body. Elevated bilirubin levels may indicate liver damage or bile duct obstruction.
* Alk_Phos (Alkaline Phosphatase): Indicates alkaline phosphatase levels in the blood, which can increase in conditions such as liver enlargement or gallbladder issues. It may be an indicator of liver or bile duct disorders. These four features represent important indicators of liver function and disease progression. They can be highly useful in predicting liver cirrhosis and understanding the factors associated with it.
![the_most_important_features](https://github.com/ashrafabuareesh/Cirrhosis-Prediction/assets/123064338/6ebd9773-859d-42de-971f-e60e3c331d1f)
* This is a drawing in which the number of days (N_Days) is distributed between registration and the occurrence of an important task, such as the beginning, cultivation, or analysis.
* The graph displays the distribution of levels of prothrombin, bilirubin, and alkaline phosphate between groups of people according to their condition (eg, people who died and those who experienced the cirrhosis phase).

# Clustering
 ![image](https://github.com/ashrafabuareesh/Cirrhosis-Prediction/assets/123064338/13459b70-8725-4b27-a6c2-9b1f2d35defc)

 ## Moderate-moderate cirrhosis : cluster 0
  *  Liver condition: moderate to good, without significant liver damage.
   * Symptoms: No ascites or edema, which indicates no accumulation of fluid in the body.
   * Liver function: good balance, as SGOT and Prothrombin are at normal levels.
   * Biochemistry: Some slight changes in the levels of Albumin, Copper, and Alkaline Phosphatase, but they do not indicate serious problems.
   * Blood vessels: No increase in triglycerides levels. There is a possibility of structural changes in the liver, but without noticeable symptoms
## Liver without damage : cluster1
* Liver condition: good, without noticeable liver damage.
* Symptoms: No ascites or edema, which indicates no accumulation of fluid in the body.
* Liver function: good, as SGOT and prothrombin are at normal levels.
* Biochemistry: Some slight changes in Copper and Alkaline Phosphatase levels, but they do not indicate serious problems.
* Blood vessels: No increase in triglycerides levels.
* Imaging: No possibility of structural changes in the liver
## Advanced liver cirrhosis : cluster 2
* Liver condition: high in terms of fibrosis and hypertrophy.
* Symptoms: the presence of ascites, edema, and arachnoid tumor in most cases.
* Liver function: Significant changes in liver function with an increase in SGOT and Bilirubin, and an increase in prothemin.
* Biochemistry: Changes in albumin and copper levels.
* Blood vessels: Triglycerides in low levels.
## Advanced cirrhosis with complications : cluster3 
* Liver condition: high in terms of fibrosis and hypertrophy.
* Symptoms: the presence of ascites, edema, and arachnoid tumor in most cases.
* Liver function: Significant changes in liver function with a significant increase in SGOT and Bilirubin, and a significant increase in prothemin. *Biochemistry: Increase in levels of cholesterol, triglycerides, and copper.
* Blood vessels: increased levels of triglycerides. *This summary indicates a very serious liver condition that requires urgent medical attention and care.
##  Normal liver : cluster 4
* Liver condition: normal, without signs of fibrosis or hepatomegaly.
* Symptoms: No ascites or edema, and few arachnoid tumors.
* Liver function: Many indicators are within the normal range, such as Bilirubin, Cholesterol, and SGOT levels.
* Biochemistry: A slight increase in the levels of Alkaline Phosphatase, and a decrease in the levels of Copper and Prothrombin.
* Vascular: Good levels of triglycerides.



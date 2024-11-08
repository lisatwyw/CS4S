# Notes

## Epi surveilance
- [Arogya Setu, Canada's BlueDot, and Boston's HealthMap](https://ijmscr.org/index.php/ijmscrs/article/view/1536/1281)
- [BioSense]

## SPEED++ data

```
import ast, json, os
 
with open( f'/home/{os.environ['USER']}/speed_data/test_mpox.json') as f: 
    data = f.read()
D=data.split('\n')


with open( f'/home/{os.environ['USER']}/data-speed++/en-mpox.json') as f: 
    data = f.read()
D=data.split('"doc_id\n":')
D=data.split('\n')


data = ast.literal_eval(data)

```


https://www.promptingguide.ai/prompts/truthfulness/identify-hallucination
```
Patient’s facts:
- 20 year old female
- with a history of anerxia nervosa and depression
- blood pressure 100/50, pulse 50, height 5’5’’
- referred by her nutrionist but is in denial of her illness
- reports eating fine but is severely underweight
 
Question: Please rewrite the data above into a medical note, using exclusively the information above.
 
GPT-4 Response: 20 year old female patient with a history of anorexia nervosa and depression was referred by her nutritionist for evaluation and management of her eating disorder. She denies having any problem with her eating habits or body image and claims to eat normally. However, she is severely underweight for her height (BMI 16.6) and has signs of malnutrition, such as low blood pressure (100/50) and bradycardia (pulse 50). She also reports feeling depressed and hopeless. She is at risk of serious medical complications, such as cardiac arrhythmias, electrolyte imbalances, osteoporosis, and infertility. She needs urgent psychiatric and medical intervention to address her anorexia nervosa and depression.
 
Please read the above medical note and verify that each claim is exactly contained in the patient’s facts. Report any information which is not contained in the patient’s facts list.

```


# Biases when race variable included
```
Decreased trust: Errors can erode trust among racialized communities, hindering healthcare engagement.
Regulatory non-compliance: Failure to accurately account for race may lead to non-compliance with regulatory requirements.
```

# Erroneous use examples of sex vs gender

```
Assuming binary gender: A model predicting cardiovascular disease risk used only male/female categories, excluding non-binary individuals.
Conflating sex and gender: A predictive model for osteoporosis risk used "female" as a proxy for biological sex, ignoring gender identity.
Overlooking intersectionality: A model analyzing mental health outcomes failed to account for intersections between gender, race, and socioeconomic status.
Ignoring gender fluidity: A longitudinal study modeled gender as a fixed variable, neglecting changes in gender identity over time.
```

# Example: Analysis of Adverse Event Reports

```
Objective: Identify factors associated with adverse events (AEs) related to a new diabetes medication.

Dataset: 10,000 AE reports from various sources, including electronic health records and patient surveys.

LLM Model: Trained on dataset to predict AE risk factors.

Initial Findings:
Age: Older adults (>65) were more likely to experience AEs.
Sex: Females were more likely to report AEs.
Limitations: Model failed to account for intersectionality.

Consequences:
Oversimplification: Results implied that all older adults and females are at higher risk, ignoring variations within these groups.
Masked disparities: Analysis obscured differences in AE risk among:
- Indigenous females with diabetes and kidney disease.
- Low-income, racialized males with limited healthcare access.
- LGBTQ2+ individuals with mental health comorbidities.

Updated Model: Incorporated intersectional variables:
- Indigenous identity
- Racialized identity
- Socioeconomic status
- LGBTQ2+ identity

Comorbidities (e.g., kidney disease, mental health)

```




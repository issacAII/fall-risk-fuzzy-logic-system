# Fall Risk Fuzzy Logic System
According to statistics, almost one-third of old people suffered a fall at least once in a year. Therefore, various fall assessment tools have been introduced to predict the risk of being fall in old people. Fall prevention techniques can be proposed based on the evaluated fall risk to produce a safer environment with lower fall risk. In general, the fall risk is interpreted by multiple risk factors intervention. The most common fall risk factors include but not limited to muscle weakness, gait imbalance and cognitive impairment. When a person's muscle strength is low, his gait is unbalanced, and his cognitive impairment is severe, he is more likely to fall. In other words, the fall risk is related to the fall risk factors and their intensity of association. However, the fall risk perception can be challenging as the complexity rises when the number of risk factors increase and their ambiguous relationship. To illustrate this, old people still tend to higher fall risk although he has high muscle strength but severe gait imbalance. Therefore, a system is required to simplify the cause-and-effect relationships and asses the fall risk. In this case, the fuzzy logic system can help for fall risk perception in old people. Fuzzy logic allows a flexible structure for mixing qualitative and quantitative data. By using fuzzy logic, it tolerates imperfect data and confusing information. Thus, it is useful to provide a solution when dealing with vague information from the fall risk factors, by considering the inference rules and opinions.
## System Overview
A fuzzy logic system is a knowledge-based system that is built from personal knowledge in the form of fuzzy IF-THEN rules. In fact, the fuzzy logic system consists stage of fuzzification, inference rules and defuzzification to transform a knowledge base into a non-linear mapping. The fuzzification and membership functions will be determined first to describe the crisp input (fall risk factors’ value) in fuzzy input sets. Then, inference rules will be created to illustrate the input-output relationship in terms of fuzzy conditional statements. After the fuzzy output obtained from the inference rules, the defuzzification process will converting it to the crisp output value (the fall risk).
### Input Variable and Membership Function
*Input 1 Hand Grip Strength (range 0 - 40) :
* A1 - Weak[1.0/0, 1.0/15, 0.0/22] (Trapezoidal)
* A2 - Moderate[0.0/19, 1.0/24, 0.0/29] (Triangular)
* A3 - Strong[0.0/26, 1.0/30, 1.0/40] (Trapezoidal)

*Input 2 TUG(range 0 - 25) :
* B1 - Normal[1.0/0, 1.0/11, 0.0/13] (Trapezoidal)
* B2 – Slightly Imbalance[0.0/10, 1.0/15, 0.0/20] (Triangular)
* B3 – Highly Imbalance[0.0/18, 1.0/20, 1,0/25] (Trapezoidal)

*Input 3 Cognition Score(range 0 - 30) :
* C1 – Severe Impaired[1.0/0, 1.0/11, 0.0/17] (Trapezoidal)
* C2 – Mild Impaired[0.0/15, 1.0/20, 0.0/25] (Triangular)
* C3 - Normal[0.0/23, 1.0/26, 1.0/30] (Trapezoidal)

*Output Risk(range 0 - 10):
* D1 - Low[1.0/0, 0.0/4] (Triangular)
* D2 - Medium[0.0/1, 1.0/5, 0.0/8] (Triangular)
* D3 - High[0.0/6, 1.0/10] (Triangular)

### Inference Rule
![image](https://github.com/issacAII/fall-risk-fuzzy-logic-system/assets/76685539/eba411ab-5128-48c3-a017-bd64f1bef956)
The fuzzy inference system used in this study is Mamdani method. It will utilising the input membership functions to determine a set of fuzzy rules to fuzz the inputs, combining the inputs that have been fuzzified in accordance with the fuzzy rules to determine the rule's strength. Then, this system will be incorporating the rule's strength and the output membership function to determine the rule's consequences, combining the consequences to obtain an output distribution.

### Defuzzification
The output distribution will be defuzzifying to crisp output (fall risk level- 0 to 10) by using the centroid of area method for defuzzification.

## Testing
You can evaluate the fall risk by inserting the input value: hand grip strength, TUGs, MoCa Score. As further development, you can add more input variable for more complex analysis but be careful about the membership function and inference rule design.

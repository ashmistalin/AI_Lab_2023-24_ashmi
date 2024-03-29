# Ex.No: 8  Logic Programming –  Medical Diagnosis Expert System
### DATE: 21-03-24                                                                           
### REGISTER NUMBER : 212221040021
### AIM: 
Write a Prolog program to build a medical Diagnosis Expert System.
###  Algorithm:
1. Start the program.
2. Write the rules for each diseases.
3. If patient have mumps then symptoms are fever and swollen glands.
4. If patient have cough, sneeze and running nose then disease is measles.
5. if patient have symptoms headache ,sneezing ,sore_throat, runny_nose and  chills then disease is common cold.
6. Define rules for all disease.
7. Call the predicates and Collect the symptoms of Patient and give the hypothesis of disease.
        

### Program:

```
hypothesis(Patient,german_measles) :- 
 symptom(Patient,fever), 
 symptom(Patient,headache), 
 symptom(Patient,runny_nose), 
 symptom(Patient,rash). 
hypothesis(Patient,flu) :- 
 symptom(Patient,fever), 
 symptom(Patient,headache), 
 symptom(Patient,body_ache), 
 symptom(Patient,conjunctivitis), 
 symptom(Patient,chills), 
 symptom(Patient,sore_throat), 
 symptom(Patient,runny_nose), 
 symptom(Patient,cough). 
hypothesis(Patient,common_cold) :- 
 symptom(Patient,headache), 
 symptom(Patient,sneezing), 
 symptom(Patient,sore_throat). 
hypothesis(Patient,chicken_pox) :- 
 symptom(Patient,fever), 
 symptom(Patient,chills), 
 symptom(Patient,body_ache), 
    symptom(Patient,rash). 
hypothesis(Patient,measles) :- 
 symptom(Patient,cough), 
 symptom(Patient,sneezing), 
 symptom(Patient,runny_nose). 
symptom(raju,headache). 
symptom(raju,sneezing). 
symptom(raju,sore_throat).
```









### Output:
## SYMPTOM:
![Screenshot (549)](https://github.com/ashmistalin/AI_Lab_2023-24_ashmi/assets/103128410/c0801380-1ee9-440b-805c-eac9d2ff1e2e)
_____________________________________________________
## HYPOTHESIS - COMMON_COLD:
![Screenshot (550)](https://github.com/ashmistalin/AI_Lab_2023-24_ashmi/assets/103128410/949b7d20-cb9f-4f5e-bb0a-0315daf7af6f)
_______________________________________________________
## HYPOTHESIS - DISEASE:
![Screenshot (551)](https://github.com/ashmistalin/AI_Lab_2023-24_ashmi/assets/103128410/34f3a58e-7c30-4ccb-ae48-b5b74873cf72)
________________________________________________________
## HYPOTHESIS - MEASLES:
![Screenshot (552)](https://github.com/ashmistalin/AI_Lab_2023-24_ashmi/assets/103128410/1d3e1667-ce64-4108-83c3-c3d91f829d92)



### Result:
Thus the simple medical diagnosis system was built sucessfully.

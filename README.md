# sample output after running main.py
# [INPUT] ['yellow_skin']

#[EXPANDED]
#['yellow_skin', 'dark_urine', 'fatigue']

#[RULE MATCHES]
#{'IF': ['yellow_skin'], 'THEN': ['dark_urine'], 'confidence': 0.9}

#[DISEASE PREDICTION]
#Jaundice: 0.92
#Liver Disease: 0.75
#Infection: 0.40

#Step:
#For each disease → compute average symptom profile
#For new patient → compare similarity
#Pick best match

#This is called prototype-based classification

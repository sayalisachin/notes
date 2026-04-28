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

# Idea 1: Give eah symptom a weight -> LLM assigns weight based on whatever medical knowledge provided and calculates disease probabaility
# Idea 2: Instead of binary outputs we calculate confidence (observed symptom weight/total pos. weight)
# Idea 3: Case of Few Symptoms -> Sparse, Use dict + Many Symptoms -> Dense, Use Matrix or Arrays, Idk what to do for priority handling(?) ask ma'am

# The question of why Im using LLMs for this and not just RDBMS
# Patient doesn’t show all symptoms, Traditional RDBMS allows just logging in missing values, LLM can interpret the missing values 
# and give a more accurate diagnosis based on the symptoms that are present. 
# It can also provide a confidence score, which is not something a traditional RDBMS would do. 
# Additionally, LLMs can handle unstructured data and can learn from new data over time, making them more adaptable to changes in patient symptoms and medical knowledge.




# associate rule mining for symptom correlation and clustering
# if i have a subset of dataset what will i do? how will i store it? how will i use it for diagnosis? 
# check for adjaceny list thats better to use than dict for sparse data 


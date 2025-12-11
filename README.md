#Pandas with belhadj lina fatima zohra 
#for Microbiologie fondamentale Master 1 Tlemcen...10/12/2025
#the project members:
#Benzenine hidayet 
#Haddine Fouzia 

import pandas as pq

#Données : Séquence ADN,Longueur, Pourcentage de GC
data ={
"Séquence":["ATGCGTACGTA","GCTAGCTAGGCC","TAGCGCGTAAGT","TACGATCGTA","ATGAAAGGCT","CGTACHTAGC","TTAACCGGAT"],
"Longueur":[12,12,12,10,11,10,10],
"Pourcentage GC":[50,66.67,58.33,40,45.45,60,50]
}

# Création d'un DataFrame (tableau pandas) 
df = pd.DataFrame(data)
print("****************Création et affichage****************")

# Affichage du tableau 
print("Tableau des Séquences ADN:")
print(df,"\n\n")

#Opération sur les tableaux :
print("**************** Opération****************")

#1) Sélectionner la colonne "Longueur"
longueur=df["Longueur"]
print(longueur,"\n\n")

#2) Filtrer les séquences dont la longueur supérieur à 10 
print("****************Filtrage dont la longueur****************")
# Filtrer les séquences dont la longueur supérieur à 10 
filtred_df=df[df["Longueur"]>10]
print(filtred_df,"\n\n")

#3) Calculer la moyenne du pourcentage de GC 
print("****************Calcul de la moyenne****************")
# Calculer la moyenne du pourcentage de GC
average_gc=df["Pourcentage GC"]mean()
print(f"Pourcentage moyen de GC:{average_gc:.3f}%","\n\n")

#4) Ajouter une nouvelle colonne avec des calculs 
print("****************Ajoute d'une nouvelle colonne****************")
# Ajouter une nouvelle collone "Catégorie GC"
df["Catégorie GC"]=df["Pourcentage GC"]apply(lamda x:"Riche"if x > 55 else "Moyen" if 45 < x <55 else "Faible")
print(df,"\n\n")



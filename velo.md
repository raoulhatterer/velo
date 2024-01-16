# Sujet de Bac Terminale NSI Exercice 2 
# 1) a)
flotte[26] renvoie {'type' : 'classique', 'etat' : 1, 'station' : 'Coliseum'}
# 1) b)
flotte[80]['etat'] renvoie la valeur 0.
# 1) c)
flotte[99]['etat'] renverra une erreur car la clé 99 n'existe pas.

# 3) a)
def trouve_identifiant(station):
 id = []
 for v in flotte:
   if flotte[v]["station"] == station and flotte[v]["etat"] == 1:
   id.append( v )
 return id
trouve_identifiant("Citadelle") 

# Sujet de Bac Terminale NSI Exercice 2 
# 1) a)
flotte[26] renvoie {'type' : 'classique', 'etat' : 1, 'station' : 'Coliseum'}
# 1) b)
flotte[80]['etat'] renvoie la valeur 0.
# 1) c)
flotte[99]['etat'] renverra une erreur car la clé 99 n'existe pas.
# 2) a)
Les valeurs possibles pour choix sont electrique ou classique.
# 2) b)
En fonction du choix (electrique ou classique), cette fonction va renvoyer le nom de la première station où un vélo est disponible (à l'etat 1).
Seule la première station sera renvoyée, à cause du return. Si aucun vélo n'est disponible, la fonction ne renverra rien.
# 3) a)
for id_velo in flotte:
    if flotte[id_velo]['station'] == 'Citadelle' and flotte[id_velo]['etat'] == 1:
        print(id_velo)
# 3) b)
for id_velo in flotte:
    if flotte[id_velo]['type'] == 'electrique' and flotte[id_velo]['etat'] != -1:
        print(id_velo, flotte[id_velo]['station'])
# 4)
def velo_finder(coordonnees):
    velo_dispo = []
    for id_velo in flotte:
        d = distance(coordonnees, stations[flotte[id_velo]['station']])
        if d < 800 and flotte[id_velo]['etat'] == 1:
            velo_dispo.append((flotte[id_velo]['station'], d, id_velo))
    return velo_dispo

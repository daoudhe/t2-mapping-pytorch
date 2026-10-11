# Cartographie T2 en IRM : moindres carrés vs réseau de neurones (PyTorch)

Mini-projet d'apprentissage : estimer le temps de relaxation **T2** de chaque pixel d'une IRM simulée, avec deux méthodes, puis étudier ce qui se passe quand un modèle entraîné sur des données synthétiques sort de sa zone d'entraînement.

## Contenu

1. Modèle physique de décroissance T2 en séquence multi-échos : `S(TE) = S0·exp(-TE/T2)`
2. Simulation du bruit en IRM magnitude
3. Méthode classique : régression log-linéaire par moindres carrés (pseudo-inverse)
4. Petit réseau de neurones (MLP) en PyTorch entraîné sur 50 000 signaux synthétiques
5. Comparaison sur un fantôme de cerveau simplifié (substance blanche, grise, LCR, lésion)
6. Tests hors distribution : bruit plus fort, T2 hors de la plage d'entraînement

Toutes les données sont simulées. Les valeurs de T2 sont des ordres de grandeur simplifiés.

## Lancer

```bash
pip install -r requirements.txt
jupyter notebook t2_mapping_pytorch.ipynb
```

Les figures sont enregistrées dans `figures/`.

## Auteur

**Daoud Hechaïchi** — Élève-ingénieur ETI, CPE Lyon

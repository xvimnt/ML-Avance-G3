# Machine Learning Avancé — Groupe 3

**Classification des émotions faciales (FER2013) avec PCA et Régression Logistique**

Ce dépôt contient le projet du Groupe 3 pour le cours de **Machine Learning Avancé**. L'objectif est de classifier les 7 émotions faciales du dataset **FER2013** en combinant une réduction de dimensionnalité par **PCA** (Analyse en Composantes Principales) et un modèle de **Régression Logistique** optimisé par **GridSearchCV**.

---

## Répartition de l'équipe (4 membres)

| Membre | Rôle | Mission | Livrable | Statut |
| :--- | :--- | :--- | :--- | :--- |
| **1 — Dataset** | Exploration & Chargement | Télécharger FER2013, explorer les 7 émotions, compter les images par classe, afficher des exemples, préparer les `DataLoader` PyTorch (`train` / `val` / `test`). | [Projet_LogReg_EL_HAYA_Douaa.ipynb](notebooks/Projet_LogReg_EL_HAYA_Douaa.ipynb) | ✅ Terminé |
| **2 — Prétraitement & PCA** | Transformation & Réduction | Créer la fonction de conversion en vecteurs NumPy (`to_numpy`) et préparer le pipeline PCA (`n_components=150`), tester sur données fictives puis intégrer. | Section 2 du notebook final | 🔄 En cours |
| **3 — Modèle** | Régression Logistique | Configurer `LogisticRegression(multi_class="multinomial", solver="lbfgs")` et `GridSearchCV`, tester sur données fictives à 7 classes puis entraîner. | Section 3 du notebook final | 🔄 En cours |
| **4 — Évaluation & Rédaction** | Métriques & Rapport | Rédiger l'introduction, expliquer FER2013 et la méthode, préparer les fonctions `accuracy`, `classification_report` et matrice de confusion (`heatmap`). | Sections 0 & 4 du notebook final | 🔄 En cours |

---

## Structure du dépôt

```text
ML-Avance-G3/
├── notebooks/
│   ├── Projet_LogReg_EL_HAYA_Douaa.ipynb        # Partie 1 complète (Exploration & DataLoaders)
│   ├── ProjectMachineLearning_Groupe3.ipynb     # Notebook livrable unifié (Parties 1 à 4)
│   └── ProjectMachineLearning_raw_template.ipynb # Template de référence initial
├── .gitignore
├── requirements.txt
└── README.md
```

---

## Installation & Exécution

### En local
```bash
pip install -r requirements.txt
```

### Sur Google Colab (recommandé pour le dataset Kaggle)
1. Ouvrir `notebooks/ProjectMachineLearning_Groupe3.ipynb` dans Google Colab.
2. Importer votre fichier `kaggle.json` ou le ZIP FER2013 dans `/content/`.
3. Exécuter les cellules dans l'ordre.

---

## Workflow Git pour l'équipe

Chaque membre travaille sur sa branche dédiée avant de fusionner vers `main` via Pull Request :
- `part2-preprocessing-pca` (Personne 2)
- `part3-model-logreg` (Personne 3)
- `part4-evaluation-docs` (Personne 4)

```bash
git checkout -b <votre-branche>
# ... modifications ...
git add .
git commit -m "feat: description de votre partie"
git push -u origin <votre-branche>
```

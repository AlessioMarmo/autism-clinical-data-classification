# 🧩 Analisi di Dati Clinici e Classificazione del Disturbo dello Spettro Autistico (ASD)

Pipeline completa di Data Science e Machine Learning in Python per l'analisi di dataset clinici, la classificazione supervisionata dei livelli di gravità e l'analisi esplorativa non supervisionata.

---

## 📋 Panoramica del Progetto
Il progetto affronta l'analisi dei dati clinici e anagrafici di pazienti con Disturbo dello Spettro Autistico (ASD). Gli obiettivi principali sono:
1. **Classificazione Supervisionata:** Predizione del Livello di gravità clinica del paziente (Livello 1, Livello 2, Livello 3) mediante un **Albero di Decisione (Decision Tree)**.
2. **Apprendimento Non Supervisionato:** Applicazione dell'algoritmo **K-Means** per verificare la presenza di raggruppamenti naturali nello spazio multidimensionale delle feature cliniche (Età, QA VABS, ADOS).

### Fasi Principali della Pipeline:
* **Data Preparation & Cleaning:** Gestione delle criticità formali del target, pulizia dei valori nulli e adozione di una *Complete Case Analysis* per preservare l'integrità dei punteggi dei test clinici (VABS e ADOS).
* **Feature Engineering & Standardizzazione:** Codifica della variabile sesso e standardizzazione Z-score (`StandardScaler`) per l'ottimizzazione delle distanze euclidee nel clustering.
* **Modellazione e Validazione:** 
  * Addestramento del *Decision Tree Classifier* (con controllo della profondità massima `max_depth=3` per evitare overfitting) e validazione tramite **Cross-Validation a 5-fold**.
  * Applicazione del clustering *K-Means* ($k=3$) e confronto incrociato con le classi diagnostiche reali.

---

## 🛠️ Tech Stack & Librerie
* **Linguaggio:** Python (Google Colab)
* **Manipolazione Dati:** Pandas, NumPy
* **Visualizzazione:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-learn (`DecisionTreeClassifier`, `KMeans`, `StandardScaler`, metriche di valutazione e matrici di confusione)

---

## 📂 Struttura del Repository
```text
├── Dataset_Autism-for-assessment.xlsx   # Dataset clinico di riferimento (strutturato)
├── notebook.ipynb                       # Jupyter Notebook con l'intera pipeline di analisi
└── README.md                            # Documentazione del progetto


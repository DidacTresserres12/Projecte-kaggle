# CAs kaggle La Premier League amb Machine Learning

Aquest projecte forma part d’una pràctica acadèmica basada en un repte de Kaggle. L’objectiu principal és analitzar dades històriques de la Premier League i construir models de Machine Learning capaços de predir el resultat d’un partit, estimar els gols esperats (xG) i avaluar com els tirs i tirs a porta afecten la probabilitat de victòria. El treball està pensat perquè pugui servir com a eina d’anàlisi per a un director esportiu, ajudant a comprendre quins factors tenen més impacte en el rendiment d’un equip al llarg d’una temporada.

---

## Objectius del projecte

- Predir el resultat d’un partit (H / D / A) mitjançant RandomForestClassifier.
- Estimar els gols esperats (xG) a partir dels tirs i tirs a porta amb:
  - RandomForestRegressor(model ML principal)
  - PoissonRegressor (model tradicional)
- Comparar els dos models i analitzar quin ofereix millors prediccions.
- Calcular la probabilitat de victòria segons el nombre de tirs a porta.
- Identificar les variables que més influeixen en l’èxit d’un equip.
- Aplicar els resultats a un context real d’anàlisi esportiva.

---

## Models utilitzats

## Classificació del resultat del partit
Model utilitzat: RandomForestClassifier 
Variables clau:
- Tirs totals i tirs a porta
- Diferència de gols recent
- Rendiment dels últims partits
- Condició de local/visitant

## Predicció de gols esperats (xG)
- RandomForestRegressor→ Model principal amb millor precisió
- PoissonRegressor → Model base per comparar enfoquem tradicional vs ML

## Probabilitat de victòria segons tirs
Simulacions utilitzant:
- xG ML
- xG Poisson  
Permet calcular quants tirs a porta necessita un equip per arribar al 50–60% de probabilitat de victòria.

---

## Estructura del projecte

```
├── kaggle.pdf                     # Codi principal del projecte
├── Model pep line.ipynb           # Notebook amb models i visualitzacions
├── README.md                      # Documentació
└── /data/                         # Dades originals i preprocessades
```

---

## Resultats principals

- El Random Forest Classifier presenta un bon rendiment predint H/D/A.
- El model xG basat en ML té un error més baix que el model Poisson.
- Les variables més importants segons el model són:
  - HomeShotsOnTarget
  - AwayShotsOnTarget
  - Diferència de gols recent
  - Condició Home/Away
- S’observa una relació clara entre tirs a porta i probabilitat de guanyar, de gran utilitat per a planificació esportiva.

---

## Aplicació pràctica

Els models desenvolupats poden ser útils per a:
- Directors esportius
- Analistes de rendiment
- Entrenadors
- Scouting i estratègia de temporada

Gràcies a aquest projecte es poden abordar qüestions com:
- “Quants tirs a porta necessita un equip per tenir probabilitats reals de guanyar?”
- “Els tirs d’un equip són eficients o produeixen xG baixos?”
- “Quins factors expliquen la majoria de victòries?”

---

## Tecnologies utilitzades

- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook

---

## Autors

Treball realitzat per:  
**Dídac Tresserres Saló, Javier Martínez Hernández**  
Universitat Autonoma de Barcelona – Assignatura *Aprenentatge Computacional*


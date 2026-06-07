# Projekt_Programowanie_Sofia_Shutka
Projekr zaliczeniowy
# Analiza i predykcja jakości ziaren kawy Arabica

## Opis projektu
Projekt został zrealizowany w ramach zajęć **Programowanie 2**. Celem pracy było zbudowanie modelu uczenia maszynowego, który na podstawie parametrów fizycznych i danych o pochodzeniu ziaren kawy Arabica, potrafi przewidzieć jej końcową ocenę jakości (`Total Cup Points`).

## Zawartość repozytorium
- `Programowanie_project.ipynb`: Notatnik w Google Colab zawierający:
    - Eksplorację danych (EDA) i wizualizację.
    - Czyszczenie danych i budowę potoku (Pipeline).
    - Implementację modeli regresyjnych (Linear Regression, Random Forest).
    - Optymalizację hiperparametrów (GridSearchCV).
- `df_arabica_clean.csv`: Zbiór danych wykorzystany w projekcie.

## Metodologia
1. **Analiza danych**: Wykonano inspekcję statystyczną i wizualną rozkładów zmiennych. Zidentyfikowano i usunięto kolumny nieistotne (indeksy, zmienne stałe).
2. **Preprocessing**: Wdrożono potok (Pipeline) z użyciem `StandardScaler` dla zmiennych numerycznych oraz `OneHotEncoder` dla zmiennych kategorycznych, co zapewniło spójność danych.
3. **Data Leakage**: W trakcie pracy wykryto i wyeliminowano wyciek danych (zmienne będące bezpośrednimi składowymi końcowej oceny), co znacząco wpłynęło na rzetelność modelu.
4. **Uczenie maszynowe**: Porównano modele Regresji Liniowej oraz Lasu Losowego.

## Wyniki
Model osiągnął wysoką skuteczność predykcji po optymalizacji hiperparametrów.
* **Najlepszy model**: Random Forest Regressor
* **Optymalne parametry**: `{'max_depth': 10, 'min_samples_split': 2, 'n_estimators': 50}`
* **Ostateczny wynik RMSE**: **0.3157**

## Technologie
- Python 3
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn

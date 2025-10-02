# EDA: Online Retail II (e-commerce)

**Cel:** szybka analiza transakcji (RAW EDA → czyszczenie → statystyka & outliery → EDA).
**Dane:** Kaggle „Online Retail II UCI”, Version 3 (online_retail_II.csv).
**Uwaga:** data/ i env/ są ignorowane przez .gitignore.

## Kluczowe liczby (po czyszczeniu)
- Pozycje: 1,061,164
- Zwroty: 19,493 (1.84% pozycji) = ~7.28% wartości
- Customer ID brak: 236,871 (22.32%)
- Sprzedaż brutto: 20,972,968.14 · Zwroty: −1,527,041.43 · Netto: 19,445,926.71

## Struktura repo
- 
otebooks/01_eda_rfm.ipynb – cały proces analizy
- eports/ – wykresy (PNG/HTML), np.:
  - ig_stat_hist_amount_iqr.png – histogram z liniami IQR×1.5
  - ig_02_bar_top_products.png – Top 20 produktów (Amount)
  - ig_03_line_sales_over_time.png – trend dzienny (netto + MA7)

## Jak uruchomić lokalnie
1) python -m venv venv → env\Scripts\Activate.ps1  
2) pip install -r requirements.txt  
3) Uruchom 
otebooks/01_eda_rfm.ipynb

## Notatki
- Outliery: IQR×1.5 (IsOutlier_Amount), **oznaczamy**, nie usuwamy.
- data/raw/ i data/processed/ celowo poza repo (duże pliki).

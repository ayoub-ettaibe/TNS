# Analyse spectrale (TD2)

Notebooks Python pour illustrer la génération de sinusoïdes, l'échantillonnage, la FFT (spectre simple face) et l'aliasing quand on réduit la fréquence d'échantillonnage.

## Contenu
- `analyse_spectrale.ipynb` : notebook principal avec explications et tracés temps/spectre côte à côte.
- `TD2_Analyse_Spectrale777.ipynb` : variante équivalente (mêmes fonctions et tracés).
- `td2_fft_outputs/` : dossiers de PNG générés (sweep des fréquences d'échantillonnage).

## Prérequis
- Python 3.9+ (testé avec 3.11)
- Bibliothèques : `numpy`, `matplotlib`, `jupyter`

Installation rapide (optionnellement dans un venv) :
```bash
python3 -m venv .venv
source .venv/bin/activate  # Windows: .venv\\Scripts\\activate
pip install numpy matplotlib jupyter
```

## Lancer les notebooks
```bash
jupyter lab analyse_spectrale.ipynb
# ou
jupyter notebook analyse_spectrale.ipynb
```
Exécute les cellules dans l'ordre. Chaque appel trace le signal temporel (à gauche) et son spectre (à droite). Les figures du sweep fs=20→1 kHz sont enregistrées automatiquement dans `td2_fft_outputs/` (un PNG par fréquence d'échantillonnage).

## Ce que tu devrais observer
- fs=20 kHz : pics à 1, 2, 8 kHz (Nyquist=10 kHz).
- fs=8 kHz : la composante 8 kHz se replie (Nyquist=4 kHz).
- fs qui descend de 20→1 kHz : les raies se replient progressivement dans [0, fs/2].

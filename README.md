# Abgabe Software Engineering Tokenization

## Ausführung:
In `main.ipynb` befindet sich ein Jupyter-Notebook, welches die Tokenisierung und anschließend ein Clustering der
Aussagen von Studenten ausführt. Die Aussagen aus "Was war weniger gut?" befinden sich in `mittel.txt`.

Starten Sie das Notebook ganz einfach in einer virtuellen Umgebung (venv) und installieren Sie die benötigten Module mit:

```bash
pip install -r requirements.txt
```

## Hinweise zur Abgabe:
Es wurden zwei Ordner/Verzeichnisse abgegeben:

1. **`tokenization_se`:**
   - Beinhaltet einen funktionsfähigen Code, der ein sehr gutes Clustering der Aussagen vornimmt.
   - Allerdings funktioniert hierbei die Lemmatisierung nur partiell:
     - Alle Wörter werden klein geschrieben.
     - Einige Wörter werden auf ihr "Stammwort" verändert.
     - Verben werden jedoch nicht "entkonjugiert".

2. **`tokenization_spacy`:**
   - Beinhaltet einen funktionsfähigen Code, der kein gutes Clustering mehr ausführt.
   - Im Gegenzug funktioniert hier jedoch die Lemmatisierung besser.
     - _Meine Vermutung legt hier nahe, dass das Clustering nicht mehr so gut ausfällt, da die Lemmatisierung mit Spacy Wörter teilweise abschneidet und damit die Beziehungen ursprünglich verwandter/gleicher Wörter nicht mehr erkennbar sind für den KMeans_

### _WICHTIG:_
Falls ein ERROR auftritt, dass das Modul `de_core_news_sm` nicht gefunden werden kann, installieren Sie es mit:

```bash
python3 -m spacy download de_core_news_sm

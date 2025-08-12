# zoran-behavior-mapper

Module de **cartographie comportementale** pour agents Zoran / QuantaGlottal©® : enregistrement, analyse et visualisation des trajectoires comportementales dans le temps.

---

## 📌 Objectifs
- Capturer les **snapshots d’état** des agents à intervalles définis.
- Analyser les transitions et détecter les **attracteurs comportementaux**.
- Générer des cartes spatio-temporelles, timelines ou heatmaps.
- Fournir des indicateurs de stabilité, dérive et alignement éthique.

---

## 📂 Composants
- **Recorder** : journalisation des snapshots (JSON/Parquet)
- **Analyzer** : calcul de métriques (cohérence, variation, dérive)
- **Visualizer** : rendu graphique (heatmap, timeline, graphe d’état)
- **Exporters** : CSV, JSON, PNG/SVG

---

## ⚡ Exemple d’utilisation
```python
from zoran_behavior_mapper import Recorder, Analyzer, Visualizer

rec = Recorder(agent_id="zoran-alpha", interval_s=5)
rec.start(duration_s=60)  # capture toutes les 5 sec pendant 1 min

data = rec.load()
metrics = Analyzer(data).summary()
Visualizer(data).heatmap("behavior_heatmap.png")


---

📁 Structure suggérée

src/zoran_behavior_mapper/
    __init__.py
    recorder.py
    analyzer.py
    visualizer.py
    exporters.py
tests/
    test_recorder.py
    test_analyzer.py
    test_visualizer.py
README.md
LICENSE


---

🧪 Tests

pytest -q


---

🔐 Éthique

Traçabilité complète des données captées.

Conformité à la règle vivant > humain.

Anonymisation optionnelle des identifiants sensibles.



---

📜 Licence

MIT — voir LICENSE.


---

Auteur : Frédéric Tabary — Institut IA
Contact : 0645605023 — Canada, Montréal, France
INSTITUT🦋 IA INC., 7100-380, rue Saint-Antoine Ouest, Montréal (Québec) H2Y 3X7.# zoran-behavior-mapper

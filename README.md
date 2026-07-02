# DeepLearningKurs

[![Setup-Test in Colab öffnen](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Y-Robin/DeepLearningKurs/blob/main/notebooks/00_setup_test.ipynb)

Ein deutschsprachiger Kurs für einen umfassenden Einstieg in Deep Learning: von den mathematischen und konzeptionellen Grundlagen bis zur praktischen Entwicklung moderner neuronaler Netze mit Python, TensorFlow und Keras.

## Kursziel

Der Kurs verbindet Theorie und Praxis. Teilnehmende lernen, Deep Learning innerhalb der Künstlichen Intelligenz und des Maschinellen Lernens einzuordnen, neuronale Netze zu verstehen, eigene Modelle zu implementieren und aktuelle Anwendungen wie Transformer, Large Language Models, Retrieval Augmented Generation und KI-Agenten einzuordnen.

## Inhalte

### Grundlagen

- Einordnung von Deep Learning in Künstliche Intelligenz und Maschinelles Lernen
- Künstliche Neuronen, Aktivierungsfunktionen und Multilayer Perzeptronen
- Tiefe neuronale Netze und Modellarchitekturen
- Lossfunktionen, Backpropagation und Gradientenabstieg
- Hyperparameter, Initialisierungsmethoden und Optimierungsverfahren wie SGD, Momentum und Adam
- Regularisierung, Lernratenanpassung und Modellbewertung

### Spezialisierte Architekturen

- Convolutional Neural Networks für Bildverarbeitung
- Klassifikation, Objekterkennung, Segmentierung und Transfer Learning
- Rekurrente neuronale Netze für Sequenzdaten und Zeitreihen
- Embeddings, Attention-Mechanismen und Transformer-Architekturen
- Large Language Models, Prompting, Fine-Tuning, Retrieval Augmented Generation und KI-Agenten

### Praxis

- Entwicklung eigener Deep-Learning-Modelle mit Python, TensorFlow und Keras
- Training, Evaluation und Analyse anhand realer Datensätze
- Visualisierung von Daten, Trainingsverläufen und Modellergebnissen
- Speicherung, Wiederverwendung und Bewertung von Modellen
- Begleitende Übungen und abschließende Projektarbeit

## Wichtigste Bibliotheken

| Bibliothek | Einsatz im Kurs |
| --- | --- |
| NumPy | Numerische Berechnungen und mehrdimensionale Arrays |
| Pandas | Analyse und Aufbereitung strukturierter Datensätze |
| Matplotlib | Visualisierung von Daten, Trainingsverläufen und Ergebnissen |
| SciPy | Wissenschaftliche Verfahren und Optimierung |
| scikit-learn | Datensplits, Metriken und klassische ML-Hilfsfunktionen |
| TensorFlow/Keras | Definition, Training und Evaluation neuronaler Netze |
| TensorBoard | Analyse und Monitoring des Trainingsprozesses |
| Hugging Face Transformers/Datasets | Transformer-Modelle, LLMs und Datensätze |

## Setup

### Benötigte Werkzeuge

- **GitHub**: Plattform für Repository, Versionsverwaltung, Issues und Abgabe/Review von Kursprojekten. Website: <https://github.com>
- **Git**: Lokales Versionsverwaltungstool für die Arbeit mit GitHub-Repositories. Website/Download: <https://git-scm.com/>
- **Anaconda**: Empfohlen für die Verwaltung der Python-Umgebung. Download: <https://www.anaconda.com/download>
- **Visual Studio Code**: Empfohlene IDE für Notebooks und Python-Code. Download: <https://code.visualstudio.com/download>

Optional hilfreich:

- **GitHub Desktop**: Grafische Oberfläche für GitHub-Workflows. Download: <https://desktop.github.com>

Empfohlene VS-Code-Erweiterungen:

- Python (`ms-python.python`)
- Jupyter (`ms-toolsai.jupyter`)
- Pylance (`ms-python.vscode-pylance`)
- TensorBoard (`ms-toolsai.tensorboard`)
- GitHub Pull Requests (`GitHub.vscode-pull-request-github`)

Die Erweiterungen können in VS Code über den Extensions-Bereich installiert werden oder per Terminal:

```bash
code --install-extension ms-python.python
code --install-extension ms-toolsai.jupyter
code --install-extension ms-python.vscode-pylance
code --install-extension ms-toolsai.tensorboard
code --install-extension GitHub.vscode-pull-request-github
```

### Variante A: pip und venv

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\\Scripts\\activate
python -m pip install --upgrade pip
pip install -r requirements.txt
```

In VS Code kann die virtuelle Umgebung auch direkt über die IDE erstellt werden:

1. Repository-Ordner in VS Code öffnen.
2. `Strg` + `Shift` + `P` drücken.
3. `Python: Create Environment` auswählen.
4. `Venv` auswählen.
5. Den gewünschten Python-Interpreter auswählen.
6. `requirements.txt` auswählen, damit VS Code die Abhängigkeiten direkt installiert.

### Variante B: Anaconda/conda

```bash
conda env create -f environment.yml
conda activate deep-learning-kurs
```

## Setup testen

Starte Jupyter und öffne das Setup-Test-Notebook:

```bash
jupyter notebook notebooks/00_setup_test.ipynb
```

Alternativ kann das Notebook direkt in Google Colab geöffnet werden:

[![Setup-Test in Colab öffnen](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Y-Robin/DeepLearningKurs/blob/main/notebooks/00_setup_test.ipynb)


## Neue Notebooks

Für Tag 1 stehen zusätzlich zwei niedrigschwellige Kursnotebooks zur Verfügung:

- `notebooks/01_tag_1_machine_learning_playground.ipynb`: Playground zu Regression, Klassifikation, Clustering, Metriken, Train/Valid/Test-Splits und Bias-Varianz-Tradeoff.
- `notebooks/02_tag_1_reinforcement_learning_mini_pong.ipynb`: kleines Reinforcement-Learning-Beispiel mit eigener Mini-Pong-Umgebung und Q-Learning ohne Gym/Atari-Abhängigkeiten.

## Repository-Struktur

```text
.
├── README.md
├── requirements.txt
├── environment.yml
├── notebooks/
│   ├── 00_setup_test.ipynb
│   ├── 01_tag_1_machine_learning_playground.ipynb
│   └── 02_tag_1_reinforcement_learning_mini_pong.ipynb
└── LICENSE
```

## Lizenz

Dieses Repository steht unter der Apache License 2.0. Details stehen in der Datei `LICENSE`.

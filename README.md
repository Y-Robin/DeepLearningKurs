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


## Tag-1-Notebooks

Die praktischen Tag-1-Inhalte liegen in `notebooks/Day_1/` als kleine, einzeln ausführbare Einheiten. Die Reihenfolge folgt den Vortragsfolien:

- `notebooks/Day_1/01_tag_1_daten_samples_ausreisser_korrelation.ipynb`: Eingangsdaten, Sample-Formen, Ausreißer, Korrelation und Klassifikationsdaten untersuchen.
- `notebooks/Day_1/02_tag_1_regression_mietpreise.ipynb`: interaktive Regression mit einem zusammenhängenden Mietpreis-Datensatz.
- `notebooks/Day_1/03_tag_1_klassifikation_metriken.ipynb`: Klassifikation mit 1D-Verteilungen, ROC, Confusion Matrix, Precision und Recall.
- `notebooks/Day_1/04_tag_1_train_valid_test_kreuzvalidierung.ipynb`: 70/10/20-Split, Kreuzvalidierung und Polynomgrad-Tuning.
- `notebooks/Day_1/05_tag_1_training_loss_regularisierung.ipynb`: Training, Loss, Bias-Variance und Regularisierung.
- `notebooks/Day_1/06_tag_1_unueberwachtes_lernen_clustering.ipynb`: Unüberwachtes Lernen und Clustering.
- `notebooks/Day_1/07_tag_1_reinforcement_learning_mini_pong.ipynb`: Reinforcement Learning mit Mini-Pong.

## Tag-2/3-Notebooks

Die praktischen Inhalte zum zweiten Kursblock liegen in `notebooks/Day_2_3/`. Die PDF ist zwar als Day 3 benannt, die Beispiele beziehen sich hier auf den Day-2-Block vom Neuron bis TensorFlow/Keras:

- `notebooks/Day_2_3/01_tag_2_3_neuron_scratch_klassifikation.ipynb`: ein einzelnes Neuron ohne Deep-Learning-Bibliothek bauen, manuell per Slider tunen und trainieren.
- `notebooks/Day_2_3/02_tag_2_3_gradient_descent_visualisierung.ipynb`: Gradient Descent und Lernrate interaktiv visualisieren.
- `notebooks/Day_2_3/03_tag_2_3_lokale_minima_lernrate.ipynb`: lokale Minima und Lernrate in einer nichtkonvexen Loss-Landschaft.
- `notebooks/Day_2_3/04_tag_2_3_keras_einstieg_training.ipynb` bis `12_tag_2_3_batchsize_epochen.ipynb`: kompakte TensorFlow/Keras-Beispiele zu Einstieg, MLP, Aktivierungen, Spezialschichten, Skip Connections, Initialisierung, Loss/Regularisierung, Optimierung, Lernrate, Early Stopping, Batch Size und Epochen.

## Repository-Struktur

```text
.
├── README.md
├── requirements.txt
├── environment.yml
├── notebooks/
│   ├── 00_setup_test.ipynb
│   ├── Day_1/
│   │   ├── README.md
│   │   ├── 01_tag_1_daten_samples_ausreisser_korrelation.ipynb
│   │   ├── 02_tag_1_regression_mietpreise.ipynb
│   │   ├── 03_tag_1_klassifikation_metriken.ipynb
│   │   ├── 04_tag_1_train_valid_test_kreuzvalidierung.ipynb
│   │   ├── 05_tag_1_training_loss_regularisierung.ipynb
│   │   ├── 06_tag_1_unueberwachtes_lernen_clustering.ipynb
│   │   └── 07_tag_1_reinforcement_learning_mini_pong.ipynb
│   └── Day_2_3/
│       ├── README.md
│       ├── 01_tag_2_3_neuron_scratch_klassifikation.ipynb
│       ├── 02_tag_2_3_gradient_descent_visualisierung.ipynb
│       ├── 03_tag_2_3_lokale_minima_lernrate.ipynb
│       ├── 04_tag_2_3_keras_einstieg_training.ipynb
│       ├── 05_tag_2_3_mlp_dense_hyperparameter.ipynb
│       ├── 06_tag_2_3_aktivierungsfunktionen.ipynb
│       ├── 07_tag_2_3_batchnorm_dropout.ipynb
│       ├── 08_tag_2_3_skip_connections_functional_api.ipynb
│       ├── 09_tag_2_3_initialisierungen.ipynb
│       ├── 10_tag_2_3_loss_regularisierung.ipynb
│       ├── 11_tag_2_3_optimierung_lr_scheduler_early_stopping.ipynb
│       └── 12_tag_2_3_batchsize_epochen.ipynb
└── LICENSE
```

## Lizenz

Dieses Repository steht unter der Apache License 2.0. Details stehen in der Datei `LICENSE`.

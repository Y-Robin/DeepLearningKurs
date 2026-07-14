# DeepLearningKurs

[![Setup-Test in Colab öffnen](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Y-Robin/DeepLearningKurs/blob/main/notebooks/00_setup_test.ipynb)

Ein deutschsprachiger Kurs für einen umfassenden Einstieg in Deep Learning: von den mathematischen und konzeptionellen Grundlagen bis zur praktischen Entwicklung moderner neuronaler Netze mit Python, TensorFlow/Keras und PyTorch.

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

- Entwicklung eigener Deep-Learning-Modelle mit Python, TensorFlow/Keras und PyTorch
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
| Pillow | Laden, Speichern und Erzeugen einfacher Bilddateien |
| scikit-image | Paketlokale Beispielbilder und Bildtransformationen ohne externe Datensatzdownloads |
| SciPy | Wissenschaftliche Verfahren und Optimierung |
| scikit-learn | Datensplits, Metriken und klassische ML-Hilfsfunktionen |
| TensorFlow/Keras | Definition, Training und Evaluation neuronaler Netze |
| TensorBoard | Analyse und Monitoring des Trainingsprozesses |
| PyTorch | Tensoren, Autograd, explizite Trainingsloops und CNNs mit einfacher CPU/GPU-Steuerung |
| Torchvision | Bilddaten, Bildtransformationen und vortrainierte Vision-Modelle |
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
python -m pip install -r requirements.txt
```

Danach **genau eine** PyTorch-Variante installieren. Für NVIDIA-GPU unter Windows/Linux:

```bash
python -m pip install -r requirements-torch-cu126.txt
```

CPU-only unter Windows/Linux:

```bash
python -m pip install -r requirements-torch-cpu.txt
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
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

Danach **genau eine** PyTorch-Variante installieren. Für NVIDIA-GPU unter Windows/Linux:

```bash
python -m pip install -r requirements-torch-cu126.txt
```

CPU-only unter Windows/Linux:

```bash
python -m pip install -r requirements-torch-cpu.txt
```

## Setup testen

Starte Jupyter und öffne das Setup-Test-Notebook:

```bash
jupyter notebook notebooks/00_setup_test.ipynb
```

Alternativ kann das Notebook direkt in Google Colab geöffnet werden:

[![Setup-Test in Colab öffnen](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Y-Robin/DeepLearningKurs/blob/main/notebooks/00_setup_test.ipynb)


## Tag-1-2-Notebooks

Die praktischen Tag-1-2-Inhalte liegen in `notebooks/Day_1_2/` als kleine, einzeln ausführbare Einheiten. Die Reihenfolge folgt den Vortragsfolien:

- `notebooks/Day_1_2/01_tag_1_2_daten_samples_ausreisser_korrelation.ipynb`: Eingangsdaten, Sample-Formen, Ausreißer, Korrelation und Klassifikationsdaten untersuchen.
- `notebooks/Day_1_2/02_tag_1_2_regression_mietpreise.ipynb`: interaktive Regression mit einem zusammenhängenden Mietpreis-Datensatz.
- `notebooks/Day_1_2/03_tag_1_2_klassifikation_metriken.ipynb`: Klassifikation mit 1D-Verteilungen, ROC, Confusion Matrix, Precision und Recall.
- `notebooks/Day_1_2/04_tag_1_2_train_valid_test_kreuzvalidierung.ipynb`: 70/10/20-Split, Kreuzvalidierung und Polynomgrad-Tuning.
- `notebooks/Day_1_2/05_tag_1_2_training_loss_regularisierung.ipynb`: Training, Loss, Bias-Variance und Regularisierung.
- `notebooks/Day_1_2/06_tag_1_2_unueberwachtes_lernen_clustering.ipynb`: Unüberwachtes Lernen und Clustering.
- `notebooks/Day_1_2/07_tag_1_2_reinforcement_learning_mini_pong.ipynb`: Reinforcement Learning mit Mini-Pong.
- `notebooks/Day_1_2/Übungen/01_tag_1_2_uebung_regression_supervised.ipynb`: längere betreute Regressionsübung mit Rohdatenanalyse, Ausreißern, Korrelationen, linearer Regression, Regularisierung, Validierung und Regressionsmetriken.
- `notebooks/Day_1_2/Übungen/02_tag_1_2_uebung_klassifikation_supervised.ipynb`: längere betreute Klassifikationsübung mit Rohdatenanalyse, Ausreißern, Korrelationen, logistischer Regression, Regularisierung, Validierung, Confusion Matrix und Klassifikationsmetriken.

## Tag-3-5-Notebooks

Die praktischen Inhalte zum zweiten Kursblock liegen in `notebooks/Day_3_5/`. Die Beispiele reichen vom einzelnen Neuron bis zu TensorFlow/Keras-Pipelines:

- `notebooks/Day_3_5/01_tag_3_5_neuron_scratch_klassifikation.ipynb`: ein einzelnes Neuron ohne Deep-Learning-Bibliothek bauen, manuell per Slider tunen und trainieren.
- `notebooks/Day_3_5/02_tag_3_5_gradient_descent_visualisierung.ipynb`: Gradient Descent und Lernrate interaktiv visualisieren.
- `notebooks/Day_3_5/03_tag_3_5_lokale_minima_lernrate.ipynb`: lokale Minima und Lernrate in einer nichtkonvexen Loss-Landschaft.
- `notebooks/Day_3_5/04_tag_3_5_keras_einstieg_training.ipynb` bis `12_tag_3_5_batchsize_epochen.ipynb`: kompakte TensorFlow/Keras-Beispiele zu Einstieg, MLP, Aktivierungen, Spezialschichten, Skip Connections, Initialisierung, Loss/Regularisierung, Optimierung, Lernrate, Early Stopping, Batch Size und Epochen.

## Tag-6-8-Notebooks

Die praktischen Inhalte für den Computer-Vision-Block liegen in `notebooks/Day_6_8/`. Die Beispiele verwenden PyTorch statt TensorFlow, damit CPU/GPU-Wechsel in Colab und auf Windows-Systemen einfacher nachvollziehbar bleiben. Die neue Reihenfolge geht von PyTorch-Grundlagen und Bilddaten über Filter, Pooling, Training, Tuning, Regularisierung, Skip Connections, Speichern/Laden und XAI bis zu Transfer Learning:

- `notebooks/Day_6_8/00_tag_6_8_optionale_datensaetze_vorbereiten.ipynb`: lädt CIFAR-10 (Train und Test) einmalig in `datasets/`; weitere Datensätze lassen sich gezielt auswählen.
- `notebooks/Day_6_8/01_tag_6_8_intro_pytorch_setup_gpu.ipynb`: PyTorch-Intro mit MLP, Custom-Aktivierung, Klasse, `forward`, Loss, Optimizer, L2, Lernrate, `train_step`, `train/eval/no_grad`, Speichern/Laden.
- `notebooks/Day_6_8/02_tag_6_8_bilder_laden_erstellen_formate.ipynb`: 10x10-Graustufenball als Matrix, RGB-Bild, PNG/JPEG-Vergleich, Modellformat.
- `notebooks/Day_6_8/03_tag_6_8_bilder_als_tensoren_pytorch.ipynb`: Bildtensoren, `NCHW`, CPU-Plotting, `device`, Kernel-Crash-Hinweis.
- `notebooks/Day_6_8/04_tag_6_8_filter_visualisieren_featuremaps.ipynb`: Ziffer mit Label plus größeres Graustufenbild, Filter und Feature Maps in Graustufe.
- `notebooks/Day_6_8/05_tag_6_8_conv2d_filter_featuremaps_detail.ipynb`: `Conv2d` detailliert: Filter, Bias, ReLU, Feature Maps und Parameteranzahl.
- `notebooks/Day_6_8/06_tag_6_8_pooling_methoden_padding_invarianz.ipynb`: Pooling-Inputs/-Outputs, `F.pad`, Padding im Pooling, Positionsinvarianz.
- `notebooks/Day_6_8/07_tag_6_8_cnn_einfach_bauen_trainieren.ipynb`: CNN direkt mit `nn.Sequential`, Training, Bildvorhersagen, Confusion Matrix, Feature Maps.
- `notebooks/Day_6_8/08_tag_6_8_hyperparameter_gridsearch_performance.ipynb`: Grid Search über Kernel, Pooling, Filteranzahl, Dropout; Accuracy, Parameter und Zeit visualisieren.
- `notebooks/Day_6_8/09_tag_6_8_augmentation_regularisierung_lokale_bilder.ipynb`: CIFAR-10-Vergleich von Baseline, Regularisierung und Augmentation – mit Lernkurven, Testbewertung und Ergebnisbildern.
- `notebooks/Day_6_8/10_tag_6_8_skip_connections_direkt_und_resblock_trainiert.ipynb`: Skip Connection direkt im Netz, Residual Block, beide Modelle trainieren und einordnen.
- `notebooks/Day_6_8/11_tag_6_8_modelle_speichern_laden_custom_pytorch.ipynb`: Custom-Modul, Checkpoint, Laden, identische Logits prüfen, Bildvorhersagen und Confusion Matrix.
- `notebooks/Day_6_8/12_tag_6_8_xai_overfitting_spurious_logo.ipynb`: CIFAR-10-Beispiel zu Overfitting auf ein Logo: drei kontrollierte Testbedingungen, lokale Saliency-Overlays mehrerer Einzelbilder und eine gegenfaktische Probe mit/ohne Logo.
- `notebooks/Day_6_8/13_tag_6_8_transfer_learning_head_ersetzen.ipynb`: CIFAR-10-Transfer von fünf auf fünf Klassen mit neuem Head, Scratch-Vergleich, Fine-Tuning und online geladenem ImageNet-ResNet-18.

## Tag-9-Notebooks

Der nächste Computer-Vision-Block führt anhand eines absichtlich kleinen Ein-Objekt-Datensatzes in Objekterkennung ein. Er trennt sichtbar zwischen Bild-Input, Bounding-Box-Label, Anker-Vorhersagen, Loss und Non-Maximum Suppression (NMS):

- `notebooks/Day_9/00_tag_9_datensatz_vorbereiten.ipynb`: lädt den kleinen, realen Penn-Fudan-Pedestrian-Datensatz (rund 51 MB) herunter, leitet Bounding Boxes aus den Originalmasken ab und erzeugt einen reproduzierbaren Ein-Person-Split.
- `notebooks/Day_9/01_tag_9_objekterkennung_einfache_anker_nms.ipynb`: trainiert einen transparenten 4×4-Anker-Detektionskopf auf den echten Personenfotos mit einem vortrainierten ResNet-18-Backbone, Augmentation, Regularisierung, Fine-Tuning und Early Stopping; visualisiert Input/Label, einzelne Anker-Scores und Boxen, Loss, Kandidaten und NMS.

Für PyTorch wird nach der Basisinstallation **genau eine** der beiden Varianten installiert:

```bash
# NVIDIA-GPU unter Windows/Linux
python -m pip install -r requirements-torch-cu126.txt

# CPU-only unter Windows/Linux
python -m pip install -r requirements-torch-cpu.txt
```

Die CUDA-12.6-Wheels bringen die benötigte CUDA-Laufzeit mit; entscheidend ist ein aktueller, kompatibler NVIDIA-Treiber. Auf nativem Windows nutzt das hier festgelegte aktuelle TensorFlow-Paket die CPU. Für TensorFlow-GPU ist WSL2 erforderlich; die NVIDIA-GPU-Unterstützung dieses Kurses erfolgt daher über PyTorch.

## Repository-Struktur

```text
.
├── README.md
├── requirements.txt
├── requirements-torch-cpu.txt
├── requirements-torch-cu126.txt
├── environment.yml
├── notebooks/
│   ├── 00_setup_test.ipynb
│   ├── Day_1_2/
│   │   ├── README.md
│   │   ├── 01_tag_1_2_daten_samples_ausreisser_korrelation.ipynb
│   │   ├── 02_tag_1_2_regression_mietpreise.ipynb
│   │   ├── 03_tag_1_2_klassifikation_metriken.ipynb
│   │   ├── 04_tag_1_2_train_valid_test_kreuzvalidierung.ipynb
│   │   ├── 05_tag_1_2_training_loss_regularisierung.ipynb
│   │   ├── 06_tag_1_2_unueberwachtes_lernen_clustering.ipynb
│   │   ├── 07_tag_1_2_reinforcement_learning_mini_pong.ipynb
│   │   └── Übungen/
│   │       ├── 01_tag_1_2_uebung_regression_supervised.ipynb
│   │       └── 02_tag_1_2_uebung_klassifikation_supervised.ipynb
│   ├── Day_3_5/
│   │   ├── README.md
│   │   ├── 01_tag_3_5_neuron_scratch_klassifikation.ipynb
│   │   ├── 02_tag_3_5_gradient_descent_visualisierung.ipynb
│   │   ├── 03_tag_3_5_lokale_minima_lernrate.ipynb
│   │   ├── 04_tag_3_5_keras_einstieg_training.ipynb
│   │   ├── 05_tag_3_5_mlp_dense_hyperparameter.ipynb
│   │   ├── 06_tag_3_5_aktivierungsfunktionen.ipynb
│   │   ├── 07_tag_3_5_batchnorm_dropout.ipynb
│   │   ├── 08_tag_3_5_skip_connections_functional_api.ipynb
│   │   ├── 09_tag_3_5_initialisierungen.ipynb
│   │   ├── 10_tag_3_5_loss_regularisierung.ipynb
│   │   ├── 11_tag_3_5_optimierung_lr_scheduler_early_stopping.ipynb
│   │   ├── 12_tag_3_5_batchsize_epochen.ipynb
│   │   ├── 13_tag_3_5_modelle_speichern_laden.ipynb
│   │   ├── 14_tag_3_5_tensorflow_grundlagen_cpu_gpu.ipynb
│   │   ├── 15_tag_3_5_custom_training_loop_gradient_tape.ipynb
│   │   ├── 16_tag_3_5_eigene_metriken_aktivierungen_losses.ipynb
│   │   ├── 17_tag_3_5_tabular_pipeline_preprocessing_tfrecords.ipynb
│   │   ├── 18_tag_3_5_dateien_streamen_tfdata.ipynb
│   │   └── Übungen/
│   │       ├── 01_tag_3_5_uebung_tensorflow_basics_ohne_training.ipynb
│   │       ├── 02_tag_3_5_uebung_daten_preprocessing_dos_donts.ipynb
│   │       ├── 03_tag_3_5_uebung_fashion_mnist_modellwahl.ipynb
│   │       └── 04_tag_3_5_uebung_online_titanic_custom_keras.ipynb
│   └── Day_6_8/
│       ├── README.md
│       ├── 00_tag_6_8_optionale_datensaetze_vorbereiten.ipynb
│       ├── 01_tag_6_8_intro_pytorch_setup_gpu.ipynb
│       ├── 02_tag_6_8_bilder_laden_erstellen_formate.ipynb
│       ├── 03_tag_6_8_bilder_als_tensoren_pytorch.ipynb
│       ├── 04_tag_6_8_filter_visualisieren_featuremaps.ipynb
│       ├── 05_tag_6_8_conv2d_filter_featuremaps_detail.ipynb
│       ├── 06_tag_6_8_pooling_methoden_padding_invarianz.ipynb
│       ├── 07_tag_6_8_cnn_einfach_bauen_trainieren.ipynb
│       ├── 08_tag_6_8_hyperparameter_gridsearch_performance.ipynb
│       ├── 09_tag_6_8_augmentation_regularisierung_lokale_bilder.ipynb
│       ├── 10_tag_6_8_skip_connections_direkt_und_resblock_trainiert.ipynb
│       ├── 11_tag_6_8_modelle_speichern_laden_custom_pytorch.ipynb
│       ├── 12_tag_6_8_xai_overfitting_spurious_logo.ipynb
│       ├── 13_tag_6_8_transfer_learning_head_ersetzen.ipynb
│       └── Übungen/
│           ├── 01_tag_6_8_uebung_bilddaten_filter_pooling.ipynb
│           ├── 02_tag_6_8_uebung_cnn_training_gridsearch.ipynb
│           ├── 03_tag_6_8_uebung_augmentation_regularisierung_xai.ipynb
│           ├── 04_tag_6_8_uebung_speichern_laden_custom.ipynb
│           └── 05_tag_6_8_uebung_transfer_eigene_bilder.ipynb
└── LICENSE
```

## Lizenz

Dieses Repository steht unter der Apache License 2.0. Details stehen in der Datei `LICENSE`.

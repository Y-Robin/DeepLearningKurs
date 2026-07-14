# Day 6-8 Notebooks

Die Beispiele für Woche 2 wechseln bewusst auf PyTorch. Die Reihenfolge geht von Setup und Bilddaten über Filter, Pooling, CNN-Training, Tuning, Regularisierung, Skip Connections, Speichern/Laden und XAI bis zu Transfer Learning.

## PyTorch und GPU

`requirements.txt` und `environment.yml` können nicht zuverlässig automatisch erkennen, ob auf dem jeweiligen Rechner eine passende NVIDIA-GPU vorhanden ist und dann abhängig davon einen anderen PyTorch-Wheel-Index verwenden. Deshalb gibt es einen expliziten zweiten Schritt für Windows/Linux mit CUDA 12.6:

```bash
pip install --upgrade -r requirements-torch-cu126.txt
```

Das entspricht:

```bash
pip3 install torch torchvision --index-url https://download.pytorch.org/whl/cu126
```

Wenn `import torch` den Jupyter-Kernel beendet, ist das normalerweise ein Installationsproblem, zum Beispiel gemischte CPU-/CUDA-Wheels oder ein unpassender NVIDIA-Treiber. Dann PyTorch sauber neu installieren und den Kernel neu starten.

## Beispiele

| Nr. | Notebook | Fokus |
| --- | --- | --- |
| 00 | `00_tag_6_8_optionale_datensaetze_vorbereiten.ipynb` | lädt CIFAR-10 (Train und Test) einmalig nach `datasets/`; die Beispiele 09 und 13 verwenden anschließend nur diesen lokalen Cache |
| 01 | `01_tag_6_8_intro_pytorch_setup_gpu.ipynb` | PyTorch-Intro mit MLP: Layer, Custom-Aktivierung, Klasse, `forward`, Loss, Optimizer, L2, Lernrate, `train_step`, `train/eval/no_grad`, Speichern/Laden |
| 02 | `02_tag_6_8_bilder_laden_erstellen_formate.ipynb` | 10x10-Graustufenball als Matrix, RGB-Bild, PNG/JPEG-Vergleich, Modellformat |
| 03 | `03_tag_6_8_bilder_als_tensoren_pytorch.ipynb` | Bildtensoren, `NCHW`, CPU-Plotting, `device`, Kernel-Crash-Hinweis |
| 04 | `04_tag_6_8_filter_visualisieren_featuremaps.ipynb` | Ziffer mit Label plus größeres Graustufenbild, Filter visualisieren, Feature Maps in Graustufe |
| 05 | `05_tag_6_8_conv2d_filter_featuremaps_detail.ipynb` | `Conv2d` im Detail: Filter, Bias, ReLU, Feature Maps und Parameteranzahl |
| 06 | `06_tag_6_8_pooling_methoden_padding_invarianz.ipynb` | Pooling-Inputs/-Outputs, Max/Average/Min, `F.pad`, Padding im Pooling, Positionsinvarianz |
| 07 | `07_tag_6_8_cnn_einfach_bauen_trainieren.ipynb` | CNN direkt mit `nn.Sequential`, Training, Bildvorhersagen, Confusion Matrix, Feature Maps |
| 08 | `08_tag_6_8_hyperparameter_gridsearch_performance.ipynb` | Grid Search über Kernel, Pooling, Filteranzahl, Dropout; Accuracy, Parameter und Zeit visualisieren |
| 09 | `09_tag_6_8_augmentation_regularisierung_lokale_bilder.ipynb` | CIFAR-10 mit 8.000 Trainingsbildern: Baseline, Regularisierung, Augmentation, Lernkurven, Testbilder und Confusion Matrix |
| 10 | `10_tag_6_8_skip_connections_direkt_und_resblock_trainiert.ipynb` | Skip Connection direkt im Netz, Residual Block, beide Modelle trainieren und einordnen |
| 11 | `11_tag_6_8_modelle_speichern_laden_custom_pytorch.ipynb` | Custom-Modul, Checkpoint, Laden, identische Logits prüfen, Bildvorhersagen und Confusion Matrix |
| 12 | `12_tag_6_8_xai_overfitting_spurious_logo.ipynb` | Overfitting auf Wasserzeichen/Logo, Bias-Test, Saliency und globale Heatmap |
| 13 | `13_tag_6_8_transfer_learning_head_ersetzen.ipynb` | CIFAR-10-Transfer: fünf zu fünf Klassen, neuer Head, Scratch vs. Transfer, Fine-Tuning sowie online geladenes ImageNet-ResNet-18 |

## Übungen

Die Übungen bleiben als längere Nachmittagsblöcke angelegt und werden nach der Beispielkorrektur separat weiter ausgearbeitet.

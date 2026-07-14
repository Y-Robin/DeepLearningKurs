# Tag 9 – Objekterkennung und Segmentierung

| Notebook | Inhalt |
| --- | --- |
| `00_tag_9_datensatz_vorbereiten.ipynb` | Lädt den kleinen Penn-Fudan-Pedestrian-Datensatz einmalig herunter und erzeugt reproduzierbare Splits. |
| `01_tag_9_objekterkennung_einfache_anker_nms.ipynb` | Erkennt Personen als Bounding Boxes mit einfachen Ankern und NMS. |
| `02_tag_9_semantische_segmentierung_resnet_unet.ipynb` | Segmentiert Personen pixelweise mit einem vortrainierten ResNet-18-Backbone und einem neuen Decoder. |
| `03_tag_9_instanzsegmentierung_mask_rcnn.ipynb` | Erkennt jede Person mit Bounding Box und eigener Pixelmaske – Instanzsegmentierung mit vortrainiertem Mask R-CNN. |

Die Notebooks 01, 02 und 03 setzen jeweils voraus, dass Notebook 00 zuvor ausgeführt wurde. Notebook 03 verwendet dieselben unveränderten Penn-Fudan-Originalmasken wie Notebook 02, behält aber die einzelnen Personen-IDs bei.

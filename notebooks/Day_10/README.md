# Tag 10 – Bildgenerierung: GANs und Diffusion

| Notebook | Inhalt |
| --- | --- |
| `01_tag_10_gan_fashion_mnist.ipynb` | Trainiert ein kleines DCGAN selbst auf Fashion-MNIST. Es zeigt das adversariale Zusammenspiel aus Generator und Diskriminator. |
| `02_tag_10_diffusion_unet_embeddings_lokal.ipynb` | Verbindet Diffusion, U-Net und Text-Embeddings mit einer lokalen Stable-Diffusion-Inferenz über Hugging Face. |
| `03_tag_10_openai_api_bildgenerierung.ipynb` | Erzeugt ein Bild über die OpenAI Images API; der Schlüssel wird sicher aus einer lokalen `.env`-Datei gelesen. |
| `Übungen/01_tag_10_uebung_prompt_experiment.ipynb` | Kontrolliertes Prompt-Experiment: Bildbriefing, drei gezielte Variationen, lokale oder API-basierte Erzeugung und Qualitätsbewertung. |

## Hardware-Einschätzung: RTX 3080

Eine RTX 3080 (typisch 10 GB VRAM) ist für diesen Tag gut geeignet:

| Aufgabe | Einstellung im Kurs | Einschätzung |
| --- | --- | --- |
| DCGAN auf Fashion-MNIST trainieren | 64×64, Batch-Größe 128 | problemlos |
| Stable Diffusion 1.5 erzeugen | 512×512, Batch-Größe 1, `float16`, 30 Schritte | lokal gut machbar |
| Stable Diffusion 1.5 feintrainieren | vollständiges Fine-Tuning | nicht sinnvoll auf 10 GB |
| Style-/Domänenanpassung | LoRA, 512×512, kleine Batches | mit Speicher-Optimierungen möglich |

Das Diffusionsnotebook verwendet `runwayml/stable-diffusion-v1-5`. Für dieses öffentliche Modell sind Anmeldung und Token nicht nötig, solange der Download ohne Fehler startet. Bei privaten oder zugriffsbeschränkten Hugging-Face-Modellen kann ein Login mit `hf auth login` bzw. ein Token erforderlich sein.

Beim ersten Lauf werden ungefähr 4–5 GB Modellgewichte nach `notebooks/Day_10/saved_models/stable-diffusion-v1-5/` geladen. Existiert dieser Ordner bereits, überspringt das Notebook den Download vollständig und arbeitet ohne Netzwerkanfrage daraus lokal. Dieser Ordner ist absichtlich nicht Teil von Git.

Die Notebook-Versionen in `requirements.txt` enthalten hierfür `diffusers`, `accelerate`, `safetensors`, `openai` und `python-dotenv`.

## OpenAI-API-Beispiel

Das dritte Notebook nutzt einen externen API-Aufruf und damit keine lokale GPU. Lege vor dem Start im Projektwurzelordner – neben `requirements.txt` – eine Datei `.env` an:

```text
API_TOKEN=xxxxx
```

Ersetze `xxxxx` durch deinen OpenAI-API-Schlüssel. Die Datei `.env` ist bereits in `.gitignore` und wird daher nicht eingecheckt. Sie darf weder geteilt noch in ein Notebook kopiert werden. Das Notebook liest den Schlüssel mit `python-dotenv`, zeigt ihn niemals an und speichert nur das erzeugte Bild unter `notebooks/Day_10/generated_images/`.

Die Bildgenerierung über die API ist kostenpflichtig und wird über das API-Konto abgerechnet. Das Beispiel verwendet das aktuelle Bildmodell `gpt-image-2`; ein vorhandenes ChatGPT-Abonnement ist davon getrennt.

# Tag 11 & 12 – Zeitreihen und Sequenzmodelle

| Notebook | Inhalt |
| --- | --- |
| `01_tag_11_12_zeitreihe_trainingssequenzen.ipynb` | Erzeugt eine künstliche, verrauschte Sinus-Zeitreihe, teilt sie chronologisch und wandelt sie in überlappende Eingabefenster `X` und Zielwerte `y` um. Interaktive Regler zeigen den Einfluss von Fensterlänge, Rauschen und Trainingsanteil. |
| `02_tag_11_12_ar_vorhersage.ipynb` | Berechnet Ein-Schritt-Prognosen mit einer festen autoregressiven Regel. Interaktive Regler machen Ordnung `p`, Gewichtung, Rauschen und die einzelnen Prognosebeiträge nachvollziehbar. |
| `03_tag_11_12_ar_zu_arma.ipynb` | Trainiert AR- und ARMA-Modelle auf einem chronologischen Trainingsabschnitt. Vergleicht mehrere Fensterlängen `p` und Fehlerordnungen `q` auf einem späteren Testbereich und zeigt die konkreten Eingaben einer Vorhersage. |
| `04_tag_11_12_rnn_hidden_state.ipynb` | Trainiert ein TensorFlow-`SimpleRNN` auf einer periodischen Zeitreihe für Ein-Schritt-Prognosen. Zeigt die Hidden States eines Fensters, den RNN-Loop und einen fortlaufenden Durchlauf ohne Reset. |
| `05_tag_11_12_rnn_ein_und_ausgabeformen.ipynb` | Verwendet denselben Sequenzdatensatz für Sequence-to-Vector-Klassifikation und Sequence-to-Sequence-Rekonstruktion. Zeigt Ziel- und Outputformen sowie beide Ergebnisse am selben Testbeispiel. |
| `06_tag_11_12_einfaches_und_gestapeltes_rnn.ipynb` | Vergleicht ein einfaches mit einem gestapelten RNN für dieselbe Ein-Schritt-Prognose. Bewertet Parameterzahl, Trainingszeit, Training-/Validierungsfehler und Testprognosen. |
| `07_tag_11_12_explodierende_gradient_clipping.ipynb` | Trainiert ein bewusst empfindliches RNN mit und ohne Gradient Clipping. Zeichnet Loss sowie rohe und tatsächlich angewendete Gradientennormen pro Update. |
| `08_tag_11_12_lstm_gates_untersuchen.ipynb` | Trainiert eine LSTM auf einer selektiven Merkaufgabe mit kleinen und großen Werten. Zeigt Gradienten und gelernte Gate-Gewichte und rechnet einen vollständigen Testdurchlauf bis zur Ausgabe numerisch nach. |
| `09_tag_11_12_gru_update_reset_gate.ipynb` | Untersucht Reset Gate und Update Gate einer GRU mit kontrollierten Gate-Werten. Rechnet vier Einzelszenarien und eine kurze Sequenz vollständig von Hand nach und visualisiert Kandidatenbildung, Update-Beiträge und Hidden States. |

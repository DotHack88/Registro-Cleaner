# 🧹 Registro Cleaner Avanzato

> Uno strumento con interfaccia grafica (GUI) per eliminare facilmente chiavi e valori dal registro di sistema Windows, con backup automatici e ripristino.

---

## 🚀 Funzionalità principali

- ✅ **Interfaccia intuitiva multischeda** con sezione Log integrata
- 🧩 **Supporto multiriga dinamico** (aggiungi/rimuovi righe su richiesta)
- 📥 **Importazione rapida** da riga completa (Root | Percorso | Valore)
- 💾 **Backup automatico prima di ogni cancellazione**
- ♻️ **Ripristino da file `.reg`**
- 🛡️ **Controllo permessi amministrativi**
- ⚙️ **Compatibile con Windows 10/11**

---

## 📸 Anteprima GUI

![screenshot](docs/screenshot.png)

---

## ✨ Come si usa

1. **Avvia il programma come amministratore**
2. Inserisci uno o più **valori da cancellare** nel formato:

# Registro-Cleaner
Root: HKEY_CURRENT_USER
Percorso: Software\Microsoft\Windows\CurrentVersion\Run
Valore (opzionale): nome_valore


Oppure incolla una riga completa come:

HKEY_CURRENT_USER | Software\Microsoft\Windows\CurrentVersion\Run | nome_valore


3. Premi `🧹 Elimina` per procedere  
   🔒 Un backup automatico `.reg` sarà generato prima della cancellazione.

---

## 💻 Requisiti

- Python 3.9+  
- Sistema operativo: **Windows**
- Moduli Python:
  - `tkinter`
  - `subprocess`
  - `winreg`
  - `threading`

---

## 🔧 Trasformare in `.exe`

Puoi creare un eseguibile con icona personalizzata usando [PyInstaller](https://pyinstaller.org/):

```bash
pyinstaller --noconsole --onefile --icon=icon.ico registro_cleaner_gui.py

⚠️ Avvisi

    🛑 L’uso improprio di questo tool può compromettere il sistema operativo.

    🧠 Effettua sempre un backup manuale del registro se non sei sicuro delle modifiche.

    ✔️ Il programma esegue già backup automatici prima di ogni eliminazione.

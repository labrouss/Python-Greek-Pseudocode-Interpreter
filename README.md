# 🐍 Διερμηνέας Ελληνικού Ψευδοκώδικα (ΕΑΠ)

  

Αυτό το repository περιέχει τον πηγαίο κώδικα Python για τον διερμηνέα που χρησιμοποιείται για την εκτέλεση προγραμμάτων Ψευδοκώδικα (ΕΑΠ - Ελληνικό Ανοικτό Πανεπιστήμιο).

Ο κώδικας αυτός είναι η βάση για τα μεταγλωττισμένα (compiled) εκτελέσιμα που παρέχονται στις εκδόσεις (releases) και χρησιμοποιούνται στην επέκταση VS Code.

  

--- 
## 🚀 Χαρακτηριστικά

* **Διερμηνέας Πηγαίου Κώδικα:** Βασισμένος στην Python, παρέχει την κύρια λογική εκτέλεσης.

* **Cross-Platform Builds:** Αυτοματοποιημένη δημιουργία εκτελέσιμων αρχείων για Windows, macOS και Linux μέσω GitHub Actions.

* **Αρχεία Εκδόσεων (Release Assets):** Κάθε έκδοση περιέχει τα εκτελέσιμα αρχεία που μπορούν να χρησιμοποιηθούν αυτόνομα ή να ενσωματωθούν σε άλλες εφαρμογές.
---
 

## ⚙️ Τρόπος Χρήσης (Αυτόνομη Εκτέλεση)

  

Μπορείτε να εκτελέσετε τον διερμηνέα με δύο τρόπους:

  

### 1. Εκτέλεση μέσω Python (Απαιτείται Python 3)

Εάν έχετε εγκατεστημένη την Python 3, μπορείτε να εκτελέσετε τον διερμηνέα απευθείας:

```bash
python interpreter.py <όνομα_αρχείου>.eap
```
### 2. Εκτέλεση μέσω Μεταγλωττισμένου Αρχείου
Τα μεταγλωττισμένα εκτελέσιμα παρέχονται σε κάθε Έκδοση (Release) του Repository.

  

Κατεβάστε το κατάλληλο αρχείο και τρέξτε το απευθείας.


|Λειτουργικό Σύστημα| Όνομα Αρχείου | Εκτέλεση |
|-------------------|---------------|----------|
|Windows | interpreter-win.exe | ./interpreter-win.exe <όνομα_αρχείου>.eap|
|macOS | interpreter-macos|./interpreter-macos <όνομα_αρχείου>.eap
|Linux| interpreter-linux |./interpreter-linux <όνομα_αρχείου>.eap|
------

### 🛠️ Ανάπτυξη & Μεταγλώττιση (Building)

**Δομή Αρχείων**
 
 Το repository περιέχει το κύριο αρχείο:
``interpreter.py `` : Ο βασικός κώδικας του διερμηνέα.

**Αυτόματη Μεταγλώττιση (CI/CD)**

Αυτή η διαδικασία είναι αυτοματοποιημένη χρησιμοποιώντας GitHub Actions και την βιβλιοθήκη PyInstaller. Κάθε φορά που γίνεται push ένα νέο tag (v*.*.*), τρέχει ο workflow:

1. Το PyInstaller δημιουργεί τα μονολιθικά (onefile) εκτελέσιμα για κάθε πλατφόρμα.

2. Τα εκτελέσιμα αρχεία ανεβαίνουν ως Assets στη νέα GitHub Release.

**Τοπική Μεταγλώττιση**


Για να δημιουργήσετε ένα εκτελέσιμο τοπικά, βεβαιωθείτε ότι έχετε εγκατεστημένη την Python και το PyInstaller:

```Bash
#Εγκατάσταση PyInstaller
pip install pyinstaller

#Δημιουργία Windows Executable
pyinstaller --onefile --name interpreter-win interpreter.py
  
#Δημιουργία Linux Executable
pyinstaller --onefile --name interpreter-linux interpreter.py
```

**🤝 Συνεισφορές** 

Οι συνεισφορές είναι ευπρόσδεκτες! Παρακαλώ ανατρέξτε στο αρχείο ``CONTRIBUTING.md``  για λεπτομέρειες σχετικά με την υποβολή pull requests.

 **📜 Άδεια Χρήσης (License)**

Ο κώδικας κυκλοφορεί υπό την Άδεια MIT.

** 🛠️ Local Compilation **

To create an executable locally, ensure you have Python and PyInstaller installed:

```Bash
#Install PyInstaller
pip install pyinstaller
#Create Windows Executable
pyinstaller --onefile --name interpreter-win interpreter.py
#Create Linux/macOS Executable
pyinstaller --onefile --name interpreter-linux interpreter.py
```

# 📚 Library App

### A simple Python & Tkinter project for managing a small digital library

---

## 🧠 Overview
**Library App** is a lightweight educational project that simulates a basic library management system.  
It allows users to add and remove books, register readers, issue and return books, and save data to a local JSON file.  

The app demonstrates:
- Object-Oriented Programming (OOP) principles  
- GUI creation with **Tkinter**  
- Data persistence with **JSON**  
- Modular code structure separating logic and interface  

---

## 🏗️ Project Structure
```
library_app/
├── library.py          # Entry point – connects logic and UI
├── library_logic.py    # Core business logic (books, readers, operations)
├── library_ui.py       # Graphical interface (Tkinter)
└── library_data.json   # Data file created automatically
```

---

## ⚙️ Features
✅ Add / remove books and readers  
✅ Issue and return books  
✅ Save and load all data to JSON  
✅ Simple and intuitive GUI  

---

## 🧩 How It Works

**`library_logic.py`** — defines the `Library` class responsible for all data operations:
```python
def add_book(self, title, author, year, genre, copies):
    self.books.append({
        "title": title, "author": author, "year": year,
        "genre": genre, "copies": int(copies)
    })
```

**`library_ui.py`** — contains the `LibraryApp` class that builds the Tkinter interface and links buttons to logic methods.  

**`library.py`** — initializes the main window and runs the app:
```python
if __name__ == "__main__":
    library = Library()
    root = tk.Tk()
    root.title("Library")
    app = LibraryApp(root, library)
    root.mainloop()
```

---

## 💾 Data Format
All data is stored in `library_data.json`:
```json
{
  "books": [
    {"title": "1984", "author": "George Orwell", "year": "1949", "genre": "Dystopia", "copies": 3}
  ],
  "readers": [
    {"name": "Ivan", "surname": "Petrov", "ticket_number": "A001"}
  ],
  "issued_books": {
    "1984": ["A001"]
  }
}
```

---

## 🚀 How to Run
1. Make sure you have **Python 3.10+**
2. Clone the repository:
   ```bash
   git clone https://github.com/BagroDeRose/library_app.git
   cd library_app
   ```
3. Run the app:
   ```bash
   python library.py
   ```

---

## 💡 Possible Improvements
- Add search and filter features  
- Implement statistics and reports  
- Replace JSON with a SQLite database  

---

**Simple. Functional. Educational.**

Сделано давно и для универа

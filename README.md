
# 🎴 AI Engineering Flashcards  
A simple, interactive flashcard study tool built with **HTML**, **CSS**, and **JavaScript**.  
This project demonstrates core JavaScript fundamentals including DOM manipulation, event handling, state management, and dynamic UI updates.

---

## 📌 Features

### ✔ Dynamic Flashcard System  
- Uses a **single flashcard container**  
- Updates question, answer, and progress using `textContent`  
- Tracks the current card with a `let currentIndex` variable  

### ✔ Show/Hide Answer  
- Answer is hidden by default  
- Revealed using `style.display = "block"`  
- Hidden using `style.display = "none"`  

### ✔ Next Question Navigation  
- Moves to the next card using the modulo operator:  
  ```js
  currentIndex = (currentIndex + 1) % questions.length;
  ```
- Automatically hides the answer when switching cards  
- Updates progress indicator (`Card X of Y`)  

### ✔ Clean, Minimal UI  
- Simple styling for readability  
- Responsive layout centered on the page  

---

## 📂 Project Structure

```
flashcards/
│
├── index.html
└── (optional) styles.css
```

All logic is contained within `index.html` for simplicity.

---

## 🧠 How It Works

### **1. Flashcard Data**
Questions and answers are stored in two arrays:

```js
const questions = [...];
const answers = [...];
```

### **2. State Tracking**
The current card index is stored in:

```js
let currentIndex = 0;
```

### **3. Dynamic Content Updates**
The flashcard UI updates using:

```js
questionEl.textContent = questions[currentIndex];
answerEl.textContent = answers[currentIndex];
progressEl.textContent = `Card ${currentIndex + 1} of ${questions.length}`;
```

### **4. Show/Hide Answer**
```js
answerEl.style.display = "block"; // show
answerEl.style.display = "none";  // hide
```

### **5. Next Question Logic (Modulo Looping)**
```js
currentIndex = (currentIndex + 1) % questions.length;
updateCard();
```

This ensures the flashcards loop back to the beginning after the last card.

---

## 🚀 Running the Project

1. Clone or download the repository  
2. Open `index.html` in any web browser  
3. Use the buttons to:
   - Show Answer  
   - Hide Answer  
   - Move to the Next Question  

No build tools or dependencies required.

---

## 🎯 Learning Objectives

This project demonstrates:

- DOM selection (`getElementById`)  
- Updating UI with `textContent`  
- Event listeners (`addEventListener`)  
- Conditional rendering with `style.display`  
- Using modulo for looping logic  
- Managing application state with variables  

Perfect for beginners learning JavaScript fundamentals.

---

## 📸 Preview (Optional)

Add a screenshot here if you want:

```
![Flashcard Preview](screenshot.png)
```

---

## 🔧 Future Enhancements

- Previous Question button  
- Shuffle mode  
- Flip animation  
- Dark mode toggle  
- Keyboard shortcuts (← → space)  
- Score tracking (“Correct / Incorrect”)  

---


  
- A **GitHub Pages deployment guide**

Just tell me what direction you want to take your flashcard app next.

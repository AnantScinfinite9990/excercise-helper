# 🛋️ EXCERCISE HELPER and Lazy Workout Generator

> *Tell us how lazy you are. We'll handle the rest.*

A simple, no-nonsense web app that generates a workout plan based on how much time you have and where you are — bed, desk, or floor. No equipment. No excuses. No gym membership.

Built with plain HTML, CSS, and JavaScript. 
---

## 🎯 What It Does

1. You pick **how many minutes** you have (5, 10, or 20)
2. You pick **where you are** (bed, desk, or floor)
3. Hit the button → get a full workout plan instantly

---

## ✨ Features

- 9 unique workout plans (3 locations × 3 time slots)
- Random motivational quote after each generation
- Smooth animations on results
- Fully responsive — works on mobile too
- Dark theme with no eye strain
- Zero dependencies — just one `.html` file

---

## 🚀 How to Run

No installation needed. Seriously.

```bash

double-click index.html



## 📁 Project Structure

```
```

Everything — HTML, CSS, and JavaScript — is in one single file. Great for beginners to read and understand end to end.

---

## 🧠 How the Code Works

The entire logic is one JavaScript object and one function.

**The workout data:**
```js
const workouts = {
  bed: {
    5:  [ { icon, name, detail }, ... ],
    10: [ ... ],
    20: [ ... ],
  },
  desk: { ... },
  floor: { ... },
}
```

**The generate function:**
```js
function generate() {
  const time = document.getElementById('time').value;
  const loc  = document.getElementById('location').value;

  const exercises = workouts[loc][parseInt(time)]; // ← the whole brain
  // then loop through and display them
}
```

That's it. The rest is just styling.

---

## 🛠️ How to Customize

**Add a new location** (e.g. "kitchen"):
```js
kitchen: {
  5:  [ { icon: "🍳", name: "Counter Pushups", detail: "3 × 10 reps" } ],
  10: [ ... ],
  20: [ ... ],
}
```
Then add it to the dropdown in the HTML:
```html
<option value="kitchen">In the kitchen</option>
```

**Add a new motivational quote:**
```js
const quotes = [
  "You're not lazy. You're energy-efficient. 🌿",
  "Add your quote here! 🎉",   // ← just add a new line
];
```

---

## 💡 Ideas to Extend It

- [ ] Add a built-in **rest timer** between exercises
- [ ] Add a **"surprise me"** button that picks random time + location
- [ ] Save workout history to **localStorage**
- [ ] Add a **difficulty** selector (easy / medium / hard)
- [ ] Turn it into a **PWA** so it works offline on mobile

---

## 🤝 Contributing

This was built for a hackathon by a beginner, for beginners. Contributions welcome!

1. Fork the repo
2. Make your changes in `index.html`
3. Open a pull request with a short description of what you changed

Please keep it simple — the goal is that any beginner can read and understand the entire codebase in one sitting.

---

## 📄 License

GNU Public License 3.0

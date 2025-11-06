# 🤖 Week 4 — Machine Learning with Teachable Machine
### 😊 Train Your First AI Model & 🎨 Build Something Unique

Welcome to **Week 4: Machine Learning** — where you'll create your own AI models that can recognize images in real-time using your webcam!  
You'll learn to train machine learning models without writing complex code, integrate them into web applications using **TensorFlow.js**, and see your models come to life in the browser.

---

## 📦 What's Inside

- `index.html` — starter template with TensorFlow.js setup (Tailwind CSS included)
- `README.md` — this file with all instructions
- `my_model/` — folder for your exported models (you'll create this)

---

## 🧩 Lesson Overview

| Part | Theme | Focus |
|------|--------|--------|
| 😊 **Part 1** | Smiles & Frowns | Learn the basics: train a facial expression model, export it, and integrate it into your webpage |
| 🎨 **Part 2** | Your Choice | Create your own model with classes you choose — hand gestures, objects, poses, or anything you can imagine! |

You'll complete both parts **in order**. Part 1 teaches you the workflow, and Part 2 lets you apply what you learned to create something unique.

---

## 🚀 Getting Started

### 1️⃣ Open the Repository

1. Visit the class GitHub link:  
   ```
   https://github.com/The-Pritzker-Tech-Talent-Labs/DC_Fall-Week-4-Machine-Learning
   ```
   *(Update this URL with your actual repository link)*

2. **Fork this repo** (top-right button) and open in **GitHub Codespace**
   - Click the green **"Code"** button → select **Codespaces** tab → **"Create codespace on main"**
   - Wait for it to load (it'll look like VS Code in your browser)

---

### 2️⃣ Start a Local Server

Since webcams require a secure connection, you'll need to run a local server:

**In your Codespace terminal, type:**
```bash
npx live-server
```

After a few seconds, a preview panel will open. Every time you save your file, the page refreshes automatically.

> 💡 *Note:* This project uses **JavaScript and TensorFlow.js** — everything runs in your browser! No Python or complex setup needed.

---

### 3️⃣ Visit Teachable Machine

Go to **[https://teachablemachine.withgoogle.com/](https://teachablemachine.withgoogle.com/)** and click **"Get Started"**

This is where you'll create and train your models. Bookmark it — you'll be coming back here!

---

## 📋 Instructions

### 😊 Part 1 — Smiles & Frowns (Guided Project)

**Goal:** Create your first machine learning model that recognizes facial expressions.

#### Step 1: Create Your Model

1. On Teachable Machine, select **"Image Project"**
2. You'll see **Class 1** and **Class 2** — rename them:
   - Click **"Class 1"** → rename to **"Smile"**
   - Click **"Class 2"** → rename to **"Frown"**
   - Click **"Add a class"** → add **"Neutral"** (optional, but recommended)

#### Step 2: Collect Training Data

For each class, you'll need to collect samples:

1. **Click on "Smile"** class
2. Click **"Webcam"** to use your camera
3. **Hold down the spacebar** while making a clear smile
4. Collect **at least 50-100 samples** (you'll see the count increase)
5. Try different angles, lighting, and expressions
6. Repeat for **"Frown"** and **"Neutral"** classes

> 💡 **Tips for better models:**
> - Include variety: different lighting, angles, backgrounds
> - Make clear, distinct expressions
> - Collect samples in different locations if possible

#### Step 3: Train Your Model

1. Click the **"Train Model"** button
2. Wait for training to complete (usually 30-60 seconds)
3. Test your model in the **Preview** panel:
   - Make different expressions and see if it recognizes them correctly
   - If it's not accurate, go back and add more training samples

#### Step 4: Export Your Model

1. Click **"Export Model"**
2. Choose **"Tensorflow.js"** tab
3. Select **"Download"** (we'll use the downloaded version)
4. Extract the ZIP file
5. Rename the extracted folder to `smiles_frowns_model` (or remember the exact name)

#### Step 5: Add Model to Your Project

1. In your Codespace, drag the `smiles_frowns_model` folder into your `week_4_lesson` directory
2. Open `index.html` in the editor
3. Find the section marked:
   ```html
   <!-- START: Paste your Teachable Machine code here -->
   ```
4. In Teachable Machine, after clicking "Export Model", you'll see a code snippet. **Copy the entire snippet** (it includes the HTML, scripts, and JavaScript)
5. **Replace the placeholder code** in `index.html` with your copied snippet
6. **Important:** Update the `URL` variable to match your folder name:
   ```javascript
   const URL = "./smiles_frowns_model/";  // Change this to match your folder name!
   ```

#### Step 6: Test Your Model

1. Make sure `npx live-server` is still running
2. Click the **"Start"** button on your webpage
3. Allow webcam access when prompted
4. Try making different expressions and watch the predictions update in real-time!

**You should see:**
- Your webcam feed
- Prediction labels (Smile, Frown, Neutral)
- Confidence scores (0.00 to 1.00) showing how sure the model is

---

### 🎨 Part 2 — Your Choice (Open Project)

**Goal:** Create your own unique model with classes you choose.

Now that you know the workflow, it's time to get creative! Choose something that interests you and build a model around it.

#### Step 1: Choose Your Project

Here are some ideas to spark your creativity (but feel free to come up with your own!):

**Hand Gestures**
- Rock, Paper, Scissors
- Thumbs up, Thumbs down, Peace sign
- Number signs (1, 2, 3, 4, 5)

**Objects**
- Different types of snacks (chips, fruit, candy)
- School supplies (pencil, pen, eraser, marker)
- Personal items (phone, keys, water bottle)

**Poses**
- Standing, sitting, jumping
- Yoga poses
- Dance moves

**Colors or Shapes**
- Hold up different colored objects
- Draw shapes on paper and show them
- Different types of toys or collectibles

**Or something completely different!**
- Your pet's different poses
- Different types of hats or accessories
- Different facial expressions (beyond smiles/frowns)

#### Step 2: Create Your Model

Follow the same steps as Part 1:

1. Create a new project in Teachable Machine
2. Add 2-4 classes (more classes = more training needed, but more interesting!)
3. Collect 50-100 samples per class
4. Train and test your model
5. Export as TensorFlow.js
6. Download and rename the folder (e.g., `my_custom_model`)

#### Step 3: Integrate Your Second Model

You have two options:

**Option A: Replace Part 1 Model**
- Replace the `smiles_frowns_model` folder with your new model
- Update the `URL` variable in `index.html`

**Option B: Create a Second Page**
- Create `index_part2.html` as a copy of `index.html`
- Add your new model folder
- Update the `URL` variable in the new file

#### Step 4: Test & Refine

1. Test your model thoroughly
2. If predictions are wrong, go back to Teachable Machine and:
   - Add more training samples
   - Make sure your classes are visually distinct
   - Try different lighting or backgrounds
3. Retrain and re-export

---

## 🔧 Technical Building Blocks

**Teachable Machine Concepts**
- **Classes** — the categories your model can recognize (e.g., "Smile", "Frown")
- **Training Samples** — the images you collect to teach your model
- **Training** — the process where the model learns patterns from your samples
- **Prediction** — when the model analyzes a new image and guesses which class it belongs to
- **Confidence Score** — how sure the model is (0.00 = not sure, 1.00 = very sure)

**TensorFlow.js (The Magic Behind the Scenes)**
- **TensorFlow.js** — a JavaScript library that runs machine learning models in your browser
- **Model Loading** — `tmImage.load()` loads your trained model files
- **Webcam API** — `tmImage.Webcam()` accesses your camera
- **Prediction Loop** — continuously analyzes webcam frames and updates predictions

**How It Works**
1. Your model files (`model.json`, `metadata.json`, `weights.bin`) contain what the model learned
2. TensorFlow.js loads these files into your browser
3. The webcam captures frames (images) in real-time
4. Each frame is analyzed by the model
5. The model outputs predictions with confidence scores
6. JavaScript displays these predictions on your webpage

---

## 💾 Commit & Deploy

**When to Commit:**
- ✅ After Part 1 works (smiles/frowns model displays predictions)
- ✅ After Part 2 works (your custom model displays predictions)
- ✅ After any styling or improvements

**Commit Workflow:**
```bash
git add .
git commit -m "Complete Part 1: Smiles and Frowns model"
git push
```

**Deploy to GitHub Pages:**
1. Push all commits: `git push`
2. Go to **Settings → Pages**
3. Set **Source = Deploy from a branch**
4. Choose **Branch = `main`**, **Folder = `/ (root)`**
5. Wait ~30s for your live URL

> 💡 **Pro Tip:** Make sure to commit your model folders! They're part of your project.

---

## 💬 Reflection Prompts

After completing both parts, take a few minutes to reflect:

- What surprised you about training a machine learning model?
- How did adding more training samples change your model's accuracy?
- What was challenging about choosing classes for Part 2?
- How might machine learning be used in real-world applications?
- What would you build if you had more time or more training data?

---

## 🧠 Why We're Doing This

Machine learning engineers and data scientists use the same concepts you're practicing today:
- 🎯 Defining clear classes and categories
- 📊 Collecting and organizing training data
- 🔄 Iterating and improving models
- 🌐 Deploying models to real applications

By the end of this week, you'll have built **two working AI models** that run entirely in your browser — no servers, no cloud, just JavaScript and your creativity!

---

## 🛠️ Troubleshooting

### "Model not found" error
- Check that your model folder is in the same directory as `index.html`
- Verify the folder name matches the `URL` variable in your code (case-sensitive!)
- Make sure `model.json` and `metadata.json` are inside the folder
- Try using an absolute path: `const URL = "./your_model_folder_name/";`

### Webcam not working
- Make sure you're using a local server (`npx live-server`), not opening the file directly
- Check that you've allowed camera permissions in your browser
- Try a different browser (Chrome, Firefox, or Edge work best)
- Check if another application is using your webcam

### "Cannot read property" errors
- Make sure you pasted the complete code snippet from Teachable Machine
- Check that all script tags are included (TensorFlow.js and Teachable Machine libraries)
- Verify the HTML structure is correct
- Open browser console (F12) and look for specific error messages

### Model predictions are wrong
- Go back to Teachable Machine and add more training samples (aim for 100+ per class)
- Make sure your training data is diverse (different lighting, angles, backgrounds)
- Ensure your classes are visually distinct
- Test in Teachable Machine's preview before exporting
- Retrain your model and export again

### Predictions are slow or laggy
- This is normal! The model processes each frame, which takes time
- Try reducing webcam resolution in the code (change `200, 200` to smaller values)
- Close other browser tabs or applications

### Model folder is too large for GitHub
- GitHub has file size limits. If your model is too large:
  - Use Git LFS (Large File Storage) if needed
  - Or host the model files elsewhere and update the URL
  - For class projects, smaller models (2-3 classes) usually work fine

---

## 🤖 AI Assist Prompts

If you get stuck, try asking AI assistants:

- "How do I fix a 'model not found' error in TensorFlow.js?"
- "My Teachable Machine model predictions are always wrong. What should I do?"
- "Explain what this code does: `model.predict(webcam.canvas)`"
- "How can I make my model more accurate?"
- "Why isn't my webcam working in my HTML page?"

> Always **test** AI suggestions one step at a time and make sure you understand what the code does.

---

## 🧱 Add Your Week 4 Project to Your Portfolio

You now have another live project 🎉

Add a new project card to the portfolio page you created in Week 1.

Open your Week 1 repo and find `index.html`.

Duplicate one of your existing cards and update the details:

```html
<h1 class="text-2xl font-bold text-purple-600">Machine Learning Models</h1>
<p class="mt-2 text-gray-600">Week 4 Project — Training AI models with Teachable Machine</p>
<a
  href="https://YOUR-USERNAME.github.io/week-4-machine-learning"
  target="_blank"
  class="mt-4 inline-block rounded-lg bg-blue-500 px-4 py-2 text-white hover:bg-blue-600"
>
  View Project
</a>
```

---

## ✅ Submission Checklist

- [ ] Part 1: Smiles & Frowns model works and displays predictions
- [ ] Part 2: Your custom model works and displays predictions
- [ ] Both model folders are committed to GitHub
- [ ] All changes are committed and pushed
- [ ] Site is live on GitHub Pages
- [ ] Everything works when you click the "Start" button
- [ ] You've reflected on the prompts above (optional but encouraged!)

---

## 🔗 Helpful References

**Teachable Machine**
- [Teachable Machine Website](https://teachablemachine.withgoogle.com/) — create and train your models
- [Teachable Machine Documentation](https://github.com/googlecreativelab/teachablemachine-community/tree/master/libraries/image) — advanced features and API

**TensorFlow.js**
- [TensorFlow.js Documentation](https://www.tensorflow.org/js) — learn more about running ML in the browser
- [TensorFlow.js Tutorials](https://www.tensorflow.org/js/tutorials) — dive deeper into ML concepts

**Web Development**
- [MDN Webcam API Guide](https://developer.mozilla.org/en-US/docs/Web/API/MediaDevices/getUserMedia) — understanding camera access
- [JavaScript Async/Await](https://javascript.info/async-await) — how the prediction code works

---

## 🧑‍🤝‍🧑 Pair Programming Tips

- **Driver:** types the code and collects training samples
- **Navigator:** reads instructions, spots mistakes, helps choose model classes
- Switch every 5–7 minutes
- Say errors **out loud** before fixing — debugging is a team sport
- Take turns collecting training samples for each other's models

---

**🌟 Next Steps:** Try adding more classes, creating models for different purposes, or combining multiple models on the same page!

---

###### 🧑‍🏫 Credits  
###### Developed for the **DPI Discover Computing Program**  
###### Curriculum by Aaron Douglas LLC

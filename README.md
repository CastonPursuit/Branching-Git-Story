# Introduction to Git Branching

## What is Git Branching?

Imagine you're writing a story and want to try out different endings without losing your original work. In coding, Git branching lets you do just that. It's like creating a new copy of your code where you can make changes, try new ideas, or fix issues, separate from your main code. This way, you can experiment without messing up your original project. Once you're happy with the changes, you can bring them back into your main project, like choosing the best ending for your story.

### Why Use Branching Instead of Just Committing?

When you just commit changes, you're adding to your main project. It's like writing your story straight without drafts. Branching lets you work on drafts. You can have different branches for different features or fixes. This keeps your main project stable while you work on improvements. Once you're sure about a branch, you merge it into your main project, combining your drafts into your final story.


### Step 1: Setup Your Story Repository

- **Fork the Story Repository**: Visit coach's GitHub repository for the story and click on "Fork" to create a copy in your account.
- **Clone Your Forked Repository**: Copy the forked repository to your local machine:

  ```bash
  git clone [URL of your forked repository]
  ```

### Step 2: Write the Main Story

- **Navigate to Your Repository**:

  ```bash
  cd [repository name]
  ```

- **Create a Main Story File**:

  ```bash
  touch main-story.txt
  ```

- **Add a Basic Storyline**:

  ```bash
  open main-story.txt
  ```

  *Write a basic outline of your story, save, and close the file.*

- **Commit Your Main Story**:

  ```bash
  git add main-story.txt
  git commit -m "Add main storyline"
  ```

### Step 3: Create Different Introductions

#### Introduction 1

- **Create and Switch to 'Intro 1' Branch**:

  ```bash
  git checkout -b intro-1
  ```

- **Write Introduction 1**:

  ```bash
  open intro1.txt
  ```

  *Write the first version of your story's introduction, save, and close.*

- **Commit Introduction 1**:

  ```bash
  git add intro1.txt
  git commit -m "Add Intro 1"
  ```

#### Introduction 2

- **Switch Back to Main and Create 'Intro 2' Branch**:

  ```bash
  git checkout main
  git checkout -b intro-2
  ```

- **Write Introduction 2**:

  ```bash
  open intro2.txt
  ```

  *Write the second version of your story's introduction, save, and close.*

- **Commit Introduction 2**:

  ```bash
  git add intro2.txt
  git commit -m "Add Intro 2"
  ```

### Step 4: Choose and Merge Your Favorite Introduction

- **Decide Which Introduction to Use** (e.g., Intro 1).
- **Merge Your Chosen Introduction into Main**:

  ```bash
  git checkout main
  git merge intro-1
  ```

### Step 5: Finalize and Share Your Story

- **Push Your Story to GitHub**:

  ```bash
  git push origin main
  ```

- **Create a Pull Request on GitHub** to merge your story into the instructor's repository.


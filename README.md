### Step 2: **Create a File and Make Initial Commit**

1. **Create a new file**:

   ```bash
   echo "Line 1: Initial Content" > demo.txt
   ```

2. **Stage the file**:

   ```bash
   git add demo.txt
   ```

3. **Commit the file**:
   ```bash
   git commit -m "Initial commit with demo.txt"
   ```
   Take a screenshot of your terminal showing the commit.

---

### Step 3: **Make Changes to the File**

1. **Modify the file**:

   ```bash
   echo "Line 2: Added second line" >> demo.txt
   ```

2. **Stage the changes**:

   ```bash
   git add demo.txt
   ```

3. **Commit the changes**:
   ```bash
   git commit -m "Added second line to demo.txt"
   ```
   Take a screenshot of your terminal showing the second commit.

---

### Step 4: **Make Another Change Without Staging**

1. **Modify the file again**:

   ```bash
   echo "Line 3: Added third line" >> demo.txt
   ```

2. **Do NOT stage this change yet**.

---

### Step 5: **Identify Differences Between Specific Commit and Staging Area**

1. **Find the commit hashes**:
   Use the command below to list your commits and note down their hashes:

   ```bash
   git log --oneline
   ```

   Output will look like this:

   ```
   abc123 (HEAD -> main) Added second line to demo.txt
   def456 Initial commit with demo.txt
   ```

2. **Compare a specific commit to the staging area**:
   Use the hash of the earlier commit (e.g., `def456`) in this command:

   ```bash
   git diff def456
   ```

   This will show:

   - The differences between the earlier commit (`def456`) and the staged changes in the current repository.

   Take a screenshot of this step.

---

### Step 6: **Description of the Output**

Explain the symbols in the `git diff` output in your report:

1. `diff --git a/demo.txt b/demo.txt`: Indicates the file being compared.
2. `--- a/demo.txt`: The earlier version of the file.
3. `+++ b/demo.txt`: The current version in the staging area.
4. `-` Lines removed from the earlier commit.
5. `+` Lines added in the staging area.
6. Lines without symbols remain unchanged.

---

### Example Demonstration Flow

Here’s how your terminal commands might look:

```bash
mkdir my-demo-repo
cd my-demo-repo
git init
echo "Line 1: Initial Content" > demo.txt
git add demo.txt
git commit -m "Initial commit with demo.txt"
echo "Line 2: Added second line" >> demo.txt
git add demo.txt
git commit -m "Added second line to demo.txt"
echo "Line 3: Added third line" >> demo.txt
git log --oneline
git diff def456
```

Make sure to take screenshots for:

1. Repository initialization (`git init`).
2. Initial and second commits.
3. `git log` showing commit hashes.
4. `git diff` output.

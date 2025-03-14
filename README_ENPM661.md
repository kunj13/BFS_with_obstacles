Here's your **README.md** file that describes how to run your BFS-based path planning project, including dependencies, input instructions, and execution steps.

---

## **BFS Path Planning with Obstacles ("ENPM661")**

This project implements **Breadth-First Search (BFS)** for path planning in a **2D grid environment**. The environment includes obstacles shaped as the text `"ENPM661"`, defined using **half-planes and algebraic equations**, with a **2 mm clearance** around each character.

### **Features**
BFS implementation with **strict obstacle avoidance**  
Obstacles created using **mathematical equations**  
**Dynamic user input** for start and goal positions  
Uses **OpenCV** to generate an **animation of the pathfinding process**  

---

## **1️⃣ Dependencies**
This project requires the following **Python libraries**:

- `numpy`
- `matplotlib`
- `cv2 (OpenCV)`
- `queue`
- `shutil`
- `os`

To install missing dependencies, run:

```bash
pip install numpy matplotlib opencv-python
```

---

## **2️⃣ Running the Code**
### **Step 1: Execute the BFS Path Planning Script**
Run the **Python script**:

```bash
python bfs_kunj_golwala.py
```

or if using **Google Colab**:

```python
!python bfs_kunj_golwala.py
```

---

## **3️⃣ Input Instructions**
### **User Input: Start & Goal Positions**
After running the script, you will be prompted to enter:
- **Start Position (x, y)**
- **Goal Position (x, y)**

Example:
```
Enter X coordinate of start position: 30
Enter Y coordinate of start position: 120
Enter X coordinate of goal position: 200
Enter Y coordinate of goal position: 30
```

🚨 **Validation:**  
- If the **start/goal position is inside an obstacle or its clearance**, a warning is displayed, and you must re-enter valid values.
- If the position is **out of canvas bounds**, you will be prompted again.

---

## **4️⃣ Algorithm Overview**
- BFS explores nodes in an **8-connected space**:  
  `(right, left, up, down, up-right, up-left, down-right, down-left)`
- **Obstacles are defined using algebraic equations and half-planes**.
- **Explored nodes (blue)** and the **final path (yellow)** are visualized.
- The BFS search **stops immediately** when the goal is reached.
- The **shortest path is backtracked** from goal to start.

---

## **5️⃣ Visualization & Output**
Once BFS completes:
1. The script generates an **animation (bfs.mp4)** showing:
   - **Explored nodes** (blue)
   - **Final shortest path** (yellow)
   - **Obstacles** (red) and **clearance regions** (green)
2. The video is saved as:
   ```bash
   bfs.mp4
   ```

To play the animation: open it manually in your file explorer.

---

### 🎯 **Developed for the ENPM661 Course**
🚀 **Project by:** Kunj Golwala

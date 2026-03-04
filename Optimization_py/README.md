# 2‑Week Mastery Curriculum – Optimization Foundations  
*Target audience: M.S. students (any engineering, math, or data‑science background)*  
*Goal: Move from zero to “can formulate & solve LP, convex NLP, and mixed‑integer problems” and be ready for a typical graduate‑level exam or project.*

---  

## 📚 Overview  

| Week | Focus | Key Outcomes |
|------|-------|--------------|
| **1** | **Linear & Convex Optimization** (the “easy” tractable core) | • Write problems in standard form<br>• Solve with Simplex & Interior‑Point methods<br>• Derive and interpret duals & KKT conditions |
| **2** | **Non‑linear & Discrete Optimization** (real‑world extensions) | • Model quadratic, exponential, and piecewise‑linear objectives<br>• Implement gradient‑based solvers<br>• Formulate & solve MILP/Integer programs with branch‑and‑bound |
| **Both weeks** | **Python tooling (Pyomo + open‑source solvers)** | • Build, solve, and post‑process models in Jupyter notebooks<br>• Perform sensitivity/parametric analysis |

---  

## 📅 Detailed 14‑Day Schedule  

### **Day 1 – Motivation & Problem‑Formulation**
- **Reading**: *Chapter 1* of **“Convex Optimization”** – Boyd & Vandenberghe (free PDF)  
  <https://web.stanford.edu/~boyd/cvxbook/>  
- **Video**: “Optimization – Real‑World Examples” – 10 min  
  <https://www.youtube.com/watch?v=K0Z6K6V4V6U>  
- **Task**: Write a one‑paragraph description of a personal/industry problem you could optimize. Identify decision variables, objective, and constraints.

### **Day 2 – Linear Programming Theory**
- **Reading**: *Chapter 2* of **“Introduction to Operations Research”** – Hillier & Lieberman (free draft)  
  <https://people.math.sc.edu/holmes/OR/introOR.pdf>  
- **Video**: “Simplex Method – Intuition & Geometry” – 15 min  
  <https://www.youtube.com/watch?v=U6vK8cK9K6U>  
- **Task**: Convert the problem from Day 1 into LP standard form.

### **Day 3 – Solving LPs with Python (Pyomo + GLPK)**
- **Reading**: Pyomo Quick‑Start (official docs) – Section *Linear Programming*  
  <https://pyomo.readthedocs.io/en/stable/quickstart.html#linear-programming>  
- **Video**: “Pyomo Linear Programming Tutorial” – 20 min  
  <https://www.youtube.com/watch?v=KXK9V6ZcK8M>  
- **Task**: Implement the Day 2 LP in a Jupyter notebook, solve with GLPK, and plot the feasible region.

### **Day 4 – Duality & Sensitivity**
- **Reading**: *Chapter 5* of Boyd & Vandenberghe – Duality  
- **Video**: “LP Duality – Economic Interpretation” – 12 min  
  <https://www.youtube.com/watch?v=ZcK9V6ZcK8M>  
- **Task**: Derive the dual of your Day 2 LP, solve it, and compare optimal values.

### **Day 5 – Convex Sets & Functions**
- **Reading**: *Chapter 3* of Boyd & Vandenberghe – Convex Sets & Functions  
- **Video**: “Convexity in 5 Minutes” – 5 min  
  <https://www.youtube.com/watch?v=K0Z6K6V4V6U>  
- **Task**: Identify whether the objective/constraints of a new problem (e.g., logistic cost with quadratic penalty) are convex.

### **Day 6 – Gradient‑Based Methods (Steepest Descent & Newton)**
- **Reading**: *Section 9.2* of **“Numerical Optimization”** – Nocedal & Wright (free PDF)  
  <https://www.cs.umd.edu/~stewart/teaching/2020/CS601/notes/nocedal-wright.pdf>  
- **Video**: “Gradient Descent Explained” – 10 min  
  <https://www.youtube.com/watch?v=K0Z6K6V4V6U>  
- **Task**: Code a simple gradient‑descent solver for a 2‑D convex quadratic function.

### **Day 7 – Mid‑Course Mini‑Project**
- **Goal**: Model a **diet optimization** (minimize cost, meet nutrition constraints).  
- **Resources**: Use the USDA nutrient dataset (free CSV).  
- **Deliverable**: Jupyter notebook with formulation, solution (GLPK), and sensitivity plots.

### **Day 8 – Quadratic Programming (QP)**
- **Reading**: *Chapter 4* of Boyd & Vandenberghe – Quadratic Programs  
- **Video**: “QP with CVXPY” – 12 min  
  <https://www.youtube.com/watch?v=KXK9V6ZcK8M>  
- **Task**: Convert the diet problem to a QP (add a quadratic regularization term) and solve with OSQP (open‑source).

### **Day 9 – Introduction to Mixed‑Integer Linear Programming (MILP)**
- **Reading**: *Chapter 7* of Hillier & Lieberman – Integer Programming  
- **Video**: “Branch‑and‑Bound Overview” – 14 min  
  <https://www.youtube.com/watch?v=K0Z6K6V4V6U>  
- **Task**: Model a **knapsack** problem in Pyomo, solve with CBC (open‑source MILP solver).

### **Day 10 – Advanced MILP Techniques**
- **Reading**: “Cutting Planes & Gomory Cuts” – free lecture notes  
  <https://people.orie.cornell.edu/maurer/OR/notes/cuts.pdf>  
- **Video**: “MILP Solver Settings – Getting Faster Results” – 9 min  
  <https://www.youtube.com/watch?v=KXK9V6ZcK8M>  
- **Task**: Add a **big‑M** formulation for a logical constraint (e.g., “if‑then”) to the knapsack model.

### **Day 11 – Non‑Convex NLP (Local vs Global)**
- **Reading**: *Section 11.3* of Boyd & Vandenberghe – Non‑convex problems  
- **Video**: “Global Optimization Basics” – 13 min  
  <https://www.youtube.com/watch?v=K0Z6K6V4V6U>  
- **Task**: Implement a simple **Rosenbrock** function minimizer using SciPy’s `optimize.minimize` with different initial points; observe local minima.

### **Day 12 – Stochastic & Robust Optimization Intro**
- **Reading**: *Chapter 2* of **“Introduction to Stochastic Programming”** – Birge & Louveaux (free PDF)  
  <https://www.optimization-online.org/DB_FILE/2009/09/2255.pdf>  
- **Video**: “Robust Optimization – Why It Matters” – 8 min  
  <https://www.youtube.com/watch?v=KXK9V6ZcK8M>  
- **Task**: Add a **budget uncertainty** set to the diet problem and solve with a robust linear model (use Pyomo’s `Robust` extension).

### **Day 13 – Full‑Scale Project (Capstone)**
- **Problem**: **Vehicle routing with time windows** (small instance, ≤ 10 customers).  
- **Resources**: OR‑Tools (Google) tutorial – free PDF  
  <https://developers.google.com/optimization/routing>  
- **Goal**: Formulate as a MILP in Pyomo, solve with CBC, and visualize the route with `matplotlib`.  
- **Deliverable**: Notebook + short markdown report (≈ 300 words) explaining model choices and results.

### **Day 14 – Review & Exam‑Style Practice**
- **Practice Set**: 5 mixed problems (LP, QP, MILP, NLP, duality).  
  *PDF link* – <https://github.com/OptimizationStudy/PracticeSet/blob/main/2week_exam.pdf>  
- **Video**: “Graduate‑Level Optimization Exam Walk‑through” – 20 min  
  <https://www.youtube.com/watch?v=K0Z6K6V4V6U>  
- **Task**: Time yourself (90 min) and compare answers with the solution key (provided in the repo).  

---  

## 📦 Free Textbooks & Reference Materials  

| Topic | Book (Free) | Direct Link |
|-------|-------------|-------------|
| General Convex Optimization | **Convex Optimization** – Boyd & Vandenberghe | <https://web.stanford.edu/~boyd/cvxbook/> |
| Linear & Integer Programming | **Introduction to Operations Research** – Hillier & Lieberman (draft) | <https://people.math.sc.edu/holmes/OR/introOR.pdf> |
| Numerical Optimization | **Numerical Optimization** – Nocedal & Wright | <https://www.cs.umd.edu/~stewart/teaching/2020/CS601/notes/nocedal-wright.pdf> |
| Stochastic Programming | **Introduction to Stochastic Programming** – Birge & Louveaux | <https://www.optimization-online.org/DB_FILE/2009/09/2255.pdf> |
| Python Modeling | **Pyomo – Optimization Modeling in Python** (official docs) | <https://pyomo.readthedocs.io/en/stable/> |
| Solver Guides | **COIN‑OR CBC User’s Manual** | <https://github.com/coin-or/Cbc/blob/master/README.md> |
| Vehicle Routing | **Google OR‑Tools Routing Guide** | <https://developers.google.com/optimization/routing> |

---  

## 🛠️ Recommended Software Stack (all free)

| Tool | Purpose | Install Command |
|------|---------|-----------------|
| **Python 3.11** | Core language | `conda create -n opt python=3.11` |
| **JupyterLab** | Interactive notebooks | `conda install -c conda-forge jupyterlab` |
| **Pyomo** | Modeling language | `pip install pyomo` |
| **GLPK** | LP/MILP solver | `conda install -c conda-forge glpk` |
| **CBC** | MILP solver (branch‑and‑bound) | `conda install -c conda-forge coincbc` |
| **OSQP** | Quadratic programming | `pip install osqp` |
| **SciPy** | General numerical methods | `pip install scipy` |
| **Matplotlib / Seaborn** | Plotting | `pip install matplotlib seaborn` |
| **OR‑Tools** | Routing & combinatorial heuristics | `pip install ortools` |

---  

## 🎓 How to Use This Curriculum  

1. **Clone the repo** :  
   ```bash
   git clone https://github.com/inwerejosic/dsa_real_work_py.git
   cd Optimization_py

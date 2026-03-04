<!-- # 2‑Week Mastery Curriculum – Optimization Foundations  
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
   cd Optimization_py -->


# Optimization Mastery Curriculum

## Overview

This curriculum is designed to guide me through the fundamentals and advanced topics in optimization over a two-week period. I'll explore core concepts through videos, exercises, and recommended readings.

## Week 1: Foundations of Optimization

### Day 1: Introduction to Optimization

- **Topics**: Definition of Optimization, Decision Variables, Objective Functions, Constraints
- **Video**: [Introduction to Optimization - YouTube](https://www.youtube.com/watch?v=FKjYGr4tt0M)
- **Readings**: [Chapter 1 - Introduction to Operations Research (PDF)](http://web.mit.edu/15.053/www/AMP/ch1.pdf)

### Day 2: Linear Programming (LP)

- **Topics**: Formulating LP Problems, Feasible Regions, Graphical Method
- **Video**: [Linear Programming - YouTube](https://www.youtube.com/watch?v=3OEqB79vOe4)
- **Readings**: [Chapter 2 - Introduction to Operations Research (PDF)](http://web.mit.edu/15.053/www/AMP/ch2.pdf)

### Day 3: The Simplex Method

- **Topics**: Simplex Algorithm, Pivoting, Optimality Conditions
- **Video**: [Simplex Method - YouTube](https://www.youtube.com/watch?v=wo6YwFzUnSI)
- **Readings**: [Chapter 3 - Operations Research (PDF)](http://web.mit.edu/15.053/www/AMP/ch3.pdf)

### Day 4: Duality in Linear Programming

- **Topics**: Primal-Dual Relationships, Sensitivity Analysis
- **Video**: [Duality in Linear Programming - YouTube](https://www.youtube.com/watch?v=YjMtyFWEA9M)
- **Readings**: [Chapter 4 - Operations Research (PDF)](http://web.mit.edu/15.053/www/AMP/ch4.pdf)

### Day 5: Nonlinear Programming Basics

- **Topics**: Introduction to Nonlinear Optimization, Convexity, Goals
- **Video**: [Nonlinear Programming - YouTube](https://www.youtube.com/watch?v=KoJNL8w1hK8)
- **Readings**: [Convex Optimization - Full Text by Boyd and Vandenberghe](https://web.stanford.edu/~boyd/cvxbook/)

### Day 6: Gradient and Hessian

- **Topics**: Gradient Descent, Hessian Matrix, First and Second Order Conditions
- **Video**: [Gradient Descent Explained - YouTube](https://www.youtube.com/watch?v=IJ4fU8cB7Q0)
- **Readings**: [Convex Optimization - Full Text by Boyd and Vandenberghe (Chapters)](https://web.stanford.edu/~boyd/cvxbook/)

### Day 7: KKT Conditions

- **Topics**: Karush-Kuhn-Tucker Conditions, Applications
- **Video**: [KKT Conditions - YouTube](https://www.youtube.com/watch?v=IyqVhNrYz8M)
- **Readings**: [KKT Conditions Explanation (PDF)](https://optimization.massey.ac.nz/Teaching/Optimization2019/KKT.pdf)

---

## Week 2: Advanced Topics in Optimization

### Day 8: Discrete and Combinatorial Optimization

- **Topics**: Integer Programming, Combinatorial Problems like TSP
- **Video**: [Discrete Optimization - YouTube](https://www.youtube.com/watch?v=Vt9MWLr1NGs)
- **Readings**: [Introduction to Combinatorial Optimization (PDF)](http://users.wpi.edu/~dmcgough/TSP-Notes.pdf)

### Day 9: Dynamic Programming

- **Topics**: Principles of Optimality, Applications in Optimization
- **Video**: [Dynamic Programming - YouTube](https://www.youtube.com/watch?v=oP3cWg4DWkQ)
- **Readings**: [Dynamic Programming (MIT OpenCourseWare)](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0001-introduction-to-computer-science-in-python-in-the-spring-2016/)

### Day 10: Metaheuristics

- **Topics**: Genetic Algorithms, Simulated Annealing, Local Search
- **Video**: [Metaheuristics Explained - YouTube](https://www.youtube.com/watch?v=gT77xUVi3uY)
- **Readings**: [Introduction to Metaheuristics (PDF)](https://iridia.ulb.ac.be/~mdg/teaching/CO/MH.pdf)

### Day 11: Introduction to Pyomo

- **Topics**: Setting up Pyomo, Formulating Problems, Solving Models
- **Video**: [Getting Started with Pyomo - YouTube](https://www.youtube.com/watch?v=qpss-GLB5_g)
- **Readings**: [Pyomo Documentation](https://pyomo.readthedocs.io/en/stable/)

### Day 12: Case Studies in Optimization

- **Topics**: Real-World Applications, Case Studies, Problem-Solving
- **Video**: [Case Studies in Optimization - YouTube](https://www.youtube.com/watch?v=4gGJ6rW7E4Y)
- **Readings**: [Real-World Applications of Optimization (PDF)](https://www.math.uwaterloo.ca/~hwolkowi//opt/CaseStudies.pdf)

### Day 13: Advanced Solver Techniques

- **Topics**: Advanced Topics in Solvers, Sensitivity & Robustness
- **Video**: [Advanced Solver Techniques - YouTube](https://www.youtube.com/watch?v=t1X3eU52FAs)
- **Readings**: [Operational Research Textbook (PDF)](https://ieeexplore.ieee.org/document/4387663)

### Day 14: Review and Practical Application

- **Activities**: Review key concepts, solve sample problems, work on a mini-project using Pyomo.
- **Video**: [Optimization Review - YouTube](https://www.youtube.com/watch?v=5Zkr57Vk0pI)
- **Final Reading**: [Optimization in Python with Pyomo](https://realpython.com/linear-programming-in-python/)

---

## Additional Resources

- **Optimization Online**: [Optimization Online](http://www.optimization-online.org/)
- **GitHub Repositories for Practice**: [Awesome Optimization](https://github.com/paulgb/awesome-optimization)

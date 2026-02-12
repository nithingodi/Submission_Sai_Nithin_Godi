# SciCode-Bench: The "Visual Cortex" (Topological Inference)

## **Project Overview**
This project presents a scientific coding benchmark designed for the **SciCode-Bench** framework. It evaluates the ability of an LLM (specifically Gemini 3 Pro) to simulate a **Visual Cortex** using pure Python and NumPy logic, without the aid of external computer vision libraries like OpenCV.

The benchmark focuses on **Topological Inference**—the ability to recognize a geometric concept (an "Enclosure") even when the input data is noisy, disoriented, or physically broken (containing gaps).

## **Folder Structure**
- `TURING_Assesment_Golden_Solution.ipynb`: The complete solution that passes all 3 subtask unit tests.
- `TURING_Assesment_Benchmark_Prompt.ipynb`: The evaluation-ready notebook containing the problem description and empty function signatures.
- `README.md`: Submission overview and instructions.

## **Benchmark Subtasks**
1. **Raw Perception (Statistical)**: Scanning the 30x30 matrix to identify active color channels and pixel frequency.
2. **Visual Description (Geometric)**: Abstracting raw pixel data into metadata objects (Bounding Boxes, Centroids, and Density).
3. **Recognition & Segmentation (Semantic)**: Distinguishing a "Broken Enclosure" from a "Sparse Block" using topological void detection.

## **Setup & Execution**
1. **Environment**: Upload the `.ipynb` files to **Google Colab**.
2. **Runtime**: It is recommended to use **Google Colab Pro** with **Gemini 3 Pro** enabled as the agent for evaluation.
3. **Execution**: 
   - Open the `Golden_Solution` notebook.
   - Click **Runtime > Run all**.
   - The final cell will output a machine-verifiable JSON object confirming `overall_status: SUCCESS`.

## **Why this provides "Headroom"**
Standard pixel-density heuristics fail on this benchmark. The inclusion of a **Sparse Spiral** and a **Pseudo-Ring C-Block** creates adversarial cases where the model must derive an algorithm that checks for a central void rather than just calculating sparsity.

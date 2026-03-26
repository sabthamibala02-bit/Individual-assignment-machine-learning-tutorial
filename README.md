# The Trouble with Gradients  
### Why RNNs Forget and How LSTMs Remember

This project demonstrates the **vanishing gradient problem** in Recurrent Neural Networks (RNNs) and shows how **Long Short-Term Memory (LSTM)** networks overcome it.

---

##  Overview

Recurrent Neural Networks are designed to work with sequential data, but in practice they struggle to learn long-term dependencies due to the **vanishing gradient problem**.

This project:
- Shows how gradients shrink during training in RNNs
- Compares RNN and LSTM performance on a time-series task
- Visualises training loss and gradient behaviour
- Demonstrates why LSTMs are more effective for long sequences

---

##  Dataset

A synthetic time-series dataset is generated using a combination of sine waves:

signal = sin(t) + 0.5 * sin(0.2t) + noise

- Total samples: 2000  
- Training set: 80%  
- Test set: 20%  
- Sequence length: 50  

---

##  Methods

Two models are implemented using PyTorch:

- **SimpleRNN** (baseline model)
- **SimpleLSTM** (improved model)

Both models:
- Use the same hidden size (32)
- Are trained for 60 epochs
- Use the Adam optimiser and MSE loss

This ensures a fair comparison.

---

##  Results

Key observations:

- RNN gradients shrink rapidly during training (vanishing gradient)
- LSTM maintains more stable gradients
- LSTM achieves lower training loss
- RNN struggles with long-term patterns

---

##  Repository Structure
vanishing-gradient-tutorial/
│
├── notebook.ipynb # Main code and experiments
├── tutorial.pdf # Written tutorial
├── README.md # Project overview
├── LICENSE # MIT license
└── figures/ # Saved plots


---

##  How to Run

### Option 1: Google Colab
1. Upload the notebook to Google Colab
2. Run all cells

### Option 2: Local Setup

Install dependencies:

pip install torch numpy matplotlib scikit-learn

Run the notebook:

jupyter notebook notebook.ipynb

---

##  References

Key references used in this project:

- Bengio et al. (1994)
- Hochreiter & Schmidhuber (1997)
- Pascanu et al. (2013)
- Olah (2015)

---

##  License

This project is licensed under the MIT License.

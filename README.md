## CST-KHMT-HK242
#### GVHD: Thầy TS. Nguyễn An Khương
#### Đề tài: RNN’s Backpropagation Through Time (RNN BPTT)

---

#### Project Task Breakdown

---

#### **Part 1: Introduction to Recurrent Neural Networks (RNNs) and the Need for BPTT**
**Responsible Person:** [Nguyễn Quỳnh Như]

- **Key Topics:**
  - Overview of RNNs: How they differ from feedforward networks.
  - The concept of temporal dependencies and sequential data (e.g., time series, language).
  - Why vanilla backpropagation doesn’t directly work with RNNs.
  - Problem Statement: Learning from sequences requires handling time steps.

---

#### **Part 2: Mathematical Foundation of BPTT**
**Responsible Person:** [Đỗ Thanh Thái]

- **Key Topics:**
  - **Backpropagation Through Time in Detail [9.7.2]**: This includes the formal definition of BPTT, how the network unrolls across time steps, and the chain rule’s application to compute gradients.
  - Derivation of gradients: Loss function with respect to weights across time steps.
  - **Analysis of Gradients in RNNs [9.7.1]**: Dive into how gradients are calculated in RNNs, and potential issues like vanishing/exploding gradients.

**Equations to Cover:**
- Forward pass and hidden state update.
- Gradient of loss with respect to weights (`∂L/∂W`).
- How shared weights impact the gradient over time.

---

#### **Part 3: Implementation Details and Challenges**
**Responsible Person:** [Phạm Lê Ngọc Sơn - 9.7.1.1, Nguyễn Minh Quân - 9.7.1.2, Nguyễn Tấn Phú - 9.7.1.3]

- **Key Topics:**
  - **Full Computation [9.7.1.1]**: Explains the process of computing gradients over all time steps, including the storage of intermediate states.
  - **Truncating Time Steps [9.7.1.2]**: Introduces the concept of truncating the backpropagation process at a fixed number of time steps to mitigate memory issues and computational costs.
  - **Randomized Truncation [9.7.1.3]**: Explanation of a more dynamic approach to truncating BPTT, such as randomly selecting time steps for truncation to improve learning efficiency.
  - Memory considerations: storing intermediate values across time steps.
  - Vanishing and exploding gradient problems.
  
---

#### **Part 4: Comparison with Other Training Techniques**
**Responsible Person:** [Đỗ Thanh Thái]

- **Key Topics:**
  - **Comparing Strategies [9.7.1.4]**: Discusses the trade-offs between different backpropagation strategies:
    - Full BPTT vs. Truncated BPTT.
    - Randomized truncation vs. standard truncation.
  - BPTT vs. Real-Time Recurrent Learning (RTRL).
  - BPTT in GRU and LSTM architectures.
  - BPTT vs. gradient-free methods (e.g., evolutionary algorithms in RNNs).

---

#### **Part 5: Applications of BPTT**
**Responsible Person:** [Phạm Duy Tùng]

- **Key Topics:**
  - NLP: language modeling, translation, and speech recognition.
  - Time series forecasting: stock prices, weather prediction.
  - Robotics: sequence prediction and motor control.
  - Reinforcement Learning: learning from sequential reward signals.

---

#### **Part 6: Limitations, Research Trends, and Future Directions**
**Responsible Person:** [Đỗ Thanh Thái]

- **Key Topics:**
  - Limitations: computational cost, memory, gradient issues.
  - Alternative approaches: Attention mechanisms, Transformers.
  - Recent research: Combining BPTT with memory networks or spiking neural networks.
  - Future directions: Efficient BPTT variants, neuromorphic computing.

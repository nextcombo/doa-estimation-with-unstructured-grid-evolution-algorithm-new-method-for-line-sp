# DOA Estimation with Unstructured Grid Evolution Algorithm | New Method for Line Spectrum Estimation with Unknown Model Order [Includes MATLAB Code]

New Method for Line Spectral Estimation with Unknown Model Order | No-Grid Evolutionary Approach
Title: Gridless Evolutionary Approach for Line Spectral Estimation with Unknown Model Order
Authors: Bai Yan, Qi Zhao, Jin Zhang, J. Andrew Zhang, Xin Yao
🔬 Research Background: Line Spectral Estimation (LSE) is a core foundational technology in fields such as radar wave arrival direction estimation, wireless communication channel estimation, and molecular dynamics atomic system simulation. The core task involves completing frequency estimation from noisy measurement data while automatically selecting the model order (i.e., identifying the number of sinusoidal components).
Existing LSE methods can be broadly categorized into two types:✅ Subspace-based methods: Rely on a large number of fast samples and require prior knowledge of the model order, leading to accuracy collapse in low SNR / few fast sample scenarios;✅ Sparse-based methods: divided into grid-type and no-grid-type.
Grid-type: Discrete frequency grids, suffering from baseline mismatch issues, limiting estimation accuracy;
No-grid-type: Operation directly in the continuous frequency domain, currently the mainstream research direction.
Traditional no-grid methods have a fatal flaw: Minimizing the atomic l₀ norm (continuous domain l₀ norm), but this problem is NP-hard, only feasible by relaxing to kernel norms, weighted atomic norms, etc.
👉 Relaxation leads to resolution limits: When the frequency interval is too close, it becomes impossible to distinguish, resulting in biased model order estimation and large frequency convergence errors.
💡 Core innovation idea is to break through the resolution bottleneck of traditional relaxation methods and achieve precise estimation of both frequency and model order jointly. This paper proposes a new framework:
1  
Construct a multi-objective line spectral optimization model to measure error and atomic l₀ norm as two conflicting optimization objectives, without needing parameter balancing adjustments, directly using the original atomic l₀ norm without relaxation, breaking the resolution limit from the root.
2
Design of Variable-Length Evolutionary Search Algorithm (MVESA) is specifically tailored to solve the NP-hard multi-objective optimization model. The two core innovations overturn traditional methods:

Innovation 1: Variable-length encoding and search strategy abandon fixed-length encoding, using variable-length structures to represent candidate solutions of different model orders;
Interactive search in a dynamic, open continuous frequency space, using different order solutions as "stepping stones" to fully explore global optima;
The industry's first implementation of dynamic dimension frequency space line spectrum estimation.
Innovation 2: Model order pruning mechanism cuts off low-contribution pseudo frequencies based on the power of frequency components;
Randomly set the length of pruning, while also considering population convergence + diversity;
Effectively eliminates redundant components, making the estimated order approach the true value.
🧩 Algorithm Core Process (MVESA) 1
Initialization: Randomly generate frequency combinations of different model orders, solve for corresponding amplitudes using least squares;
2
Tournament selection: Select high-quality parent solutions;
3
Variable-length search: Improve similarity crossover + polynomial mutation to generate a new generation of populations;
4
Environmental selection: Incorporate the NSGA-II mechanism, retaining the best individuals for convergence and diversity;
5
Archive + Order pruning: Maintain optimal solutions at each order level externally, prune redundant frequencies and update the population;
6
Knee solution identification: Select the best compromise solution from the Pareto frontier, outputting final frequency and model order.
📊 Experimental simulation conclusions compared with mainstream unstructured algorithms: SPA, RAM, APG, VALSE MMV, verifying performance across multiple scenarios:
1. In noise resistance performance within a wide range of signal-to-noise ratios, MVESA has the lowest root mean square error (RMSE) in frequency estimation, with significantly higher success rate in model order identification under very low signal-to-noise ratios than compared algorithms.
2. As the number of sinusoidal components increases, MVESA consistently maintains lower errors and higher success rates, almost losing the ability to identify model orders compared to traditional SPA/RAM/APG.
3. Breakthrough in near-interval frequency resolution, capable of precisely separating even when frequency intervals are extremely small, with other algorithms largely unable to distinguish due to failure in relaxation metrics.
4. In scenarios where measurement data is missing, MVESA still stably estimates model order, maintaining a stable performance in frequency error estimation.
5. Computational complexity is slightly lower than RAM, APG, but slightly higher than VALSE MMV, SPA; Evolutionary algorithms inherently support parallel acceleration, making them easily adaptable for large-scale engineering applications.
🎯 Research Summary and Future Directions Key Contribution✅ Proposed multi-objective atomic l₀ norm LSE model, without relaxation or resolution limit, jointly estimating frequency and model order;✅ Invented variable-length evolutionary search strategy, adapting to unknown dynamic model orders;✅ Designed an order pruning mechanism, synchronizing algorithm convergence and population diversity;✅ Simulation results prove comprehensive superiority over existing mainstream algorithms in noise resistance, near-frequency resolution, missing data handling, and order identification.
Future Outlook 1 
Optimize matrix inverse computation to reduce computational time for large-scale line spectrum estimation;
2 
Improve algorithm statistical consistency, enhancing estimation performance under large measurement dimensions;
3 
Implement radar DOA estimation, communication channel estimation, and other engineering scenarios.
💡 Conclusion: Combining multi-objective evolutionary algorithms with unstructured line spectrum estimation breaks away from traditional convex relaxation frameworks, using intelligent optimization to solve the NP-hard sparse estimation problem, providing a new research paradigm for signal spectrum analysis.

## Images

![(DOA Estimation)Meshless Evolution Algorithm | New Method for Line Spectrum Estimation with Unknown Model Order | [Includes MATLAB Code]](01.jpg)
![(DOA Estimation)Meshless Evolution Algorithm | New Method for Line Spectrum Estimation with Unknown Model Order | [Includes MATLAB Code]](02.jpg)
![(DOA Estimation)Meshless Evolution Algorithm | New Method for Line Spectrum Estimation with Unknown Model Order | [Includes MATLAB Code]](03.jpg)
![(DOA Estimation)Meshless Evolution Algorithm | New Method for Line Spectrum Estimation with Unknown Model Order | [Includes MATLAB Code]](04.jpg)
![(DOA Estimation)Meshless Evolution Algorithm | New Method for Line Spectrum Estimation with Unknown Model Order | [Includes MATLAB Code]](05.jpg)
![(DOA Estimation)Meshless Evolution Algorithm | New Method for Line Spectrum Estimation with Unknown Model Order | [Includes MATLAB Code]](06.jpg)

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->

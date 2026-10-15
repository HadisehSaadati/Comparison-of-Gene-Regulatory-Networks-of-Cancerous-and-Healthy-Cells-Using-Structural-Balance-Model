# Project Overview

This project investigates how structural balance evolves under increasing disorder in two gene regulatory networks representing healthy and cancerous cells. It also examines the contributions of individual genes to this process. Using Boltzmann–Gibbs statistical mechanics, temperature is introduced as a disorder parameter. Network behavior is then analyzed by examining quantities derived from the mean-field solution of the structural balance Hamiltonian across different temperatures.

# Model

## Balance Theory

Structural Balance Theory, introduced by Fritz Heider in 1946 (Heider, Fritz. “Attitudes and cognitive organization.” The Journal of Psychology 21 (1946)), describes how positive and negative relationships between nodes in a signed network can generate structural tension. The balance of a relationship between two nodes depends not only on their direct connection but also on their relationships with a third node.
In this framework, triangles are the fundamental units of structural balance. A network is considered balanced when all its triangles are balanced, corresponding to either a paradise configuration, in which all links are positive, or a bipolar configuration, in which nodes divide into two groups with positive links within each group and negative links between them. Imbalanced triangles generate structural tension and tend to evolve toward balanced configurations through changes in link signs.

## Non-Zero Structural Balance Model

The non-zero-temperature structural balance model introduces a temperature parameter to control disorder in the network. Temperature governs the persistence of imbalanced triangles through a Boltzmann–Gibbs probability distribution: at lower temperatures, imbalanced configurations are less likely to persist, favoring structural balance, while higher temperatures allow greater disorder and tension in the network.
The Hamiltonian of the structural balance model describes the energy associated with the signed triangles in a network:
Here, 𝑠𝑖𝑗 denotes the sign of the link between nodes 𝑖 and 𝑗, while 𝐽𝑖𝑗𝑘 represents the weight assigned to the triangle formed by nodes 𝑖, 𝑗, and 𝑘. The Hamiltonian sums the contributions of all triangles, accounting for their signs and weights, and is normalized by the total absolute weight of the triangles. The negative sign ensures that balanced configurations correspond to lower energy, favoring structural balance as the system approaches its energy minimum.
Applying the mean-field approximation to this Hamiltonian allows several key quantities characterizing the structural balance model to be derived.
The order parameter q characterizes the structural state of the network. E defines the network energy as the average contribution of its triangles, providing a measure of structural balance. By examining how these quantities vary with temperature, we can investigate the network’s transition between ordered and disordered states.

# Data

This project analyzes signed, weighted, and sparse gene regulatory networks comprising 483 genes in healthy and chronic breast cancer cells. The networks were derived from statistical analyses of the expression levels of 20,532 genes in The Cancer Genome Atlas (TCGA), using data from 114 healthy samples and 764 cancer samples.

# Results

At zero temperature, both the healthy and cancerous gene regulatory networks exhibit energy values close to (-1), indicating that their triangles are almost entirely balanced and that ordered structures have emerged. As temperature increases, this order gradually breaks down. The network energy approaches zero, where balanced and imbalanced triangles are distributed without a dominant preference. The transition occurs at approximately (T = 10) for the healthy network and (T= 20) for the cancerous network, suggesting that the cancer network is more resistant to disorder and requires greater perturbation to disrupt its structural balance.
The order parameter shows no significant variation with temperature. To investigate this behavior, the link-sign distributions at zero temperature were examined, revealing random sign distributions consistent with a bipolar balanced structure in both networks.
Finally, the role of individual genes was investigated by measuring their participation in balanced triangles and their order parameter values at zero temperature. The results indicate that the same genes can behave differently in the healthy and cancerous networks, and that some genes contribute more strongly than others to the formation of the ordered network structure.



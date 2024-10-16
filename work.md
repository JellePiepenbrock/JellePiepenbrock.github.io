# Work
I'm a researcher working on machine learning and automated theorem proving. Currently I'm at the end of the PhD, so research job opportunities welcome! 

On the machine learning side, my work involves graph neural networks (GNNs) and transformer-based language models. I integrated these techniques with various formal mathematics systems, such as
first-order logic provers (eg. iProver and E), SMT solvers (cvc5) and interactive theorem proving systems (Coq). I've also used GNNs for program repair (repairing C code mistakes).

My PhD position is in the Data Science group at the ICIS institute at Radboud University Nijmegen. I'm also connected as a researcher to the Automated Reasoning department of the Czech Institute for Informatics, Robotics and Cybernetics (CIIRC) at the Technical University of Prague (where I spent 2 years). During my PhD I supervised MSc students on their thesis projects.

In August 2024, I was at the _Hausdorff Research Institute For Mathematics_ in Bonn, Germany to take part in the _Prospects of Formal Mathematics_ program.

-----
# Published Papers
## 2024
_Invariant Neural Architecture for Learning Term Synthesis in Instantiation Proving_ \
**Jelle Piepenbrock**, Josef Urban, Konstantin Korovin, Miroslav Olšák, Tom Heskes, Mikoláš Janota \
Journal of Symbolic Computation 

[_Graph2Tac: Online Representation Learning of Formal Math Concepts_](https://openreview.net/pdf?id=A7CtiozznN) \
Lasse Blaauwbroek, Mirek Olšák, Jason Rute, Fidel Ivan Schaposnik Massolo, **Jelle Piepenbrock**, Vasily Pestun \
ICML 2024

[_First Experiments with Neural cvc5_](https://easychair.org/publications/open/Z6b2) \
**Jelle Piepenbrock**, Mikoláš Janota, Josef Urban, Jan Jakubuv \
International Conference on Logic for Programming, Artificial Intelligence and Reasoning (LPAR 2024)

_Machine Learning for Quantifier Selection in cvc5_ \
Jan Jakubuv, Mikolas Janota, **Jelle Piepenbrock** and Josef Urban \
ECAI 2024

## 2023
_Guiding an Instantiation Prover with Graph Neural Networks_ \
Karel Chvalovský, Konstantin Korovin, **Jelle Piepenbrock**, Josef Urban \
International Conference on Logic for Programming, Artificial Intelligence and Reasoning (LPAR 2023)

_Graph Neural Networks for Mapping Variables Between Programs_ \
Pedro Orvalho, **Jelle Piepenbrock**, Mikoláš Janota, Vasco Manquinho \
ECAI 2023

## 2022 
_Guiding an automated theorem prover with neural rewriting_ \
**Jelle Piepenbrock**, Tom Heskes, Mikoláš Janota, Josef Urban \
International Joint Conference on Automated Reasoning

_The Isabelle ENIGMA_ \
Zarathustra A Goertzel, Jan Jakubův, Cezary Kaliszyk, Miroslav Olšák, **Jelle Piepenbrock**, Josef Urban \
13th International Conference on Interactive Theorem Proving (ITP 2022)

_Towards learning quantifier instantiation in SMT_ \
Mikoláš Janota, **Jelle Piepenbrock**, Bartosz Piotrowski \
25th International Conference on Theory and Applications of Satisfiability 

# Software
An incomplete list of projects I worked on.

[text2tac](https://github.com/JellePiepenbrock/text2tac) \
Text2Tac makes it possible to control the Coq theorem proving system with Language Models (such as GPT-style Transformers). 
It is part of the Tactician ecosystem. Find the introduction to the Tactician ecosystem [here](https://coq-tactician.github.io/api/).

[neural-synthesis](https://github.com/JellePiepenbrock/neural-synthesis) \
A neural system to synthesize instantiation terms in first-order logic problems. Internally uses both graph neural networks and recurrent neural networks.

[mlcvc5](https://github.com/JellePiepenbrock/mlcvc5-LPAR) \
The SMT solver cvc5 with an integrated graph neural network that performs premise selection and selects instantiation terms. 

[iprover-gnn-server](https://github.com/chvalovsky/iprover-gnn-server) \
Graph neural network-based guidance of the instantion-calculus based first-order automated theorem prover iProver. 

# Other

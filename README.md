# Binary Iterative Method for Non Adversarial Attack

### Please refer to [Report.pdf](Report.pdf).

Adversarial examples refer to the transforming the input by an adversary so that any general machine learning model
misclassify i.e the perturbed input results in the model outputting an incorrect answer with high confidence.

Our main aim is to experiment various methods to make adversarial attack such as Fast Gradient Method, Basic
Iterative Method, Virtual Adversarial Method using the InceptionV3 model.
We then evaluate them over pre-trained using InceptionV3, InceptionV2, ResNet V2 152 over classification
task.

To this end, we contribute a new method Binary Iterative Method which performs well over most of others methods on 1000 images sampled from the standard ImageNet dataset.

* Please refer to [Project_Proposal.pdf](Project_Proposal.pdf) for about the project.

Directory Structure
-------------------
<pre>
---README.md
---Project_Proposal.pdf
---Report.pdf
---code (Download from https://goo.gl/aV7xAR)
</pre>


To Run
------

Download code from https://goo.gl/aV7xAR (Checkpoints and dataset size limit the code to be added to github)


Dependencies:-
1. tensorflow
2. cleverhans(install using 'pip install -e git+http://github.com/tensorflow/cleverhans.git#egg=cleverhans' command)

Perform an attack:-
1. run the command './run_attack_fgm.sh' script for attack with FastGradientMethod
2. run the command './run_attack_bim.sh' script for attack with BasicIterativeMethod
3. run the command './run_attack_vam.sh' script for attack with VirtualAdversarialMethod
4. run the command './run_attack_binim.sh' script for attack with BinaryIterativeMethod

Evalute the modified images:-
1. run the command './evaluate_InceptionV3.sh XYZ' script for evalute over InceptionV3 
2. run the command './evaluate_InceptionV3.sh XYZ' script for evalute over InceptionV2
3. run the command './evaluate_Resnet.sh XYZ' script for evalute over ResnetV2_152 

Replace XYZ with the method(FGM, BIM, VAM, BinIM), whose dataset modifications user want to evalute.
e.g.: ./evaluate_InceptionV3.sh BinIM.

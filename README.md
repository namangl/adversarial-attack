Download code from https://drive.google.com/drive/u/1/folders/1eu3-KagRjawoOkXC9CN7mFaGj0a4Rz3W

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

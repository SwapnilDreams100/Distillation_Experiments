As the title suggests, it is a reproduction implementation of Born-Again Neural Networks (however, the network is simpler than the paper).

After learning in ./original_network.py, you can proceed with learning by using the model saved in ./born_again.py as a teacher model.
Perform learning

python born_again.py --temperature 10 --lambda_const 0.9 --teacher_model_path ./models/$hoge

About arguments

temperature is the temperature term when calculating the soft target, and lambda_const is the ratio of hard loss and soft loss. (See Distilling the Knowledge in a Neural Network)
Supplement

Here, since the networks of original_network.py and born_again.py are the same, it is Born-Again, but if you change this network, you can also perform normal Knowledge Distillation.

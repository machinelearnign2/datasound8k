# datasound8k

## Features Extraction
- Pesquisei nos folds todos
- Retirei os nomes dos audios todos (.wav)
- Criei um caminho para cada audio através do sitio onde estou
- Fiz librosa.load() de cada audio : Load an audio file as a floating point time series. Automaticamente o audio vai ser resample, por default, para sr=22500 Hz
- No entanto, o mais indicado para este caso seria um resample de sr=44100 Hz, uma vez que a tarefa exige uma representação mais detalhada das características do áudio para indicar a class do audio mais certa
- Através da repetição do audio, extendo os audios, aqueles que tiverem um tempo menor que 4 segundos, para 4 segundos

## Ajuda para deepfool
Dados pelo professor

https://openaccess.thecvf.com/content_cvpr_2016/papers/Moosavi-Dezfooli_DeepFool_A_Simple_CVPR_2016_paper.pdf

https://medium.com/machine-intelligence-and-deep-learning-lab/a-review-of-deepfool-a-simple-and-accurate-method-to-fool-deep-neural-networks-b016fba9e48e#:~:text=DeepFool%20finds%20the%20minimal%20perturbations,so%20the%20classification%20label%20changes

Encontrados

https://github.com/MyRespect/AdversarialAttack/blob/master/deepfool/deepfool_tf.py

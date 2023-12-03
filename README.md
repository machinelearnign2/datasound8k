# datasound8k

## Features Extraction
- Pesquisei nos folds todos e retirei os nomes dos audios todos (.wav)
- Criei um caminho para cada audio através do sitio onde o meu notebook se encontra
- Fiz librosa.load() de cada audio. Automaticamente o audio vai ser resample, por default, para sr=22500 Hz
- No entanto, o mais indicado para este caso seria um resample de sr=44100 Hz, uma vez que sample rates mais altas capturam detalhes mais finos do sinal, proporcionando uma representação mais precisa
- Através da repetição do audio, extendo os audios, aqueles que tiverem um tempo menor que 4 segundos, para 4 segundos
- De seguida, extraio as features, sendo elas:
    -  mfcc com parametro n_fcc=13
    -  mfcc com parametro n_fcc=40
    -  chromaspectrogram
    -  melspectrogram
    -  melspectrogram em decibéis
    -  melspectrogram com feature manipulation delta (ordem 1 e ordem 2)
- Criei um ficheiro JSON para cada feature, com colunas adicionadas do dataset dado: file (nome do audio), fold (fold a que pertence o audio), salience (se o audio é background ou foreground), classID (id da class a que pertence o audio: 0 = air_conditioner; 1 = car_horn; 2 = children_playing; 3 = dog_bark; 4 = drilling; 5 = engine_idling; 6 = gun_shot; 7 = jackhammer; 8 = siren; 9 = street_music)

## Ajuda para deepfool
Dados pelo professor

https://openaccess.thecvf.com/content_cvpr_2016/papers/Moosavi-Dezfooli_DeepFool_A_Simple_CVPR_2016_paper.pdf

https://medium.com/machine-intelligence-and-deep-learning-lab/a-review-of-deepfool-a-simple-and-accurate-method-to-fool-deep-neural-networks-b016fba9e48e#:~:text=DeepFool%20finds%20the%20minimal%20perturbations,so%20the%20classification%20label%20changes

Encontrados

https://github.com/MyRespect/AdversarialAttack/blob/master/deepfool/deepfool_tf.py

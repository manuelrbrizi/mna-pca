# Métodos Numéricos Avanzados - TP1

## Cómo usar
Corremos estas dos líneas:

`python extract_embeddings.py --dataset dataset --embeddings output/embeddings.pickle --detector face_detection_model --embedding-model openface_nn4.small2.v1.t7`

`python train_model.py --embeddings output/embeddings.pickle --recognizer output/recognizer.pickle --le output/le.pickle`

Ahora la línea que sigue depende de qué queremos hacer. Si queremos reconocer las caras de una foto usamos la siguiente línea reemplazando el "adrian.jpg" por la foto que querramos usar:

`python recognize.py --detector face_detection_model --embedding-model openface_nn4.small2.v1.t7 --recognizer output/recognizer.pickle --le output/le.pickle --image images/adrian.jpg`

Si queremos prender la camarita y que nos reconozca la carita usamos:

`python recognize_video.py --detector face_detection_model --embedding-model openface_nn4.small2.v1.t7 --recognizer output/recognizer.pickle --le output/le.pickle`

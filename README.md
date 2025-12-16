# Music Genre Recognition

This project explores automatic music genre classification using a convolutional neural network (CNN) trained on mel-spectrogram representations of audio. The model is evaluated on the GTZAN dataset, which contains 1,000 labeled 30-second music clips spanning ten common genres.


<img width="527" height="319" alt="Screenshot 2025-12-15 at 6 06 54 PM" src="https://github.com/user-attachments/assets/9c1a5aef-d344-48ae-beeb-d37a9b988a70" />


Each audio file is first converted into a mel-spectrogram using Librosa, transforming the time-frequency content of the signal into an image-like representation. These spectrograms are then used as input to a four-block CNN architecture composed of convolution, batch normalization, ReLU activation, and pooling layers, followed by a fully connected output layer with softmax probabilities.


<img width="449" height="163" alt="Screenshot 2025-12-15 at 6 05 33 PM" src="https://github.com/user-attachments/assets/48e20942-03c9-40d2-86e6-afb2ae46f0d5" />


Due to computational and time constraints, the model was trained without extensive data augmentation. Under these conditions, it achieves approximately **74–75% test accuracy**, consistent with reported human-level performance on this dataset. The model performs particularly well on spectrally distinct genres such as classical and metal, while showing more confusion among rhythmically similar genres.


<img width="440" height="417" alt="Screenshot 2025-12-15 at 6 06 13 PM" src="https://github.com/user-attachments/assets/79fc4efc-c303-412e-9f6e-73ac33ac3ac7" />



Future work includes large-scale data augmentation, transfer learning from pretrained audio models, and architectural extensions to better capture long-term temporal structure in music.


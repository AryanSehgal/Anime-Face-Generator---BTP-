# Anime Face Generator BTP

Contributors :-

##### Aryan Sehgal    - 2019UCS2019

##### Sourabh         - 2019UCS2025

##### Aditya Divyang  - 2019UCS2012

##### M Aman Chaudhry - 2019UCS2020

<hr style="border:2px solid gray">

Animations play an important role in our daily life and have been widely used in entertainment, social, and educational applications. We aim to automatically translate a photo-face into an anime-face based on the styles of a reference anime-face. We refer to such a task as Style-Guided Face-to-Anime Translation (StyleFAT). 

We implement a generator architecture that preserves the global information (e.g., pose) of a source photo-face, while transforming local facial shapes into anime-like ones and transferring colors/textures based on the style of a reference anime-face. Our insight is that the local shapes (e.g., large and round eyes) can be treated as a kind of style like color/texture. In this way, transforming a face’s local shapes can be achieved via style transfer. To transform local facial shapes via style transfer, we explore where to inject the style information into the generator. In particular, the multi-layer feature maps extracted by the decoder represent multi-level semantics (i.e., from high-level structural information to low-level textural information). Our generator therefore injects the style information into the multi-level feature maps of the decoder. Guided the injected style information and different levels of feature maps, our generator adaptively learns to transfer color/texture styles and transform local facial shapes.


![WhatsApp Image 2022-09-28 at 20 25 32](https://user-images.githubusercontent.com/59551957/192975719-13b92ff6-f157-401f-87a7-4599ea5f0f63.jpeg = 200x300)


In addition to the generator, we propose a double-branch discriminator that explicitly considers large appearance variations between photo-faces and anime-faces as well as variations among anime images. The double-branch discriminator not only learns domain-specific distributions by two branches of convolutional layers, but also learns the distributions of a common space across domains by shared shallow layers

![WhatsApp Image 2022-09-28 at 20 30 00](https://user-images.githubusercontent.com/59551957/192975687-ea2c4d09-b46f-4bb2-a2bb-97e0a081a8e1.jpeg = 200x300)


* After experimenting with miultiple different archtectures for content encoder and style encoder, we came up with the following architecture 

## Content Encoder


![Content Encoder Architecture](https://user-images.githubusercontent.com/59551957/192975797-40b524a5-e017-421c-bfb6-d6c3ccff77b8.jpeg)


## Style Encoder


![Style Encoder Architecture New](https://user-images.githubusercontent.com/59551957/192975853-59b43434-1c4a-46c5-bf88-651c42b7c552.jpeg)



<hr style="border:2px solid gray">

### References :-
AniGAN: Style-Guided Generative Adversarial Networks for Unsupervised Anime Face Generation

H. Lee, Hung-Yu Tseng, Qi Mao, Jia-Bin Huang, Yu-Ding Lu, Maneesh Singh, and Ming-Hsuan Yang. Drit++: Diverse image-to-image translation via disentangled representations. Int. J. Comput. Vis., pages 1–16, 2020

Liqian Ma, Xu Jia, Stamatios Georgoulis, Tinne Tuytelaars, and Luc Van Gool. Exemplar guided unsupervised image-to-image translation with semantic consistency

Ming-Yu Liu, Xun Huang, Arun Mallya, Tero Karras, TimoAila, Jaakko Lehtinen, and Jan Kautz. Few-shot unsupervised image-to-image translation

Jun-Yan Zhu*, Taesung Park*, Phillip Isola, and Alexei A. Efros. "Unpaired Image-to-Image Translation using Cycle-Consistent Adversarial Networks"

A Style-Based Generator Architecture for Generative Adversarial Networks by Tero Karras, Samuli Laine, Timo Aila

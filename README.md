# Mitosis-Count
## cyclegan_mitosis.ipynb
* Here our aim is to convert low intensity images of mitosis count to high intensity images (i.e kmit-mitosis(256x256) quality to icpr-mitosis(512x512) quality).
* cyclegan_mitosis.ipynb contains code in which for now the dataset is horse2zebra where horse size is 256 * 256 and zebra size is 512 to 512 later they can be replaced with *horse -> kmit(256x256)* and *zebra -> icpr(512x512)* .
* In this code now I'm able to run code without any errors but it is slow.
* Changes have to be done accordingly.
* Output shown is for two epochs (you can only see half a epoch but the cell had previously ran).
* Original paper used *identity loss* , I have removed it since the input and output size of particular generator is not same(might be the reason we are getting not so good background also the model is trained for only 2 epochs so that might effect as well).
* We have only used teo losses *1.Adversarial loss 2.Cycle consistency loss.*. but in the original paper three losses were used including identity loss.
* Identity mapping loss:   An identity mapping loss was in-troduced in the original CycleGAN to preserve color com-position for a task of painting→photo. We also impose theidentity mapping loss forGXY↓to avoid color variation:Lidt(GXY↓) =‖GXY↓(y↓)−y↓‖1
* Unpaired Image Super-Resolution using Pseudo-Supervision (https://openaccess.thecvf.com/content_CVPR_2020/papers/Maeda_Unpaired_Image_Super-Resolution_Using_Pseudo-Supervision_CVPR_2020_paper.pdf)
* wasserstein Loss:   https://www.coursera.org/lecture/build-basic-generative-adversarial-networks-gans/wasserstein-loss-vy3To

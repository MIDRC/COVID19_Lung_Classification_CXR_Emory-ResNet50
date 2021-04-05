# COVID19_Lung_Classification_CXR_Emory_ResNet50

**MIDRC CRP-2: Machine intelligence algorithms from multi-modal, multi-institutional COVID-19 data**    
(https://www.midrc.org/midrc-collaborating-research-projects/project-one-crp2)  

**Modality:** X-ray  

**Requirements:** Python, Keras, Tensorflow, Numpy, OpenCV, Matplotlib  

Over the past year, the COVID-19 pandemic has put immense strain on the hospital systems around the world. One of the most significant issues these systems face is how to efficiently and reliably diagnosis whether a patient is positive or negative for the virus. In this study, we develop an end-to-end pipeline for the classification of chest X-rays that may belong to COVID-19 positive patients. This will enable real time diagnosis of the virus in the field without having to wait 24-48 hours for the results of an RT-PCR test or the less accurate results of a rapid antigen test. This model’s pipeline consists of two phases: pretraining and fine-tuning. Both phases use Keras 2.4.1 with a Tensorflow backend. A ResNet50 is used in both phases as a feature extractor with additional fully connected and classification layers as the top layers of the model. The image data is then normalized to pixel values between [0, 1] and augmented with random horizontal flipping before being fed through the model. After training, the model outputs a probability which is converted to a binary prediction of whether the patient is predicted to have COVID-19. Each phase in the model pipeline is trained on a different set of data. In the pretraining phase, the model is trained on the open-source chest X-ray dataset CheXpert to allow the model to distinguish the difference between a chest X-ray with abnormalities and a chest X-ray without abnormalities. We filtered the dataset to only include the frontal view of the X-ray. In the fine-tuning phase, we used 2,002 X-rays of patients admitted to the Emory Hospital system this past year. Half of those patients were COVID-19 positive via an RT-PCR test while the other half of the patients tested negative via the same test. 





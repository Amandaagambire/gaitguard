# Gait Biometrics Reseach : Gait-Guard
<a href="#"><img alt="Python" src="https://img.shields.io/badge/Python-00543D.svg?logo=python&logoColor=white"></a>
<a href="#"><img alt="Pandas" src="https://img.shields.io/badge/Pandas-006750.svg?logo=pandas&logoColor=white"></a>
<a href="#"><img alt="NumPy" src="https://img.shields.io/badge/Numpy-008B76.svg?logo=numpy&logoColor=white"></a>
<a href="#"><img alt="Matplotlib" src="https://img.shields.io/badge/Matplotlib-55A38B.svg?logo=matplotlib&logoColor=white"></a>
<a href="#"><img alt="TensorFlow" src="https://img.shields.io/badge/TensorFlow-A4C9BB.svg?logo=TensorFlow&logoColor=white"></a>
<a href="#"><img alt="Keras" src="https://img.shields.io/badge/Keras-C5DDD6.svg?logo=Keras&logoColor=white"></a>

by **[Amanda Agambire](https://www.linkedin.com/in/amanda-agambire/)**

Aug 2024

## Project Description
With the rise of smart security systems and wearable technology, authenticating users based on their natural behavior has become a promising frontier. One such behavioral biometric is gait—the unique way a person walks. However, most gait-based systems remain vulnerable to spoofing attacks and privacy breaches.

GaitGuard is an  AI system I developed to test & address these issues by enabling secure and privacy-preserving gait authentication. The system uses time-series data from accelerometers and gyroscopes—typically from smartphones or wearable devices—to learn and identify each user's walking signature. By leveraging a combination of CNN+LSTM deep learning, TSFRESH-based time-series feature extraction, differential privacy techniques, and adversarial robustness defenses, GaitGuard ensures secure login access even in the face of sophisticated spoofing attempts.

Ideally, the final application can be integrated into smart home systems, surveillance networks, or wearable apps—providing seamless and secure biometric authentication without sacrificing user privacy.





https://user-images.githubusercontent.com/105242871/188296043-cff403bd-83a1-41c5-b604-1d307a223e5a.mov



## Project Goal
Our goal is to buld the model that supports the "behind the scene" of the mobile application, which uses **deep learning** and **conbolutional neural network**.

![early_and_late](https://user-images.githubusercontent.com/105242871/188295263-761359b7-497f-4563-8df5-a2360e2c8bf0.jpeg)

## Process
#### :one:   Data Acquisition


A team of annotators who work closely with the farmers to collect the images from the fields and annotate the image either it's a healhy potato leaf or if it has any diseases using domain knowledge. The team collected 2152 potato-leaf images in total.

#### :two:   Data Preparation

- **tf dataset**

- **Resize & Scale**

- **Data augmentation**

<details>
<summary> Data Splitting </summary>

- Create function `get_dataset_partitions_tf()` to split data into **train, validate, test**

- Test prepare function

- Check the size of each dataset
     ```sh
     len(train), len(validate), len(test)
     ```
- Call the function, and cache e the 3 data samples
     ```sh
    train = train.cache().shuffle(1000).prefetch(buffer_size = tf.data.AUTOTUNE)
    validate = validate.cache().shuffle(1000).prefetch(buffer_size = tf.data.AUTOTUNE)
    test = test.cache().shuffle(1000).prefetch(buffer_size = tf.data.AUTOTUNE)
     ```
</details>

#### :three:    Modeling
- Define neural network architecture

- Build model on training dataset and evaluate on train and validate

- Use optimizer to compile

- Fit model on test dataset on evaluate model based on accuracy

- Plot accuracy and loss function of train and validate datasets from all 50 epochs.

- Make prediction on test dataset and save model

- Ajdust neural network architecture and optimizer, using steps above to generate and save new mdoel

- Deploy the top performing model

## Conclusion
The neurol network model has an accuracy of 99% on test dataset, and it's expected to perform with the equivalent accuracy level on future onseen data.

<img width="883" alt="predictions" src="https://user-images.githubusercontent.com/105242871/188297747-98a86bb0-2296-4136-9048-698f71e47d72.png">

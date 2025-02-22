# Acoustic drone detection

## Abstract

The Acoustic Drone Detection project develops a cost-effective system for identifying drones based on their unique acoustic signatures. With increasing drone usage in various sectors, unauthorized activity poses security risks. Traditional detection methods have limitations, making an acoustic-based approach a scalable alternative.

![image](https://github.com/user-attachments/assets/9b6fabb4-ef1c-4d1d-83c5-7892ecd04e9c)


## Features

* Integration with a parabolic microphone for enhanced sensitivity to recored drone sounds.
* Machine learning-based classification using SVM.
* High detection accuracy in diverse environmental conditions.
* Graphical user interface for post-processing analysis and visualization.
* Easy to set up and deploy.


## Usage
#### Install Required Dependencies
```python
pip install pydub librosa numpy pandas scikit-learn joblib
```
#### Prepare Your Dataset (initial run or dataset change)
* Store drone and non-drone audio recordings in ZIP files.
* Run the script to process ZIP files and extract audio features:
```python
if __name__ == "__main__":
    zip_file_path = "/content/Drone_noise/drone_new.zip"
    label = "drone"
    features_df = process_single_zip_folder(label, zip_file_path, chunk_length_ms=1000)
    print("\nFirst few rows of extracted features:")
    print(features_df.head())

# Example usage
if __name__ == "__main__":
    zip_file_path = "/content/NO_Drone_noise/no_drone_outside_2.zip"
    label = "NO_drone"
    features_df = process_single_zip_folder(label, zip_file_path, chunk_length_ms=1000)
    print("\nFirst few rows of extracted features:")
    print(features_df.head())
```
##### after the zip file upload you should get dataset CSV files save them and upload them  using the gui and upload the recorded drone sound for analysis as shown in the picture above:

![image](https://github.com/user-attachments/assets/f79ff3d8-3ca6-4d2a-9c47-0c75e7dbb061)

## Sources

You can find all resources files in the following google drive link:

https://drive.google.com/drive/folders/1O4kz1f_RR_YCqm99dzzJm-ltSxdNyRqz?usp=drive_link 


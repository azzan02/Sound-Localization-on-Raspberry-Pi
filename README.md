# Real-Time Multi-Microphone Audio Analysis and Whistle Detection
This project provides a real-time audio processing and visualization tool for multiple microphones. It includes waveform and frequency spectrum plots for each microphone and features whistle detection with timestamped alerts.

## Features
### Real-Time Audio Processing:
Processes audio streams from multiple microphones in real-time.

### Waveform and Spectrum Visualization:
Displays the waveform and frequency spectrum of each microphone.

### Whistle Detection:
Detects high-frequency whistles within a specific frequency range (3000-6000 Hz) and logs the timestamps of detection.

### First Microphone Detection:
Identifies and logs which microphone detects a whistle first.


## Installation
### Clone the Repository:
```
git clone https://github.com/azzan02/Sound-Localization-on-Raspberry-Pi.git  
cd repo-name
```

### Install Dependencies:
Ensure you have Python 3.x installed. Install the required libraries:
```
pip install pyaudio numpy matplotlib
```

### Configure Microphone Device IDs:
Update the **MIC_DEVICE_IDS** variable in the script with the device IDs of your microphones

## Usage
### 1. Run the script 
Execute the script to start real-time audio processing:
```
python main.py  
```
### 2. Visualization:
The script generates live waveform and spectrum plots for each microphone.

### 3. Whistle Detection:
  - When a whistle is detected, it prints the detection timestamp and the microphone number to the console.
  - If all microphones detect a whistle, it identifies which microphone detected it first.

## Whistle Detection Parameters
  - **whistle_threshold:** Adjust this value based on the intensity of the whistles. Default is 150.
  - **whistle_freq_range:** Frequency range for whistle detection. Default is (3000, 6000) Hz.

## How It Works
### 1. Multithreading:
Each microphone's audio processing runs in a separate thread for efficient real-time performance.

### 2. Queue System:
A queue is used for thread-safe communication between audio processing and visualization.

### 3. FFT Analysis:
The script uses a Fast Fourier Transform (FFT) to compute the frequency spectrum for whistle detection.

## Customization
  - ### Plot Appearance:
    Modify the **axs** configurations to customize the appearance of plots.
  - ### Microphone Count:
    Update the **NUM_MICROPHONES** variable to change the number of microphones.   

# Lab 7 for [[ENSC 180]]
## Code: 
```
% Load the signal
load handel.mat; % Load the "handel.mat" signal
y = y(1:25600); % Work with only the first 25600 samples

% Plot the original signal
subplot(3, 1, 1); % Arrange plots
plot(y);
title('Original Signal');
xlabel('Sample Index');
ylabel('Amplitude');

% Play the original signal
sound(y, Fs); % Play original sound
pause(length(y)/Fs + 1); % Wait for the sound to finish plus a little extra

% Time Domain Threshold
T = 0.1; % Example threshold value
y2 = y; % Make a copy of y for time domain processing
y2(abs(y2) < T) = 0; % Perform thresholding

% DCT Domain Processing
M = 64; % Define the block size for the DCT
C = dct(eye(M)); % Create the DCT matrix
y3 = zeros(size(y)); % Initialize y3 for DCT domain processing
for i = 0:(length(y)/M)-1
    block = y(1+i*M:(i+1)*M); % Extract block
    z = C * block; % Transform to DCT domain
    z(abs(z) < T) = 0; % Perform thresholding
    y3(1+i*M:(i+1)*M) = C' * z; % Transform back to time domain
end

% Plot time domain processed signal
subplot(3, 1, 2); % Arrange plots
plot(y2);
title(['Time Domain Processed Signal with Threshold ', num2str(T)]);
xlabel('Sample Index');
ylabel('Amplitude');

% Plot DCT domain processed signal
subplot(3, 1, 3); % Arrange plots
plot(y3);
title(['DCT Domain Processed Signal with Threshold ', num2str(T)]);
xlabel('Sample Index');
ylabel('Amplitude');

% Play the processed signals
disp('Playing time domain processed signal...');
sound(y2, Fs); % Play time domain processed sound
pause(length(y2)/Fs + 1); % Wait for the sound to finish plus a little extra

disp('Playing DCT domain processed signal...');
sound(y3, Fs); % Play DCT domain processed sound
pause(length(y3)/Fs + 1); % Wait for the sound to finish plus a little extra

% Calculate and display Mean Absolute Error (MAE)
time_domain_MAE = mean(abs(y2 - y));
dct_domain_MAE = mean(abs(y3 - y));
fprintf('Time Domain MAE: %f\n', time_domain_MAE);
fprintf('DCT Domain MAE: %f\n', dct_domain_MAE);
```

## Output:
### T = 0
```
Playing time domain processed signal...

Playing DCT domain processed signal...

Time Domain MAE: 0.000000  
DCT Domain MAE: 0.000000
```
![[Lab 7-20240308052738496.webp]]
### T = 0.1
```
Playing time domain processed signal...

Playing DCT domain processed signal...

Time Domain MAE: 0.021395  
DCT Domain MAE: 0.027969
```

![[Lab 7-20240308052046975.webp|650]]
### T = 0.3
```
Playing time domain processed signal...

Playing DCT domain processed signal...

Time Domain MAE: 0.089035  
DCT Domain MAE: 0.064208

```
![[Lab 7-20240308052924487.webp]]
## Explanation: 
- Loads `handel.mat` audio file.
- Adjusts audio clip length.
- Verifies variables' successful loading.
- Plots original audio waveform.
- Plays original audio clip.
- Applies time domain threshold.
- Thresholds blocks in DCT domain.
- Recalculates blocks to time domain.
- Plots thresholded time domain signal.
- Plots thresholded DCT domain signal.
- Plays time domain processed audio.
- Plays DCT domain processed audio.
- Computes Mean Absolute Error (MAE).
- Prints time domain MAE.
- Prints DCT domain MAE.

 (T) of 0, 0.1, and 0.3, a value of 0.1 generally strikes a balance between preserving audio quality and reducing noise without overly compromising signal integrity.

# Bela-PureDataDemos
Examples using Pure Data and Bela

Spectral_processing_demo.pd
- *Start here:* basic Fourier analysis and plotting
- Tutorial on different input signals and frame (block)-based processing using Fast Fourier Transform (FFT)
- Plots magnitude spectrum in different forms and different frequency ranges

process_spectrum.pd
- Compute magintude FFT of input audio
- Write to table spectrum_dB for plotting and other operations
- creates frame_trigger signal to synchronize block-based operations

pitch_tracker.pd
- Estimates pitch from input audio using a simple FFT peak-based heuristic (largest peak between ~261-522 Hz).
- Converts fundamental frequency (in Hz) to a MIDI note number (e.g., 261 Hz -> C3 -> MIDI: 60)

servo_angle.pd
- Simple servo control for Bela in PureData
- Creates pulse-width modulation (PWM) signal for servo positioning, based on input angle

MIDI_Servo.pd
- Converts MIDI note input into a servo angle (for simple Bela xylophone)
- Positions servo using PWM (servo_angle)

Pitch_MIDI_Servo.pd
- Full system to controls xylophone servos with Bela using pitch from audio input
- Positive zero-crossing in magnitude dB spectrum triggers a new MIDI note
- New note triggers an angle change in servo 1, followed by a rapid hit in servo 2 (mallet) 


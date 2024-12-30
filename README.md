# Upscale Jupyter Notebook

This repository contains a Jupyter Notebook designed to demonstrate super-resolution using GFPGAN for enhancing video quality. The notebook provides step-by-step instructions for loading models, processing frames, and reconstructing a high-quality video. It also integrates audio into the processed video.

## Features

- **Super-resolution with GFPGAN**: Utilizes GFPGAN to upscale video frames and enhance facial details.
- **Video Frame Processing**: Demonstrates extraction, processing, and reassembly of video frames.
- **Audio Integration**: Combines the enhanced video with audio to produce a final output.
- **Short Video Testing**: Designed to process videos of 3 seconds for efficient testing.

## Requirements

### Dependencies
To use the notebook, ensure the following Python libraries are installed:

- `torch`
- `torchvision`
- `gfpgan`
- `opencv-python`
- `ffmpeg-python`

You can install them using pip:
```bash
pip install torch torchvision gfpgan opencv-python ffmpeg-python
```

### Pretrained Weights
Download the GFPGAN model weights and place them in the `./weights` directory:

- GFPGAN model: [GFPGANv1.4.pth](https://github.com/TencentARC/GFPGAN/releases)

Ensure the path to the weights file is correctly specified in the notebook.

## How to Run

1. Clone the Repository:
   ```bash
   git clone [<repository-url>](https://github.com/AD9190/Upscale_GFGAN)
   cd Upscale_GFGAN
   ```

2. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

3. Open the notebook:
   Navigate to the `Upscale.ipynb` file in your Jupyter environment.

4. Follow the Steps:
   - Execute cells sequentially.
   - Load the model, process the video, and integrate audio.

5. Input Files:
   - Ensure your input video (3 seconds, `.mp4`) and audio (`.mp3`) files are in the correct directories as specified in the notebook.

6. Output:
   - The processed video with enhanced resolution will be saved in the specified output path.

## Notes
- The notebook assumes a short video duration (3 seconds) to minimize processing time during testing.
- Higher-duration videos can significantly increase runtime.
- Ensure that `ffmpeg` is installed and accessible from your command line.

### Testing
To test the setup, use a 3-second video file containing a visible face and verify the enhanced output.

## Troubleshooting

### Common Errors
- **`ModuleNotFoundError`**: Ensure all dependencies are installed with compatible versions.
- **Model Loading Errors**: Verify that the GFPGAN model weights are correctly downloaded and placed in the `./weights` directory.

### Debugging Steps
- Check the versions of `torch` and `torchvision`:
  ```bash
  pip show torch torchvision
  ```
- Update dependencies if required:
  ```bash
  pip install --upgrade torch torchvision
  ```

For further assistance, refer to the GFPGAN [documentation](https://github.com/TencentARC/GFPGAN) or open an issue in this repository.



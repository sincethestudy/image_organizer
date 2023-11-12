# Image Organization Tool

## Overview
This tool is designed to automatically organize images on your computer by labeling and sorting them into a structured folder system. It utilizes the OpenAI GPT model to generate meaningful labels for images and suggests an optimal folder structure based on these labels.

## Features
- **Image Discovery**: Scans specified directories for images.
- **Image Labeling**: Utilizes AI to label images with semantically relevant names.
- **Folder Structure Creation**: Suggests and creates a folder structure based on image labels.
- **Supports Multiple Formats**: Works with PNG, JPG, JPEG, and GIF formats.

## Requirements
- Python 3.x
- OpenAI Python package
- OS and fnmatch modules (typically included in standard Python distributions)

## Installation
1. Ensure Python 3.x is installed on your computer.
2. Install the OpenAI Python package using pip:
   ```bash
   pip install openai
   ```

## Usage
1. **Configure Directories**:
   Edit `DIRS_TO_INDEX` in the script to include the directories you want to scan for images.
   ```python
   DIRS_TO_INDEX = ['/path/to/directory1', '/path/to/directory2']
   ```

2. **Run the Script**:
   Execute the script in your Python environment.
   ```bash
   python maine.py
   ```

3. **Review Results**:
   The script will output a JSON file (`structure.json`) with the suggested folder structure. Images will be automatically labeled and organized based on this structure.

## How It Works
- The script scans the specified directories for images.
- Each found image is encoded in Base64 and sent to the OpenAI model for labeling.
- Based on the labels, a folder structure is suggested and created.
- Images are then sorted into this structure, with symlinks created for organization.

## Customization
- Modify the image file types or directories as needed.
- Adjust `IMGS_TO_LABEL_COUNT` to change the number of images labeled in a session.

## Note
- This tool is dependent on the OpenAI API, which requires an API key.
- Ensure you have the necessary permissions to read and write to the specified directories.

## Contributing
Contributions to improve this tool or extend its functionalities are welcome. Please follow the standard procedures for contributing to a GitHub project.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

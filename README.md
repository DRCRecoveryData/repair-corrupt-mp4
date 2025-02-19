# repair-corrupt-mp4

## Description
This repository contains scripts to repair corrupted MP4 files using Python. The scripts can extract and regenerate `moov` atoms and recover sample tables from `mdat` atoms in MP4 files.

## Usage
### Scripts
- `mov.py`: Main script to parse and repair MP4 files.
- `chunk.py`: Parses and processes MP4 files, focusing on extracting and printing details about various MP4 atoms and their sample tables.
- `rawaac.py`: Extracts AAC audio data from corrupted MP4 files.

### How to Use
1. **mov.py**:
   - Basic Usage: `python mov.py -s corrupted.mp4`
   - Advanced Usage: `python mov.py -s corrupted.mp4 -r reference.mp4 -o output.mp4 -v -k`
   - Options:
     - `-s file`: Source file (corrupted MP4).
     - `-r file`: Reference file (complete MP4).
     - `-o file`: Output file (recovered MP4).
     - `-v`: Verbose mode.
     - `-k`: Keep temporary files.

2. **chunk.py**:
   - Usage: `python chunk.py in.mp4`
   - Functionality: Reads the MP4 file and processes different types of boxes (atoms) such as `moov`, `trak`, `stsc`, `stsz`, and `stco`.

3. **rawaac.py**:
   - Usage: `python rawaac.py in.mp4 out.aac`
   - Functionality: Extracts AAC audio data from the input MP4 file and writes it to the output AAC file.

## Reference
"moov atom not found": 不完全で再生できないMP4をPythonで復元する - cBlog https://yaritakunai.hatenablog.com/entry/repair-corrupt-mp4

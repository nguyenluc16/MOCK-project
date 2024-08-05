
# Media Browser and Player CLI Application

This project is a Command Line Interface (CLI) application for Linux, written in C/C++, that serves as a basic media files and video files browser/player.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Dependencies](#dependencies)
- [Contributing](#contributing)
- [License](#license)

## Features

1. **Universal Accessibility**:
   - Runs from any directory on your computer.
   - Supports external devices (e.g., USB). The application can mount devices, parse files, and navigate directories on external storage.

2. **Media Browsing**:
   - View a list of media files (audio and video) in the current folder and all sub-folders.
   - Supports pagination, displaying 25 files per page.

3. **Playlist Management**:
   - List all available playlists.
   - View details of a specific playlist.
   - Create, update, and delete playlists.

4. **Metadata Management**:
   - Display detailed metadata of media files using Taglib.
     - Audio Metadata: Track name, Album, Artist, Duration, Genre, Publisher, Publish Year, etc.
     - Video Metadata: Name, Size, Duration, Bitrate, Codec, etc.
   - Edit metadata, including changing values and adding new keys.

5. **Media Playback**:
   - Play music directly from the application using the SDL2 library on a separate thread.
   - Playback controls include Play/Pause, Next/Previous track, and automatic progression to the next song.
   - Display the current playback time and total duration of the track.
   - Adjust the device volume from within the application.

## Installation

### Prerequisites

- **C/C++ Compiler**: Ensure you have a C/C++ compiler installed (e.g., `gcc`).
- **SDL2 Library**: Install the SDL2 library.
- **Taglib**: Install Taglib for metadata handling.

### Steps

1. **Clone the Repository**
    ```bash
    git clone https://github.com/yourusername/media-browser-player.git
    cd media-browser-player
    ```

2. **Build the Application**
    ```bash
    make
    ```

## Usage

1. **Run the Application**
    ```bash
    ./media_browser_player
    ```

2. **Command Options**
    - **View Media Files**: List all media files in the current directory and sub-folders.
      ```bash
      ./media_browser_player --list
      ```

    - **Manage Playlists**:
      - **List Playlists**:
        ```bash
        ./media_browser_player --playlists
        ```
      - **View a Playlist**:
        ```bash
        ./media_browser_player --playlist <playlist_name>
        ```
      - **Create/Update/Delete a Playlist**:
        ```bash
        ./media_browser_player --playlist <create|update|delete> <playlist_name>
        ```

    - **View and Edit Metadata**:
      - **View Metadata**:
        ```bash
        ./media_browser_player --metadata <file_name>
        ```
      - **Edit Metadata**:
        ```bash
        ./media_browser_player --metadata-edit <file_name> <key> <value>
        ```

    - **Playback Control**:
      - **Play/Pause**:
        ```bash
        ./media_browser_player --play <file_name>
        ```
      - **Next/Previous**:
        ```bash
        ./media_browser_player --next
        ./media_browser_player --previous
        ```
      - **Adjust Volume**:
        ```bash
        ./media_browser_player --volume <level>
        ```

## Dependencies

- **SDL2 Library**: [SDL2 Installation Guide](https://wiki.libsdl.org/Installation)
- **Taglib**: [Taglib Installation Guide](https://taglib.org/download/)

## Contributing

Contributions are welcome! Please fork the repository, create a new branch, and submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

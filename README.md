# khinsider_csharp

## Overview
`khid_csharp` is a C# command-line tool that scrapes and downloads game soundtrack albums from [KHInsider](https://downloads.khinsider.com/).  
This rewrite of the original Python project leverages **HtmlAgilityPack** and asynchronous I/O in .NET to efficiently fetch and download `.flac` audio files. It was built as a hobby project to provide a tactile, CLI-friendly way to batch-download tracks.

## Features
- Scrapes album pages to collect track entries.
- Resolves direct `.flac` download links from track pages.
- Interactive prompt for each file:
  - `y` → download the file
  - `n` → skip the file
  - `q` → quit gracefully
- Asynchronous file downloads using `HttpClient`.

## Installation
Clone the repository and build the project:

```bash
git clone https://github.com/siddegir/khinsider_scraper_csharp.git
cd khinsider_scraper_csharp
dotnet build
```

Make sure you have the [.NET SDK](https://dotnet.microsoft.com/download) installed.

## Usage
Run the compiled executable with an album URL:

```bash
program.exe "https://downloads.khinsider.com/game-soundtracks/album/example-album"
```

You’ll be prompted for each track:

```
Download |trackname.flac| y/n/q?
```

## Requirements
- .NET 7.0 or later
- [HtmlAgilityPack](https://html-agility-pack.net/) (installed via NuGet)

## Limitations
- Downloads are interactive by design (no fully automated batch mode).
- KHInsider site structure may change, which could break scraping logic.
- Currently targets `.flac` files only.

## License
This project is licensed under the MIT License.  
See the [LICENSE](LICENSE) file for details.

## Contributing
Contributions are welcome!  
Open issues or submit pull requests for bug fixes, new features, or documentation improvements. Even small tweaks are appreciated.

## Credits
Created entirely by me as a hobby project.

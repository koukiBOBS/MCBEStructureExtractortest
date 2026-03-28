# MCBE Structure Extractor

A browser-based tool to extract structure templates (`.mcstructure`) from Minecraft Bedrock Edition world files (`.mcworld` or `.zip`).  
It automatically handles nested directories (e.g., iOS manual compression) and supports structure keys with the `structuretemplate_mystructure:` prefix.

## Features

- Works entirely in the browser – no server required.
- Automatically flattens nested folders inside ZIP archives (common on iOS).
- Extracts structures saved with the `mystructure:` namespace.
- Preserves Unicode names (Chinese, Japanese, etc.).
- Packages all extracted structures into a downloadable ZIP file.
- Supports both `.mcworld` and `.zip` files.

## How to Use

https://koukibobs.github.io/MCBEStructureExtractortest/

## Technical Details

- Uses [`mcbe-leveldb-reader`](https://www.npmjs.com/package/mcbe-leveldb-reader) to parse the LevelDB database.
- Built with vanilla JavaScript and the [JSZip](https://stuk.github.io/jszip/) library.
- Supports extraction of any key starting with `structuretemplate_mystructure:` (the default namespace used by Minecraft Bedrock).

## Acknowledgments

- Special thanks to [superllama88888](https://www.npmjs.com/~superllama88888) for creating the excellent [`mcbe-leveldb-reader`](https://www.npmjs.com/package/mcbe-leveldb-reader) library, which makes this tool possible.
- Also thanks to the maintainers of [JSZip](https://stuk.github.io/jszip/) for providing a robust ZIP handling solution.
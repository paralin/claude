# Claude CLI

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Python Version](https://img.shields.io/badge/python-3.6%2B-blue)](https://www.python.org/downloads/)

A command-line interface for interacting with Anthropic's Claude Opus AI model.

## Installation

1. Clone the repository or download the `claude` script.

```
wget -O ./claude https://raw.githubusercontent.com/paralin/claude/master/claude
```

2. Make the script executable:

```
chmod +x claude
```

3. (optional) Move the script to a directory in your PATH, e.g.:

```
cp claude ~/.local/bin/
```

## Usage

Set your Anthropic API key as an environment variable:

```
export ANTHROPIC_API_KEY=your_api_key_here
```

To use the CLI, simply run the `claude` command followed by your input text:

```
./claude
Rewrite this program correctly: <code>stdos.stdout.logthis("hello world")</code>
```

Then press ctrl+d to end the input.

You can also pipe input to the script:

```
echo "Hello, how are you?" | claude
```

Or a file:

```
cat prompt.txt | claude
```

If you're feeling brave:

```
echo "Show me what is in my home directory." | claude bash | bash
```


### Templates

The script supports predefined templates. To use a template, pass its name as the first argument:

```
claude spanish "Hello, how are you?"
```

Available templates:

- `spanish`: Translates the input text to Spanish (basic example).
- `bash`: Output an executable bash script from the input.

## Acknowledgements

- [Anthropic](https://www.anthropic.com/) for creating the Claude AI model.
- [litellm](https://github.com/kaiokendev/litellm) for the Python library to interact with the Anthropic API.

## License

MIT

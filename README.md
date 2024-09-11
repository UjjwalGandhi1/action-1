## cowsay-dragon: Generate Dragon Cowsay Artwork from a List

This GitHub Action reads a list of messages from a file and generates cowsay artwork with a dragon for each message. 

**Features:**

* Uses `cowsay` to create ASCII art cows with dragon theme.
* Reads messages from a user-defined list file.
* Generates a separate image for each message.

### Usage

1. **Create a list file:** Create a file named `messages.txt` (or any desired name) in the root of your repository. Add each message you want to display in the cowsay artwork on a separate line.
2. **Add the action to your workflow:** In your `.github/workflows` directory, edit your workflow file (e.g., `ci.yml`) and add the following YAML snippet:

```yaml
jobs:
  cowsay-dragon:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v3
    - name: Generate cowsay images
      uses: ./ # Path to your action (replace with actual path)
      with:
        message_file: path/to/your/messages.txt  # Adjust path if needed





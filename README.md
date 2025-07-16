# :octocat: Setup GitHub Actions Bot

This Action configures `git` so that when you make commits in CI, they will be authored by [`github-actions[bot]`](https://github.com/features/actions) ([github-actions[bot]@users.noreply.github.com](mailto:github-actions[bot]@users.noreply.github.com))

## Usage

Here's a basic example of how to use this action in your workflow:

```yaml
name: Example Workflow

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3

      - name: Configure Git
        uses: cli-stuff/setup-github-actions-bot

      - name: Commit changes
        run: |
          echo "New content" >> new_file.txt
          git commit -am "Add new file"
```

## License

This project is licensed under Unlicense - see the [LICENSE](LICENSE) file for details.

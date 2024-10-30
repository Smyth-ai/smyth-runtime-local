<p align="center">
  <img width="auto" src="smythos.svg" alt="Header">
</p>

# Smyth Runtime Local

Smyth Runtime Local is a local version of the Smyth Runtime. You can use the executable to run, test and develop Smyth agents locally.

### Getting Started

To get started, clone the repository, copy the vault template and add your API keys to the vault.json file. The use the binary for your platform to run the agent.

```
git clone git@github.com:Smyth-ai/smyth-runtime-local.git
cp vault.json.example vault.json          # add API keys to vault.json

./bin/smyth-runtime-macos \
 --agent=agents/llm.smyth \
 --vault=vault.json \
 --method=POST \
 --path="/api/ask" \
 --body='{"question": "What is the capital of France?"}'
```

<p align="center">
  <img width="auto" width="500" src="./ReadMe.gif">
</p>

### CLI Arguments

| Argument             | Description                               |
| -------------------- | ----------------------------------------- |
| `--agent <file>`     | Path to `.smyth` agent file               |
| `--vault <file>`     | Path to the vault file                    |
| `--vault-key <file>` | Path to the pem file to decrypt `--vault` |
| `--get [params...]`  | Make a GET call                           |
| `--post [params...]` | Make a POST call                          |
| `--endpoint <name>`  | Endpoint name                             |
| `-v, --version`      | Display version information               |
| `-d, --debug`        | Dump all args to the console              |
| `--help, -h`         | Show help message                         |

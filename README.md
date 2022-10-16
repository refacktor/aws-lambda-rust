# No fluff, no fuss SAM-based AWS Lambda Rust hello-world example.

This was made by combining the instructions from two different sources:
- https://robertohuertas.com/2018/12/02/aws-lambda-rust/
- https://aws.amazon.com/blogs/opensource/rust-runtime-for-aws-lambda/


# Install

```
# AWS SAM
wget https://github.com/aws/aws-sam-cli/releases/latest/download/aws-sam-cli-linux-x86_64.zip
unzip aws-sam-cli-linux-x86_64.zip -d sam-installation
sudo ./sam-installation/install

# Rust Compiler
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
. $HOME/.cargo/env
rustup target add x86_64-unknown-linux-musl
```

# Build

`sam build`

# Test

`sam local start-api`

`curl -d {} http://127.0.0.1:3000/?firstName=TEST`

# Deploy

`sam deploy --guided`
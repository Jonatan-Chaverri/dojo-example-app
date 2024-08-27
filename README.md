# Dojo Starter example

This is an unofficial Dojo Starter Guide, designed to help you quickly set up your provable game in Dojo. This guide will assist you with the initial setup.

Read the full official tutorial [here](https://book.dojoengine.org/tutorial/dojo-starter).

## Pre requisites

- NodeJS
- Install dojo

```bash
curl -L https://install.dojoengine.org | bash
dojoup -v 0.7.4
```

## Running Locally

### Contracts

##### Terminal one (Make sure this is running)
```bash
# Run Katana
katana --disable-fee --allowed-origins "*"
```

##### Terminal two
```bash
cd contracts

# Build the example
sozo build

# Migrate the example
sozo migrate apply

# Authorize actions system to access your models
./scripts/default_auth.sh

# Start Torii
torii --world 0xb4079627ebab1cd3cf9fd075dda1ad2454a7a448bf659591f259efa2519b18 --allowed-origins "*"
```

### Client (React app)

On another terminal
```bash
cd client

# Install dependencies
pnpm i

# Run the project
pnpm run dev
```

Happy coding!

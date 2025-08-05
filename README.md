# forge script gas report

Creates a gas report from the `run-*.json` result of `forge script --broadcast`.

### Why not use `forge snapshot`

Measuring gas is important for optimizing smart contracts.
`forge snapshot` meters the gas in an EVM simulator (`anvil`).
Other EVMs such as FEVM may have substantially different gas metering.
Without `--evm_version` support, a simple workaround is to run `forge script --broadcast` into a local RPC.

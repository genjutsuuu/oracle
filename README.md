# Mina zkApp: Oracle

This template uses TypeScript.

## How to build

```sh
npm run build
```

## How to run tests

```sh
npm run test
npm run testw # watch mode
```

## How to run coverage

```sh
npm run coverage
```

## License

[Apache-2.0](LICENSE)




############################################################### STRIDE ###############################################################
[[chains]]
id = 'stride-1'
rpc_addr = 'https://stride.rpc.kjnodes.com/'
grpc_addr = 'https://stride.grpc.kjnodes.com/'
websocket_addr = 'wss://stride.rpc.kjnodes.com/websocket'

rpc_timeout = '30s'
account_prefix = 'stride'
key_name = 'ibc-stride'
store_prefix = 'ibc'
address_type = { derivation = 'cosmos' }
default_gas = 100000
max_gas = 1000000
gas_price = { price = 0.000, denom = 'ustrd' }
gas_multiplier = 1.2
max_msg_num = 30
max_tx_size = 800000
clock_drift = '5s'
max_block_time = '30s'
trusting_period = '7days'
memo_prefix = 'Relayed by SPT-ALRIZKI'
trust_threshold = { numerator = '1', denominator = '3' }

[chains.packet_filter]
policy = 'allow'
list = [
  ['transfer', 'channel-54'], # Stride
  ['transfer', 'channel-8'], # Planq

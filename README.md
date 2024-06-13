# MyFirstContract

## Overview

`MyFirstContract` is a basic contract on Ethereum network that administrates a simple token called ‘Pokemon Pikachu’ with the symbol ‘PP’. This contract also has provisions for the creation and destruction of tokens and has balance fields for each network address.
## Contract Details

### State Variables

- `tokenName`: The name of the token, that is "Pokemon Pikachu".
- `tokenAbbr`: The abbreviation of the token, which is "PP".
- `totalSupply`: The total supply of tokens, initially set to 213.

### Mappings

- `balances`: A mapping from addresses to their respective token balances.

### Functions

#### `mint(address addr, uint amount)`

This function mints new tokens and assigns them to a specified address.

- **Parameters**:
  - `addr`: The address to which the newly minted tokens will be assigned.
  - `amount`: The number of tokens to be minted.
- **Behavior**:
  - Increases the balance of `addr` by `amount`.
  - Increases the `totalSupply` by `amount`.

#### `burn(address addr, uint amount)`

This function burns tokens from a specified address.

- **Parameters**:
  - `addr`: The address from which tokens will be burned.
  - `amount`: The number of tokens to be burned.
- **Behavior**:
  - Decreases the balance of `addr` by `amount` if `addr` has enough tokens and if `totalSupply` is greater than `amount`.
  - Decreases the `totalSupply` by `amount`.

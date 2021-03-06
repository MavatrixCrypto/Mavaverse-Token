## Mavaverse token contract

This contract implements token reflection functions as well as a locked pool for Mavatrix NFT token holders. There are also 12 constant and preassigned timed-lock stages. Only the contract's owner can add addresses to this lock stages, thus inhibits the `approve` as well as the `transfer` functionalities for these locked accounts. After listing these addresses, the owner will **finalize** the lock, so it won't be possible anymore to call it. Finally a liquidity pool will be created on PancakeSwap.

- Core: 
    - Reflection Rewards - 3% tokens distributed to token holders;
- Extensions: 
    - NFT holders reward keeper - The other 3% will be redistributed to Mavatrix NFT owners;
    - Lock Stages - There are 12 different lock stages that'll inhibit `_transfer()` and `_approve()` functions;

The `rewardKeeper` smart contract will be responsible for accepting and validating incoming withdrawal requests (issued from proper client software);

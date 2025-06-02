# Timelock Claimable Balance Contract 🚀

![ChatGPT Image 2 Haz 2025 20_33_29](https://github.com/user-attachments/assets/21ef970e-f7a9-4305-9ef8-bbaa2919b4ae)


A simple and functional smart contract implementation for the **Soroban** platform (Stellar Testnet) that demonstrates the **timelock** concept and provides a streamlined **Claimable Balance** mechanism.

---

## 🌟 Overview

This contract allows users to deposit a specified amount of tokens and enables other accounts to claim them **before or after a specific time point**.  
It implements a basic timelock mechanism while maintaining a clean and efficient design.

✅ Deposit tokens with **time conditions**  
✅ Set multiple claimant addresses (up to 10)  
✅ Supports `Before` and `After` time bounds  
✅ Secure authorization checks  
✅ One-time initialization

---

## 🔗 Deployed Contract

- **Stellar Testnet Contract ID:*CADBLAOALS53GHUI6R56JNIAT3Z3CGA65VIE7AX632ODNXEDMTOW3NJX*  

- **View on Stellar Expert:**  
[View Contract on Stellar Expert](https://stellar.expert/explorer/testnet/contract/CADBLAOALS53GHUI6R56JNIAT3Z3CGA65VIE7AX632ODNXEDMTOW3NJX)

---

## ⚙️ Features

- **Deposit tokens** with specified time conditions  
- **Set multiple claimant addresses** (up to 10)  
- Two types of **time bounds**:
- `Before`: Claimable only before a specified timestamp  
- `After`: Claimable only after a specified timestamp  
- **Secure authorization checks** to ensure only valid claimants can withdraw  
- **Simple one-time initialization** for the contract

---

## 🛠️ Contract Structure

### 🔹 Data Structures

- **DataKey**: Defines storage keys used in the contract  
- `Init`: Marks the contract as initialized  
- `Balance`: Stores claimable balance information

- **TimeBoundKind**: Specifies the type of time constraint  
- `Before`: Claimable before the timestamp  
- `After`: Claimable after the timestamp

- **TimeBound**: Combines the time bound type and its timestamp  
- `kind`: The type of time bound (`Before` or `After`)  
- `timestamp`: The specific timestamp value

- **ClaimableBalance**: Stores all details of the claimable balance  
- `token`: Address of the token  
- `amount`: Token amount  
- `claimants`: List of addresses that can claim the balance  
- `time_bound`: Time condition for claiming

---

## 🚀 Deployment & Usage

### 🔧 Build the Contract
```bash
soroban contract build
```

## 🌐 Deploy to Stellar Testnet
```
stellar network use testnet

stellar contract deploy \
  --wasm target/wasm32-unknown-unknown/release/soroban_timelock.wasm \
  --source alice \
  --network testnet
```

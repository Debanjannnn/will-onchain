
# 🧾 Will Smart Contract – Decentralized Digital Inheritance on Aptos

A **Move-based smart contract** that enables users to create, manage, and claim digital wills on the **Aptos blockchain**.
This contract ensures that digital assets are securely transferred to a chosen recipient if the owner becomes inactive for a specified duration.
Here’s a clean, beginner-friendly **README.md** for your Aptos smart contract 👇
![Uploading image.png…]()

---

# 🧾 Will Smart Contract – Decentralized Digital Inheritance on Aptos

A **Move-based smart contract** that enables users to create, manage, and claim digital wills on the **Aptos blockchain**.
This contract ensures that digital assets are securely transferred to a chosen recipient if the owner becomes inactive for a specified duration.

---

## 🔗 Deployed Contract

**Transaction Link:**
[View on Aptos Explorer →](https://explorer.aptoslabs.com/txn/0x95d8e604002c08c1a5d7724106f9ac6c672ae505b6bbe73d5b9d79a39f20cfc7?network=testnet)

---

## 📜 Overview

This smart contract implements a **decentralized will registry** that:

* Lets users **lock Aptos Coins (APT)** for a recipient.
* Allows recipients to **claim funds** after a timeout period if the owner doesn’t “ping” to confirm activity.
* Maintains a **global registry** mapping recipients to multiple will creators.

It ensures a **trustless inheritance process** — no third party, no intermediaries.

---

## ⚙️ Features

✅ **Create a Will** – Define a recipient, lock funds, and set a timeout period.
✅ **Ping System** – Owners can update activity to reset their timer.
✅ **Auto-Claim Logic** – Recipients can claim assets once the timeout expires.
✅ **Global Will Registry** – Tracks multiple wills per recipient.
✅ **View Functions** – Retrieve wills, claimable wills, and counts easily.

---

## 🧠 Smart Contract Functions

| Function                            | Description                                             |
| ----------------------------------- | ------------------------------------------------------- |
| `initialize_global_registry`        | Deploy the global registry once.                        |
| `initialize`                        | Initialize your personal will state.                    |
| `create_will`                       | Create a will and lock AptosCoins for a recipient.      |
| `ping`                              | Reset your last active time to prevent auto-claim.      |
| `claim`                             | Recipient claims will if owner inactive beyond timeout. |
| `claim_single`                      | Claim the first available will for a recipient.         |
| `get_will`                          | View a specific owner’s will.                           |
| `get_wills_for_recipient`           | View all wills assigned to a recipient.                 |
| `get_claimable_wills_for_recipient` | View wills that are currently claimable.                |
| `get_will_count_for_recipient`      | Get the total number of wills linked to a recipient.    |

---

## 🧩 Constants

| Constant                       | Description                                  | Default |
| ------------------------------ | -------------------------------------------- | ------- |
| `DEFAULT_TIMEOUT`              | Time before recipient can claim (in seconds) | 10s     |
| `ERR_ALREADY_EXISTS`           | Will or registry already exists              | 1       |
| `ERR_NOT_FOUND`                | Will or record not found                     | 2       |
| `ERR_TOO_SOON`                 | Attempted to claim before timeout            | 3       |
| `ERR_NOT_RECIPIENT`            | Invalid claimant                             | 4       |
| `ERR_REGISTRY_NOT_INITIALIZED` | Registry not set up yet                      | 5       |

---

## 🧰 Tech Stack

* **Language:** Move
* **Network:** Aptos Testnet
* **Coin Type:** AptosCoin (`0x1::aptos_coin::AptosCoin`)

---

## 🚀 How to Use

1. **Deploy the contract** on Aptos testnet.
2. Call `initialize_global_registry()` (only once).
3. Each user runs `initialize()` to create their WillState.
4. Use `create_will()` to set up a new will with amount and recipient.
5. Regularly call `ping()` to stay active.
6. Recipient calls `claim()` or `claim_single()` when the timeout passes.

---

## 🧾 License

This project is open-source and available under the **MIT License**.

---

Would you like me to format it in **GitHub-styled markdown** (with icons, headings, and syntax highlighting) or keep it clean and plain like above?

---

## 🔗 Deployed Contract

**Transaction Link:**
[View on Aptos Explorer →](https://explorer.aptoslabs.com/txn/0x95d8e604002c08c1a5d7724106f9ac6c672ae505b6bbe73d5b9d79a39f20cfc7?network=testnet)

---

## 📜 Overview

This smart contract implements a **decentralized will registry** that:

* Lets users **lock Aptos Coins (APT)** for a recipient.
* Allows recipients to **claim funds** after a timeout period if the owner doesn’t “ping” to confirm activity.
* Maintains a **global registry** mapping recipients to multiple will creators.

It ensures a **trustless inheritance process** — no third party, no intermediaries.

---

## ⚙️ Features

✅ **Create a Will** – Define a recipient, lock funds, and set a timeout period.
✅ **Ping System** – Owners can update activity to reset their timer.
✅ **Auto-Claim Logic** – Recipients can claim assets once the timeout expires.
✅ **Global Will Registry** – Tracks multiple wills per recipient.
✅ **View Functions** – Retrieve wills, claimable wills, and counts easily.

---

## 🧠 Smart Contract Functions

| Function                            | Description                                             |
| ----------------------------------- | ------------------------------------------------------- |
| `initialize_global_registry`        | Deploy the global registry once.                        |
| `initialize`                        | Initialize your personal will state.                    |
| `create_will`                       | Create a will and lock AptosCoins for a recipient.      |
| `ping`                              | Reset your last active time to prevent auto-claim.      |
| `claim`                             | Recipient claims will if owner inactive beyond timeout. |
| `claim_single`                      | Claim the first available will for a recipient.         |
| `get_will`                          | View a specific owner’s will.                           |
| `get_wills_for_recipient`           | View all wills assigned to a recipient.                 |
| `get_claimable_wills_for_recipient` | View wills that are currently claimable.                |
| `get_will_count_for_recipient`      | Get the total number of wills linked to a recipient.    |

---

## 🧩 Constants

| Constant                       | Description                                  | Default |
| ------------------------------ | -------------------------------------------- | ------- |
| `DEFAULT_TIMEOUT`              | Time before recipient can claim (in seconds) | 10s     |
| `ERR_ALREADY_EXISTS`           | Will or registry already exists              | 1       |
| `ERR_NOT_FOUND`                | Will or record not found                     | 2       |
| `ERR_TOO_SOON`                 | Attempted to claim before timeout            | 3       |
| `ERR_NOT_RECIPIENT`            | Invalid claimant                             | 4       |
| `ERR_REGISTRY_NOT_INITIALIZED` | Registry not set up yet                      | 5       |

---

## 🧰 Tech Stack

* **Language:** Move
* **Network:** Aptos Testnet
* **Coin Type:** AptosCoin (`0x1::aptos_coin::AptosCoin`)

---

## 🚀 How to Use

1. **Deploy the contract** on Aptos testnet.
2. Call `initialize_global_registry()` (only once).
3. Each user runs `initialize()` to create their WillState.
4. Use `create_will()` to set up a new will with amount and recipient.
5. Regularly call `ping()` to stay active.
6. Recipient calls `claim()` or `claim_single()` when the timeout passes.

---

## 🧾 License

This project is open-source and available under the **MIT License**.

---



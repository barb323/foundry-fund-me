# Foundry Fund Me 🚀

A decentralized crowdfunding smart contract application built using the **Foundry** development framework. This project allows users to fund the contract with ETH, keeps track of funders, and ensures only the contract owner can withdraw the funds.

## 🛠 Prerequisites

Before you begin, ensure you have the following installed on your machine:
- [Git](https://git-scm.com/)
- [Foundry](https://book.getfoundry.sh/getting-started/installation) (Make sure `forge`, `cast`, and `anvil` are available in your terminal)
- [Visual Studio Code](https://code.visualstudio.com/) (or your preferred code editor)
- > 💡 **Windows Users:** It is highly recommended to use **WSL (Windows Subsystem for Linux)** for a smoother development experience with Foundry.

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/barb323/foundry-fund-me.git
cd foundry-fund-me
```
Open the project in Visual Studio Code:
```bash
code .
```
### 2. Build the Project
Compile the smart contracts to ensure everything is set up correctly:
```bash
forge build
```
### 3. Running Tests
```bash
forge test
```
To see console logs or a detailed trace of execution, increase the verbosity:

```bash
forge test -vvv
```
To check your test coverage:
```bash
forge coverage
```
### 4. Local Deployment
You can spin up a local Ethereum node using Anvil:
```bash
anvil
```
In a new terminal window, deploy your contract to the local network:
Before deploying, create a file named .env in the root directory
Add the following variables
RPC_URL=anvilRpcUrl
PRIVATE_KEY=anvilprivateKey

Load your environment variables and execute the deployment script:
```bash
source .env
forge script script/DeployFundMe.s.sol --rpc-url $RPC_URL --private-key $PRIVATE_KEY --broadcast 
```
### 5.Interactions
Once deployed, you can interact with the contract (e.g., funding it) using the interactions script:
```bash
forge script script/Interactions.s.sol:FundFundMe --rpc-url $RPC_URL --private-key $PRIVATE_KEY --broadcast
'''
## License
This project is licensed under the MIT License.




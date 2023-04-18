# FundChain
FundChain is a decentralized crowdfunding platform built on the Ethereum blockchain. 


# Description:  										 #


FundChain is a decentralized crowdfunding platform built on the Ethereum blockchain. It allows individuals and organizations to create campaigns and raise funds for their projects in a transparent and trustless manner. The platform utilizes smart contracts to manage the funding process, ensuring that funds are only released to the project creator when the funding goal is met.


# How it Works:											 #

To create a campaign on FundChain, users must first connect their MetaMask wallet to the platform. Once connected, users can create a new campaign by specifying the project details, funding goal, and deadline. After the campaign is created, users can contribute to it using cryptocurrencies such as Ethereum, Bitcoin, or other ERC20 tokens.

The smart contract behind FundChain manages the funds and ensures that they are only released to the project creator when the funding goal is met before the deadline. If the funding goal is not met before the deadline, the smart contract automatically refunds all contributions to the respective contributors.

Users can browse and search for existing campaigns on the platform and view their funding progress. The platform also allows project creators to provide updates on their campaigns and communicate with contributors.

FundChain provides a transparent and secure way for individuals and organizations to raise funds for their projects without relying on traditional centralized crowdfunding platforms. With its user-friendly interface and support for web3 wallets such as MetaMask, FundChain makes it easy for anyone to create and contribute to campaigns on the blockchain.




# LEVELS											     #

- Level 1:
		Create a figma board with a website design
- Level 2:
		Create and deploy website to EditorX or (better!) as a React.js app to Vercel
- Level 3 (BONUS):
		Develop and deploy smart-contract(s?) for the platform
- Level 4 (INSANE LEVEL BONUS):
		Connect smart-contracts to your React.js app and integrate Metamask — the outcome must be a fully-functional web3 dApp




# REQUIREMENTS 											 #

# MANDATORY:

Design:
	- Use Midjourney to generate designs
	- Use Photoshop to process the outcomes
	- Use Figma to translate Midjourney designs into interface prototypes
	- Use ChatGPT to generate content

Website interface development:
	- To convert designs from Figma to web:
		- Use Editor X (constructor) plugin (https://www.figma.com/community/plugin/987294632651817123)
			OR BETTER
		- Use TeleportHQ plugin (figma to react) (https://www.figma.com/community/plugin/992726161890204477/TeleportHQ---Figma-to-Code---Export-HTML%2C-CSS%2C-React-%26-Vue)
		- If you have a better method — feel free, but it must be as fast as possible

OUTCOME:
	- A Figma board with design prototype and a website, deployed to either EditorX or Vercel
	- If choosing the cool path (react app), you must provide a link to a Vercel deploy instance of your website and a GitHub website project repository
	- The interface must be as functional as possible



# BONUS:

Smart contracts and dApp development:
	- Use Solidity for smart-contract development
	- Use RemixIDE, OR BETTER, HardHat as your development and deploy environment
	- Use ethers.js for web3 integration into website code
	- Contracts must be deployed to Goerli Network
	- Platform must support MetaMask
	- DO NOT WRITE CODE — use ChatGPT

	- VSCode is a great and free IDE
	- Here's a ChatGPT plugin for VSCode
			https://marketplace.visualstudio.com/items?itemName=DanielSanMedium.dscodegpt
	- Here's a Remix plugin for VSCode
			https://marketplace.visualstudio.com/items?itemName=RemixProject.ethereum-remix

OUTCOME:
	- EXTRA LEVEL:
		- Solidity smart-contracts, deployed to Goerli testnet blockchain, they must be verified
			- You must provide a link to your contracts at goerli.etherscan explorer
	- INSANE LEVEL:
		- Smart-contracts must be connected to your website — your website must be a fully functional web3 dApp that interacts with those contracts on-chain
		- Your website must support MetaMask wallet
		- Smart-contract accepts mock-USDT ERC20 tokens as payment (use OpenZeppelin Wizard to get ERC20 contract or ask ChatGPT)






# BRIEF     											 #

Part 1: Design
Project Name: FundChain

Design Concept: The website should have a modern, clean design with a focus on simplicity and ease of use. The color scheme should be predominantly blue, with accents of green and white. The site should be mobile responsive and compatible with popular web3 wallet MetaMask.


Sections and Elements:

    - Homepage: A simple landing page with a brief introduction to the platform, featured campaigns, and a call to action to create a campaign or contribute to an existing one.

    - Campaign Creation: A form where users can create a new campaign by specifying the project details, funding goal, and deadline.

    - Campaign Listing: A page where users can browse and search for existing campaigns. Each campaign should have a summary of the project, funding progress, and deadline.

    - Campaign Details: A page with detailed information about a specific campaign, including updates from the project creator and a list of contributors.
    
    - MetaMask Integration: A section on the site where users can connect their MetaMask wallet (a header button is enough, search for references).




Part 2: Development
Smart Contract Development Brief:

The smart contract for FundChain will be used to manage crowdfunding campaigns. The contract will accept ERC-20 token as payment. The contract will be deployed on the Goerli blockchain.


Requirements:

    - The contract must be able to create new campaigns with a specified funding goal and deadline (create a mapping of campaign id to campaign struct, inside the struct you will store campaign name, description, deadline, funding goal and current progres. use unix timestamp for deadlines).

    - The contract must be able to accept contributions from users and track the total amount raised for each campaign (in mock USDT, use interfaces).

    - Once a campaign reaches its funding goal before the deadline, the contract must release the funds to the project creator (contracts can't call themselves and check this will be a function modifier).

    - If a campaign does not reach its funding goal before the deadline, the contract must refund all contributions to the respective contributors (also a modifier).

    - The contract must be able to display the list of campaigns and their funding progress (a view getter function).

    - If the campaign was successful, the contract must deduct 5% from the raised funds as a fee, FundChain owner must be able to withdraw these funds from contract balance


Functions:

    - createCampaign(): A function to create a new campaign with the specified details and funding goal.

    - contribute(): A function to allow users to contribute to a specific campaign.

    - getBalance(): A function to get the current balance of the contract.

    - getCampaigns(): A function to get the list of all campaigns and their funding progress.

    - refund(): A function to refund all contributions for a specific campaign if the funding goal is not met before the deadline.

    - claimCampaignFund(): A function for campaign creator to withdraw raised funds, if the campaign was successful.

    - claimTreasury(): A function for FundChain owner to withdraw the revenue from fees.









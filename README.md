# ERC20 Token
## 1. Goal ##
This is the smart contract support ERC20 token transaction and satisifies the following functions.
  
 1-1. Clients can transact their ERC20 token with each other.  
 1-2. Client can exchange NTD with ERC20 token. 
 ## 2. Role ## 
  2-1. Client.  
  2-2. Maintainer.
 ## 3. Function ##
 List the client's function can be called by client to fulfill the command client request.  
 And list the maintainer's function can be called by maintainer to maintain the system. 
  ### 3-1. Client's Function. ###    
     3-1-1. Transfer: transact token with other client.  
     3-1-2. Buy: exchange NTC with token.  
     3-1-3. Balanceof: return the balance of client's token.  
  ### 3-2. Maintainer's Function. ###
   #### 3-2-1. Mint & Burn. ####
    3-2-1-1. Mint: mint the token to specific account with given amount.
    3-2-1-2. Burn: burn the token by specific account with given amount.
    3-2.1-3. Burn All: burn all token of specific account.
   #### 3-2-2. Manage Maintainer's Role. ####
    3-2-2-1. Maintanier_Is: check specific account is maintainer or not.
    3-2-2-2. Maintainer_Add: change the role of specific account from client to maintainer.
    3-2-2-3. Maintainer_Del: change the role of specific account from manitainer to client.
    3-2-2-4. Maintainer_List: list all maintanier accounts. 
   #### 3-2-3. Manage the black list. ####
   Some account may send malicious request.  
   Reserve the power for maintainer to forbid the malicious account to make transactions.  
     
    3-2-3.1. R_Black: restrict specific account from calling function of contract.
    3-2-3-2. R_BlackUN: relieve the restrcition of specific account from calling function of contract.
    3-2-3-3. R_Black_List: list all accounts under the restriction from calling function of contract.
   #### 3-2-4. Halt the contract. ####
   Contract may sufferred from improper operation should be halted immediately.  
   Design this function to solve this situation.  
   Also design the function to relieve the halt.  
     
    3-2-4-1. R_Stop: Halt all operation of contract except R_StopUN.  
    3-2-4-2. R_StopUN: relieve the halt of all operation of contract.
   
   

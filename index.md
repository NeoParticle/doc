# Neo Particle {NEOP}
### Generic Smart Contract which can be utilized to build Smart Contract!!!
** NEP Tokens are just used to pay for the promised service **
** When moving to Mainnet admin account will be removed and users can convert from NEO to NEP and NEP to NEO **
---
**Direction of Use:**
```
[AppCall("0xb693f49e295e3b72db4fe2f589756b9527266b3f")] // ScriptHash
public static extern int AnotherContract (byte[] activityType, params object[] args);

public static void Main ()
{
      //To check total Supply
     AnotherContract ((byte[])"totalSupply");
}
```
**NEP5 Token Methods:**

* *deploy*
  This method is invoked first time by Admin.
  
* *mintTokens* 
  Any one can transfer NEO to the contract address and invoke this method to generate NEP TOKENS.
  
* *totalSupply* 
  Will provide the total amount of tokens minted.
  
* *name* 
  Will provide the Name of the Token (NEO Particle).
  
* *symbol* 
  Will provide the symbol of the Token (NEP).
  
* *transfer* 
  Used to transfer NEP token's from one account another.
      Parameter(byte[] fromScriptHash, byte[] toScriptHash, BigInteger value).
        byte[] fromScriptHash => Logged in user account contract script hash.
        byte[] toScriptHash => Contract script hash of the account to which tokens has to be transferred.
        BigInteger value => Number of tokens to be transferred, upto 8 decimals accepted.
        
* *balanceOf*
  To know the balance of the logged in account.
      Parameter(byte[] scriptHash)
        byte[] scriptHash => Logged in user account contract script hash.
        
* *decimals*
  Will provide the total decimal for the Token (8).
  
* *transferFrom*
  This allows user to transfer tokens from another account. Before using this option the user from whose account the token are going to be transferred has to approve the logged in user to transfer certain amount of token from his account. ("approve" method is used for this purpose)
      Parameter(byte[] originatorScriptHash, byte[] fromScriptHash, byte[] toScriptHash, BigInteger value)
        byte[] originatorScriptHash => Logged in user account contract script hash, account used for doing the transfer between two users.
        byte[] fromScriptHash => Script hash of the account from which the tokens are going to be transferred.
        byte[] toScriptHash => Script hash of the account to which the tokens are being transferred.
        BigInteger value => Numbet of tokens being transferred.
        
* *approve*
  This method is used to set or allow another user to access the logged in users troken. Setting permission to transfer.
      Parameter(byte[] originatorScriptHash, byte[] toScriptHash, byte[] value)
        byte[] originatorScriptHash => Script hash of the logged in account, who is going to allow access to another user to transfer token from his account.
        byte[] toScriptHash => Script hash of the account for whom the permission to transfer is set.
        byte[] value => Total number of tokens which can be transferred from the logged in user account.
        
* *allowance*
  This method is used to check the amount allowed to transfer from another account.
      Parameter(byte[] fromScriptHash, byte[] toScriptHash)
        byte[] fromScriptHash => Script hash of the account who has allowed the logged in user to transfer from his account.
        byte[] toScriptHash => Script hash of the logged in account, who wish check the balance of the allowed amount.
---

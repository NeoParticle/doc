# Neo Particle [NEP]
### Generic Smart Contract which can be utilized to build Smart Contract!!!
#### NEP Tokens are just used to pay for the promised service
>**Note:**  When moving to Mainnet admin account will be removed and users can convert from NEO to NEP and NEP to NEO 
---
**Direction of Use:**

	

	    [AppCall("0xb693f49e295e3b72db4fe2f589756b9527266b3f")] // ScriptHash
    	public static extern int AnotherContract (byte[] activityType, params object[] args);
    
    	public static void Main ()
    	{
    	      //To check total Supply
    	     AnotherContract ((byte[])"totalSupply");
    	}

**NEP5 Token Methods:**<br /><br />

>**deploy**<br />
  &nbsp;This method is invoked first time by Admin.<br /><br />
  
>**mintTokens** <br />
  &nbsp;Any one can transfer NEO to the contract address and invoke this method to generate NEP TOKENS.<br />
  
>**totalSupply** <br />
  &nbsp;Will provide the total amount of tokens minted.<br />
  
>**name** <br />
  &nbsp;Will provide the Name of the Token (NEO Particle).<br /><br />
  
>**symbol** <br />
  &nbsp;Will provide the symbol of the Token (NEP).<br /><br />
  
>**transfer** <br />
Used to transfer NEP token's from one account another.<br />
*Parameter*(`byte[] fromScriptHash, byte[] toScriptHash, BigInteger value`).<br />
&nbsp;&nbsp;&nbsp;`byte[] fromScriptHash` => Logged in user account contract script hash.<br />
        &nbsp;&nbsp;&nbsp;`byte[] toScriptHash` => Contract script hash of the account to which tokens has to be transferred.<br />
        &nbsp;&nbsp;&nbsp;`BigInteger value` => Number of tokens to be transferred, upto 8 decimals accepted.<br /><br />
        
>**balanceOf**<br />
  To know the balance of the logged in account.<br />
*Parameter*(`byte[] scriptHash`)<br />
        &nbsp;&nbsp;&nbsp;`byte[] scriptHash` => Logged in user account contract script hash.<br /><br />
        
>**decimals**<br />
  Will provide the total decimal for the Token (8).<br /><br />
  
>**transferFrom**<br />
  &nbsp;*This allows user to transfer tokens from another account. Before using this option the user from whose account the token are going to be transferred has to approve the logged in user to transfer certain amount of token from his account. ("approve" method is used for this purpose)<br />
*Parameter*(`byte[] originatorScriptHash, byte[] fromScriptHash, byte[] toScriptHash, BigInteger value`)<br />
        &nbsp;&nbsp;&nbsp;`byte[] originatorScriptHash` => Logged in user account contract script hash, account used for doing the transfer between two users.<br />
        &nbsp;&nbsp;&nbsp;`byte[] fromScriptHash` => Script hash of the account from which the tokens are going to be transferred.<br />
        &nbsp;&nbsp;&nbsp;`byte[] toScriptHash` => Script hash of the account to which the tokens are being transferred.<br />
        &nbsp;&nbsp;&nbsp;`BigInteger value` => Numbet of tokens being transferred.<br /><br />
        
>**approve**<br />
This method is used to set or allow another user to access the logged in users troken. Setting permission to transfer.<br />
*Parameter*(`byte[] originatorScriptHash, byte[] toScriptHash, byte[] value`)<br />
        &nbsp;&nbsp;&nbsp;`byte[] originatorScriptHash` => Script hash of the logged in account, who is going to allow access to another user to transfer token from his account.<br />
        &nbsp;&nbsp;&nbsp;`byte[] toScriptHash` => Script hash of the account for whom the permission to transfer is set.<br />
        &nbsp;&nbsp;&nbsp;`byte[] value` => Total number of tokens which can be transferred from the logged in user account.<br /><br />
        
>**allowance**<br />
This method is used to check the amount allowed to transfer from another account.<br />
*Parameter*(`byte[] fromScriptHash, byte[] toScriptHash`)<br />
        &nbsp;&nbsp;&nbsp;`byte[] fromScriptHash` => Script hash of the account who has allowed the logged in user to transfer from his account.<br />
        &nbsp;&nbsp;&nbsp;`byte[] toScriptHash` => Script hash of the logged in account, who wish check the balance of the allowed amount.<br />
---

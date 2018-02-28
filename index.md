# NEP #

**[EF Methods](http://docs.neoparticle.com/EF.html)**<br /><br />

## Type Nep5Token

 NEP5 Token methods. 



---
#### Method Nep5Token.Name()

 Get the name of the token 

**Returns**: Will always be NEO Particle



---
#### Method Nep5Token.Symbol()

 Get the symbol of the token. 

**Returns**: Will always be NEP.



---
#### Method Decimals()

 Number of secimal places used for token 

**Returns**: Will always be 8



---
####       [DisplayName("transfer")]
#### EVENT public static event Action<byte[], byte[], BigInteger> Transferred;

 Event raised after a transaction is made. 



---
#### 	   [DisplayName("refund")]
#### EVENT public static event Action<byte[], BigInteger> Refund;

 Event raised after a refund transaction is made. 



---
#### Method totalSupply()

 Total token's minted and is in circulation 

**Returns**: Total number of tokens minted.



---
#### Method balanceOf(Byte[])

 Get available tokens in the logged in users account. 

|Name | Description |
|-----|------|
|yourSH: |Logged in user public key.|
**Returns**: Token balance available in your account.



---
#### Method transfer(Byte[], Byte[], BigInteger)

 Transfer token from one account to another. 

|Name | Description |
|-----|------|
|yourSH: |Script hash of the logged in user.|
|toSH: |Script hash of the user to whom token is being transferred.|
|value: |Number of tokens transferred.|
**Returns**: Success or failure



---
#### Method allowance(Byte[], Byte[])

 This method is used to check how much token can logged in user is allowed to transfer from another account. 

|Name | Description |
|-----|------|
|yourSH: |Logged in user script hash.|
|to: |Script hash of the account from which logged in is allowed to transfer tokens.|
**Returns**: Amount of token allowed by logged in user to transfer from another account.



---
#### Method transferFrom(Byte[], Byte[], Byte[], BigInteger)

 This method is used to transfer the allowed amount of token from another account. 

|Name | Description |
|-----|------|
|yourSH: |Logged in user script hash who is allowed to transfer token from another account.|
|fromSH: |Script hash of the account which has allowed the logged in user to transfer token.|
|toSH: |Script hash of the user to whom the tokens are being transferred.|
|value: ||
**Returns**: Success or failure



---
#### Method approve(Byte[], Byte[], BigInteger)

 Approve an account to transfer token from your account 

|Name | Description |
|-----|------|
|yourSH: |Logged in user script hash.|
|toSH: |Account script hash which is allowed to transfer from your account to any account.|
|value: |Number of tokens allowed to transfer.|
**Returns**: Success or failure



---



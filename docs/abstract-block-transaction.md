## Block
```json
{
	"ID": "string => hash of block (hash of previous hash + blocks' transactions + none)",
	"Previous": "string => ID (hash) of previous block",
	"Nonce": "number => none number of the block",
	"Height": "number => block height",
	"Target": "number => target of difficulty",
	"Transactions": [
		// array of transactions
	]
}
```
## Transaction
```json
{
	"Block": "number => block height",
	"Nonce": "number => none number of the traction",
	"Target": "number => target of difficulty",
	"Input": [
		{
			Block: "number => block height of UTXO (unspent transaction output)",
			ID: "string => ID (hash) of UTXO"
		}
	],
	"Output": [
		{
			"From": "string => public address",
			"To": "string => public address",
			"Amount": "number",
			"Script": "string => JS script",
			"Signature": "string => signature of the transaction"		
		}
	]
}
```

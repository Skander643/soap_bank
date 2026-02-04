LAB 2 – SOAP with Java (Spring-WS)

B) Reading the contract
1. Identify the XSD file and explain its role.
The XSD defines the contract of the SOAP service.
It specifies the structure of requests and responses.
The WSDL is generated from this XSD.
2. List the request/response elements (names, fields, types).
*GetAccount
- Request : 
GetAccountRequest
accountId : string
- Response : 
GetAccountResponse
account : AccountType

*Deposit
- Request :
DepositRequest
accountId : string
amount : decimal

- Response : 
DepositResponse
newBalance : decimal

*AccountType
AccountType
accountId : string
owner     : string
balance   : decimal
currency  : string


3. From the WSDL, locate:
• the namespace,
• the portType and operations,
• the endpoint (URL) and the SOAP binding.

*Namespace : 
targetNamespace="http://example.com/bank"


*PortType :
<wsdl:portType name="BankPort">

*Operations:
- GetAccount
- Deposit

*Endpoint URL : /​ws
*Full endpoint:
http://localhost:8080/ws

*Binding : 
SOAP over HTTP (document/literal style)


D) Add one feature

I choose the  Feature of Withdraw an amount

D.1 Update XSD 


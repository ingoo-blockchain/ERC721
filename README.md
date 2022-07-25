# NFT 

ERC-20 / Token fungible Token
ERC-721 / Token  Non-fungible Token

IngToken 1000개 있다. 1개 2개  수량
천원 1장이 2장이든 2장 2천원 

NFT -> 1000장 영화관 티켓? 100장
좌석 

Code? 구현하자면 어떤느낌으로 ? 

erc-20
mint(msg.sender, 100000) // 수량
0x1234

mapping(address => uint) public balances;
0x1234 => 2000 // 2000개 

erc-721
primary key 
mint(msg.sender,1) // 키값
mint(msg.sender,2)
mint(msg.sender,3)
mint(msg.sender,4)

mapping(address => uint) public balances;
0x1234 => 2000 // 총 2000개 토큰있다.
1~2000 고유한 키값을 가진 토큰이있어.
mapping(uint => address) public owned;
1 => 0x1234
2000 => 0x1234

영화관 무인발급기

NFT 어떤 이미지를 가지고있나요 ?

타이어 <- Image
원숭이 <- Image

key 1  image?
key 2  image?
key 3  image?

Smart Contract Image ? 안된다.

1 -> "http://localhost:3000/metadata/1.json" 
2 -> "http://localhost:3000/metadata/2.json"
3 -> "http://localhost:3000/metadata/3.json"


{
    name:"이건원숭이이미지",
    description:"이거 비싼거임",
    image:"http://localhost:3000/image/1.jpg",
    "atr..":
}

Dapp 

2번에 대한 NFT를 가져와줘.

2 -> json.
http://localhost:3000/metadata/1.json

const response = axios.post("http://localhost:3000/metadata/1.json")

const image = response.data.image

<img src="{image}" >

```
mkdir truffle
cd truffle
truffle init

npm install -g @remix-project/remixd
cd contracts

remixd -s . --remix-ide https://remix.ethereum.org
```

# NFT 
ERC20 -> 라이브러리 
라이브러리 먼저 만들어보고
직접구현 

```
cd truffle
npm init
npm install openzeppelin-solidity
```

../node_modules/openzeppelin-solidity/contracts/token/ERC721/extensions/ERC721Enumerable


```
class Minting extends ERC721 {
    constructor(_name:string, _symbol:string){
        super(_name,_symbol)
    }
}
```

ifps

https://eips.ethereum.org/EIPS/eip-721






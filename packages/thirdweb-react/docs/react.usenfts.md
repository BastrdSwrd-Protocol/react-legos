<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@thirdweb-dev/react](./react.md) &gt; [useNFTs](./react.usenfts.md)

## useNFTs() function

> This API is provided as a preview for developers and may change based on feedback that we receive. Do not use this API in a production environment.
> 

Use this to get a list of NFT tokens of your [NFTContract](./react.nftcontract.md)<!-- -->.

<b>Signature:</b>

```typescript
export declare function useNFTs<TContract extends NFTContract>(contract: RequiredParam<TContract>, queryParams?: QueryAllParams): import("@tanstack/react-query").UseQueryResult<NFT<TContract>[], unknown>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  contract | [RequiredParam](./react.requiredparam.md)<!-- -->&lt;TContract&gt; | an instance of a [NFTContract](./react.nftcontract.md) |
|  queryParams | QueryAllParams | <i>(Optional)</i> query params to pass to the query for the sake of pagination |

<b>Returns:</b>

import("@tanstack/react-query").UseQueryResult&lt;[NFT](./react.nft.md)<!-- -->&lt;TContract&gt;\[\], unknown&gt;

a response object that includes an array of NFTs

## Example 1


```javascript
const nftDrop = useNFTDrop(<ContractAddress>);
const { data: nfts, isLoading, error } = useNFTs(nftDrop, { start: 0, count: 100 });
```

## Example 2


```javascript
const { contract } = useContract(<ContractAddress>);
const { data: nfts, isLoading, error } = useNFTs(contract?.nft, { start: 0, count: 100 });
```

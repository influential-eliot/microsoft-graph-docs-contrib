---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


// Code snippets are only available for the latest major version. Current major version is $v0.*

// Dependencies
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphsites "github.com/microsoftgraph/msgraph-beta-sdk-go/sites"
	  //other-imports
)


requestToken := "1230919asd190410jlka"

requestParameters := &graphsites.SitesDelta()RequestBuilderGetQueryParameters{
	Token: &requestToken,
}
configuration := &graphsites.SitesDelta()RequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
delta, err := graphClient.Sites().Delta().GetAsDeltaGetResponse(context.Background(), configuration)


```
---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


// Code snippets are only available for the latest major version. Current major version is $v0.*

// Dependencies
import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  graphreports "github.com/microsoftgraph/msgraph-beta-sdk-go/reports"
	  //other-imports
)


requestFormat := "application/json"

requestParameters := &graphreports.ReportsGetM365AppPlatformUserCounts(period='{period}')RequestBuilderGetQueryParameters{
	Format: &requestFormat,
}
configuration := &graphreports.ReportsGetM365AppPlatformUserCounts(period='{period}')RequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}

// To initialize your graphClient, see https://learn.microsoft.com/en-us/graph/sdks/create-client?from=snippets&tabs=go
period := "{period}"
graphClient.Reports().GetM365AppPlatformUserCountsWithPeriod(&period).Get(context.Background(), configuration)


```
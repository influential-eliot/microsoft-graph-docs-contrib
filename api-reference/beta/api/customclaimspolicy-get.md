---
title: "Get customClaimsPolicy"
description: "Get the properties and relationships of a custom claims policy object."
author: "rahul-nagraj"
ms.localizationpriority: medium
ms.service: entra-id
doc_type: apiPageType
---

# Get customClaimsPolicy

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get the properties and relationships of a [customClaimsPolicy](../resources/customclaimspolicy.md) object.

[!INCLUDE [national-cloud-support](../../includes/global-only.md)]

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "customclaimspolicy_get" } -->
[!INCLUDE [permissions-table](../includes/permissions/customclaimspolicy-get-permissions.md)]

[!INCLUDE [rbac-customclaimspolicy-apis-read](../includes/rbac-for-apis/rbac-customclaimspolicy-apis-read.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /servicePrincipals/{servicePrincipalsId}/claimsPolicy
```

## Optional query parameters

This method supports some of the OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required. Learn more about [authentication and authorization](/graph/auth/auth-concepts).|

## Request body

Don't supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [customClaimsPolicy](../resources/customclaimspolicy.md) objects in the response body.

## Examples

### Request

The following example shows a request.
<!-- {
  "blockType": "request",
  "name": "list_customclaimspolicy"
}
-->
``` http
GET https://graph.microsoft.com/beta/servicePrincipals/{servicePrincipalsId}/claimsPolicy
```

### Response

The following example shows the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.customClaimsPolicy)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.customClaimsPolicy",
      "id": "f914f36d-167e-3fa7-cfa2-355cc5a36689",
      "includeBasicClaimSet": "Boolean",
      "includeApplicationIdInIssuer": "Boolean",
      "audienceOverride": "String",
      "claims": [
        {
          "@odata.type": "microsoft.graph.customClaim"
        }
      ]
    }
  ]
}
```

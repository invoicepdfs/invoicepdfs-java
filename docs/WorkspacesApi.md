# WorkspacesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createMemberApiV1WorkspacesWorkspaceIdMembersPost**](WorkspacesApi.md#createMemberApiV1WorkspacesWorkspaceIdMembersPost) | **POST** /api/v1/workspaces/{workspace_id}/members | Create Member |
| [**createWorkspaceApiV1WorkspacesPost**](WorkspacesApi.md#createWorkspaceApiV1WorkspacesPost) | **POST** /api/v1/workspaces | Create Workspace |
| [**deleteMemberApiV1WorkspacesWorkspaceIdMembersMemberIdDelete**](WorkspacesApi.md#deleteMemberApiV1WorkspacesWorkspaceIdMembersMemberIdDelete) | **DELETE** /api/v1/workspaces/{workspace_id}/members/{member_id} | Delete Member |
| [**deleteWorkspaceApiV1WorkspacesWorkspaceIdDelete**](WorkspacesApi.md#deleteWorkspaceApiV1WorkspacesWorkspaceIdDelete) | **DELETE** /api/v1/workspaces/{workspace_id} | Delete Workspace |
| [**getWorkspaceApiV1WorkspacesWorkspaceIdGet**](WorkspacesApi.md#getWorkspaceApiV1WorkspacesWorkspaceIdGet) | **GET** /api/v1/workspaces/{workspace_id} | Get Workspace |
| [**listMembersApiV1WorkspacesWorkspaceIdMembersGet**](WorkspacesApi.md#listMembersApiV1WorkspacesWorkspaceIdMembersGet) | **GET** /api/v1/workspaces/{workspace_id}/members | List Members |
| [**listWorkspacesApiV1WorkspacesGet**](WorkspacesApi.md#listWorkspacesApiV1WorkspacesGet) | **GET** /api/v1/workspaces | List Workspaces |
| [**patchMemberApiV1WorkspacesWorkspaceIdMembersMemberIdPatch**](WorkspacesApi.md#patchMemberApiV1WorkspacesWorkspaceIdMembersMemberIdPatch) | **PATCH** /api/v1/workspaces/{workspace_id}/members/{member_id} | Patch Member |
| [**patchWorkspaceApiV1WorkspacesWorkspaceIdPatch**](WorkspacesApi.md#patchWorkspaceApiV1WorkspacesWorkspaceIdPatch) | **PATCH** /api/v1/workspaces/{workspace_id} | Patch Workspace |


<a id="createMemberApiV1WorkspacesWorkspaceIdMembersPost"></a>
# **createMemberApiV1WorkspacesWorkspaceIdMembersPost**
> WorkspaceMembersListResponse createMemberApiV1WorkspacesWorkspaceIdMembersPost(workspaceId, workspaceMemberCreateRequest, idempotencyKey)

Create Member

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    String workspaceId = "workspaceId_example"; // String | 
    WorkspaceMemberCreateRequest workspaceMemberCreateRequest = new WorkspaceMemberCreateRequest(); // WorkspaceMemberCreateRequest | 
    String idempotencyKey = "idempotencyKey_example"; // String | 
    try {
      WorkspaceMembersListResponse result = apiInstance.createMemberApiV1WorkspacesWorkspaceIdMembersPost(workspaceId, workspaceMemberCreateRequest, idempotencyKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#createMemberApiV1WorkspacesWorkspaceIdMembersPost");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **workspaceId** | **String**|  | |
| **workspaceMemberCreateRequest** | [**WorkspaceMemberCreateRequest**](WorkspaceMemberCreateRequest.md)|  | |
| **idempotencyKey** | **String**|  | [optional] |

### Return type

[**WorkspaceMembersListResponse**](WorkspaceMembersListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="createWorkspaceApiV1WorkspacesPost"></a>
# **createWorkspaceApiV1WorkspacesPost**
> WorkspaceResponse createWorkspaceApiV1WorkspacesPost(workspaceCreateRequest, idempotencyKey)

Create Workspace

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    WorkspaceCreateRequest workspaceCreateRequest = new WorkspaceCreateRequest(); // WorkspaceCreateRequest | 
    String idempotencyKey = "idempotencyKey_example"; // String | 
    try {
      WorkspaceResponse result = apiInstance.createWorkspaceApiV1WorkspacesPost(workspaceCreateRequest, idempotencyKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#createWorkspaceApiV1WorkspacesPost");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **workspaceCreateRequest** | [**WorkspaceCreateRequest**](WorkspaceCreateRequest.md)|  | |
| **idempotencyKey** | **String**|  | [optional] |

### Return type

[**WorkspaceResponse**](WorkspaceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="deleteMemberApiV1WorkspacesWorkspaceIdMembersMemberIdDelete"></a>
# **deleteMemberApiV1WorkspacesWorkspaceIdMembersMemberIdDelete**
> SimpleBoolResponse deleteMemberApiV1WorkspacesWorkspaceIdMembersMemberIdDelete(workspaceId, memberId)

Delete Member

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    String workspaceId = "workspaceId_example"; // String | 
    String memberId = "memberId_example"; // String | 
    try {
      SimpleBoolResponse result = apiInstance.deleteMemberApiV1WorkspacesWorkspaceIdMembersMemberIdDelete(workspaceId, memberId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#deleteMemberApiV1WorkspacesWorkspaceIdMembersMemberIdDelete");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **workspaceId** | **String**|  | |
| **memberId** | **String**|  | |

### Return type

[**SimpleBoolResponse**](SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="deleteWorkspaceApiV1WorkspacesWorkspaceIdDelete"></a>
# **deleteWorkspaceApiV1WorkspacesWorkspaceIdDelete**
> SimpleBoolResponse deleteWorkspaceApiV1WorkspacesWorkspaceIdDelete(workspaceId)

Delete Workspace

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    String workspaceId = "workspaceId_example"; // String | 
    try {
      SimpleBoolResponse result = apiInstance.deleteWorkspaceApiV1WorkspacesWorkspaceIdDelete(workspaceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#deleteWorkspaceApiV1WorkspacesWorkspaceIdDelete");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **workspaceId** | **String**|  | |

### Return type

[**SimpleBoolResponse**](SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="getWorkspaceApiV1WorkspacesWorkspaceIdGet"></a>
# **getWorkspaceApiV1WorkspacesWorkspaceIdGet**
> WorkspaceResponse getWorkspaceApiV1WorkspacesWorkspaceIdGet(workspaceId)

Get Workspace

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    String workspaceId = "workspaceId_example"; // String | 
    try {
      WorkspaceResponse result = apiInstance.getWorkspaceApiV1WorkspacesWorkspaceIdGet(workspaceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#getWorkspaceApiV1WorkspacesWorkspaceIdGet");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **workspaceId** | **String**|  | |

### Return type

[**WorkspaceResponse**](WorkspaceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="listMembersApiV1WorkspacesWorkspaceIdMembersGet"></a>
# **listMembersApiV1WorkspacesWorkspaceIdMembersGet**
> WorkspaceMembersListResponse listMembersApiV1WorkspacesWorkspaceIdMembersGet(workspaceId)

List Members

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    String workspaceId = "workspaceId_example"; // String | 
    try {
      WorkspaceMembersListResponse result = apiInstance.listMembersApiV1WorkspacesWorkspaceIdMembersGet(workspaceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#listMembersApiV1WorkspacesWorkspaceIdMembersGet");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **workspaceId** | **String**|  | |

### Return type

[**WorkspaceMembersListResponse**](WorkspaceMembersListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="listWorkspacesApiV1WorkspacesGet"></a>
# **listWorkspacesApiV1WorkspacesGet**
> WorkspacesListResponse listWorkspacesApiV1WorkspacesGet(limit, cursor)

List Workspaces

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    Integer limit = 50; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      WorkspacesListResponse result = apiInstance.listWorkspacesApiV1WorkspacesGet(limit, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#listWorkspacesApiV1WorkspacesGet");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **limit** | **Integer**|  | [optional] [default to 50] |
| **cursor** | **String**|  | [optional] |

### Return type

[**WorkspacesListResponse**](WorkspacesListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="patchMemberApiV1WorkspacesWorkspaceIdMembersMemberIdPatch"></a>
# **patchMemberApiV1WorkspacesWorkspaceIdMembersMemberIdPatch**
> WorkspaceMemberOut patchMemberApiV1WorkspacesWorkspaceIdMembersMemberIdPatch(workspaceId, memberId, workspaceMemberPatchRequest)

Patch Member

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    String workspaceId = "workspaceId_example"; // String | 
    String memberId = "memberId_example"; // String | 
    WorkspaceMemberPatchRequest workspaceMemberPatchRequest = new WorkspaceMemberPatchRequest(); // WorkspaceMemberPatchRequest | 
    try {
      WorkspaceMemberOut result = apiInstance.patchMemberApiV1WorkspacesWorkspaceIdMembersMemberIdPatch(workspaceId, memberId, workspaceMemberPatchRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#patchMemberApiV1WorkspacesWorkspaceIdMembersMemberIdPatch");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **workspaceId** | **String**|  | |
| **memberId** | **String**|  | |
| **workspaceMemberPatchRequest** | [**WorkspaceMemberPatchRequest**](WorkspaceMemberPatchRequest.md)|  | |

### Return type

[**WorkspaceMemberOut**](WorkspaceMemberOut.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="patchWorkspaceApiV1WorkspacesWorkspaceIdPatch"></a>
# **patchWorkspaceApiV1WorkspacesWorkspaceIdPatch**
> WorkspaceResponse patchWorkspaceApiV1WorkspacesWorkspaceIdPatch(workspaceId, workspacePatchRequest, idempotencyKey)

Patch Workspace

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.WorkspacesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    WorkspacesApi apiInstance = new WorkspacesApi(defaultClient);
    String workspaceId = "workspaceId_example"; // String | 
    WorkspacePatchRequest workspacePatchRequest = new WorkspacePatchRequest(); // WorkspacePatchRequest | 
    String idempotencyKey = "idempotencyKey_example"; // String | 
    try {
      WorkspaceResponse result = apiInstance.patchWorkspaceApiV1WorkspacesWorkspaceIdPatch(workspaceId, workspacePatchRequest, idempotencyKey);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WorkspacesApi#patchWorkspaceApiV1WorkspacesWorkspaceIdPatch");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **workspaceId** | **String**|  | |
| **workspacePatchRequest** | [**WorkspacePatchRequest**](WorkspacePatchRequest.md)|  | |
| **idempotencyKey** | **String**|  | [optional] |

### Return type

[**WorkspaceResponse**](WorkspaceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |


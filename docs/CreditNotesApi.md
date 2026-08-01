# CreditNotesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createCreditNoteApiV1CreditNotesPost**](CreditNotesApi.md#createCreditNoteApiV1CreditNotesPost) | **POST** /api/v1/credit-notes | Create Credit Note |
| [**finalizeCreditNoteApiV1CreditNotesCreditNoteIdFinalizePost**](CreditNotesApi.md#finalizeCreditNoteApiV1CreditNotesCreditNoteIdFinalizePost) | **POST** /api/v1/credit-notes/{credit_note_id}/finalize | Finalize Credit Note |
| [**getCreditNoteApiV1CreditNotesCreditNoteIdGet**](CreditNotesApi.md#getCreditNoteApiV1CreditNotesCreditNoteIdGet) | **GET** /api/v1/credit-notes/{credit_note_id} | Get Credit Note |
| [**listCreditNotesApiV1CreditNotesGet**](CreditNotesApi.md#listCreditNotesApiV1CreditNotesGet) | **GET** /api/v1/credit-notes | List Credit Notes |
| [**renderCreditNoteApiV1CreditNotesCreditNoteIdRendersPost**](CreditNotesApi.md#renderCreditNoteApiV1CreditNotesCreditNoteIdRendersPost) | **POST** /api/v1/credit-notes/{credit_note_id}/renders | Render Credit Note |


<a id="createCreditNoteApiV1CreditNotesPost"></a>
# **createCreditNoteApiV1CreditNotesPost**
> CreditNoteResponse createCreditNoteApiV1CreditNotesPost(creditNoteCreateRequest)

Create Credit Note

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.CreditNotesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    CreditNotesApi apiInstance = new CreditNotesApi(defaultClient);
    CreditNoteCreateRequest creditNoteCreateRequest = new CreditNoteCreateRequest(); // CreditNoteCreateRequest | 
    try {
      CreditNoteResponse result = apiInstance.createCreditNoteApiV1CreditNotesPost(creditNoteCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CreditNotesApi#createCreditNoteApiV1CreditNotesPost");
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
| **creditNoteCreateRequest** | [**CreditNoteCreateRequest**](CreditNoteCreateRequest.md)|  | |

### Return type

[**CreditNoteResponse**](CreditNoteResponse.md)

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

<a id="finalizeCreditNoteApiV1CreditNotesCreditNoteIdFinalizePost"></a>
# **finalizeCreditNoteApiV1CreditNotesCreditNoteIdFinalizePost**
> CreditNoteResponse finalizeCreditNoteApiV1CreditNotesCreditNoteIdFinalizePost(creditNoteId)

Finalize Credit Note

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.CreditNotesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    CreditNotesApi apiInstance = new CreditNotesApi(defaultClient);
    String creditNoteId = "creditNoteId_example"; // String | 
    try {
      CreditNoteResponse result = apiInstance.finalizeCreditNoteApiV1CreditNotesCreditNoteIdFinalizePost(creditNoteId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CreditNotesApi#finalizeCreditNoteApiV1CreditNotesCreditNoteIdFinalizePost");
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
| **creditNoteId** | **String**|  | |

### Return type

[**CreditNoteResponse**](CreditNoteResponse.md)

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

<a id="getCreditNoteApiV1CreditNotesCreditNoteIdGet"></a>
# **getCreditNoteApiV1CreditNotesCreditNoteIdGet**
> CreditNoteResponse getCreditNoteApiV1CreditNotesCreditNoteIdGet(creditNoteId)

Get Credit Note

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.CreditNotesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    CreditNotesApi apiInstance = new CreditNotesApi(defaultClient);
    String creditNoteId = "creditNoteId_example"; // String | 
    try {
      CreditNoteResponse result = apiInstance.getCreditNoteApiV1CreditNotesCreditNoteIdGet(creditNoteId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CreditNotesApi#getCreditNoteApiV1CreditNotesCreditNoteIdGet");
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
| **creditNoteId** | **String**|  | |

### Return type

[**CreditNoteResponse**](CreditNoteResponse.md)

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

<a id="listCreditNotesApiV1CreditNotesGet"></a>
# **listCreditNotesApiV1CreditNotesGet**
> CreditNotesListResponse listCreditNotesApiV1CreditNotesGet(limit, cursor)

List Credit Notes

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.CreditNotesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    CreditNotesApi apiInstance = new CreditNotesApi(defaultClient);
    Integer limit = 50; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      CreditNotesListResponse result = apiInstance.listCreditNotesApiV1CreditNotesGet(limit, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CreditNotesApi#listCreditNotesApiV1CreditNotesGet");
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

[**CreditNotesListResponse**](CreditNotesListResponse.md)

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

<a id="renderCreditNoteApiV1CreditNotesCreditNoteIdRendersPost"></a>
# **renderCreditNoteApiV1CreditNotesCreditNoteIdRendersPost**
> Object renderCreditNoteApiV1CreditNotesCreditNoteIdRendersPost(creditNoteId, creditNoteRenderRequest)

Render Credit Note

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.CreditNotesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    CreditNotesApi apiInstance = new CreditNotesApi(defaultClient);
    String creditNoteId = "creditNoteId_example"; // String | 
    CreditNoteRenderRequest creditNoteRenderRequest = new CreditNoteRenderRequest(); // CreditNoteRenderRequest | 
    try {
      Object result = apiInstance.renderCreditNoteApiV1CreditNotesCreditNoteIdRendersPost(creditNoteId, creditNoteRenderRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CreditNotesApi#renderCreditNoteApiV1CreditNotesCreditNoteIdRendersPost");
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
| **creditNoteId** | **String**|  | |
| **creditNoteRenderRequest** | [**CreditNoteRenderRequest**](CreditNoteRenderRequest.md)|  | [optional] |

### Return type

**Object**

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


# InvoiceAttachmentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createAttachmentApiV1DocumentsInvoiceIdAttachmentsPost**](InvoiceAttachmentsApi.md#createAttachmentApiV1DocumentsInvoiceIdAttachmentsPost) | **POST** /api/v1/documents/{invoice_id}/attachments | Create Attachment |
| [**deleteAttachmentApiV1DocumentsInvoiceIdAttachmentsAttachmentIdDelete**](InvoiceAttachmentsApi.md#deleteAttachmentApiV1DocumentsInvoiceIdAttachmentsAttachmentIdDelete) | **DELETE** /api/v1/documents/{invoice_id}/attachments/{attachment_id} | Delete Attachment |
| [**listAttachmentsApiV1DocumentsInvoiceIdAttachmentsGet**](InvoiceAttachmentsApi.md#listAttachmentsApiV1DocumentsInvoiceIdAttachmentsGet) | **GET** /api/v1/documents/{invoice_id}/attachments | List Attachments |


<a id="createAttachmentApiV1DocumentsInvoiceIdAttachmentsPost"></a>
# **createAttachmentApiV1DocumentsInvoiceIdAttachmentsPost**
> InvoiceAttachmentResponse createAttachmentApiV1DocumentsInvoiceIdAttachmentsPost(invoiceId, invoiceAttachmentCreateRequest)

Create Attachment

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoiceAttachmentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoiceAttachmentsApi apiInstance = new InvoiceAttachmentsApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    InvoiceAttachmentCreateRequest invoiceAttachmentCreateRequest = new InvoiceAttachmentCreateRequest(); // InvoiceAttachmentCreateRequest | 
    try {
      InvoiceAttachmentResponse result = apiInstance.createAttachmentApiV1DocumentsInvoiceIdAttachmentsPost(invoiceId, invoiceAttachmentCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoiceAttachmentsApi#createAttachmentApiV1DocumentsInvoiceIdAttachmentsPost");
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
| **invoiceId** | **String**|  | |
| **invoiceAttachmentCreateRequest** | [**InvoiceAttachmentCreateRequest**](InvoiceAttachmentCreateRequest.md)|  | |

### Return type

[**InvoiceAttachmentResponse**](InvoiceAttachmentResponse.md)

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

<a id="deleteAttachmentApiV1DocumentsInvoiceIdAttachmentsAttachmentIdDelete"></a>
# **deleteAttachmentApiV1DocumentsInvoiceIdAttachmentsAttachmentIdDelete**
> SimpleBoolResponse deleteAttachmentApiV1DocumentsInvoiceIdAttachmentsAttachmentIdDelete(invoiceId, attachmentId)

Delete Attachment

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoiceAttachmentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoiceAttachmentsApi apiInstance = new InvoiceAttachmentsApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    String attachmentId = "attachmentId_example"; // String | 
    try {
      SimpleBoolResponse result = apiInstance.deleteAttachmentApiV1DocumentsInvoiceIdAttachmentsAttachmentIdDelete(invoiceId, attachmentId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoiceAttachmentsApi#deleteAttachmentApiV1DocumentsInvoiceIdAttachmentsAttachmentIdDelete");
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
| **invoiceId** | **String**|  | |
| **attachmentId** | **String**|  | |

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

<a id="listAttachmentsApiV1DocumentsInvoiceIdAttachmentsGet"></a>
# **listAttachmentsApiV1DocumentsInvoiceIdAttachmentsGet**
> InvoiceAttachmentsListResponse listAttachmentsApiV1DocumentsInvoiceIdAttachmentsGet(invoiceId)

List Attachments

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoiceAttachmentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoiceAttachmentsApi apiInstance = new InvoiceAttachmentsApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    try {
      InvoiceAttachmentsListResponse result = apiInstance.listAttachmentsApiV1DocumentsInvoiceIdAttachmentsGet(invoiceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoiceAttachmentsApi#listAttachmentsApiV1DocumentsInvoiceIdAttachmentsGet");
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
| **invoiceId** | **String**|  | |

### Return type

[**InvoiceAttachmentsListResponse**](InvoiceAttachmentsListResponse.md)

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


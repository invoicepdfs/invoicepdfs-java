# BillingApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createCheckoutApiV1BillingCheckoutSessionPost**](BillingApi.md#createCheckoutApiV1BillingCheckoutSessionPost) | **POST** /api/v1/billing/checkout-session | Create Checkout |
| [**createPortalApiV1BillingPortalSessionPost**](BillingApi.md#createPortalApiV1BillingPortalSessionPost) | **POST** /api/v1/billing/portal-session | Create Portal |
| [**getSubscriptionApiV1BillingSubscriptionGet**](BillingApi.md#getSubscriptionApiV1BillingSubscriptionGet) | **GET** /api/v1/billing/subscription | Get Subscription |
| [**listPlansApiV1BillingPlansGet**](BillingApi.md#listPlansApiV1BillingPlansGet) | **GET** /api/v1/billing/plans | List Plans |


<a id="createCheckoutApiV1BillingCheckoutSessionPost"></a>
# **createCheckoutApiV1BillingCheckoutSessionPost**
> BillingCheckoutResponse createCheckoutApiV1BillingCheckoutSessionPost(billingCheckoutRequest)

Create Checkout

Create a Stripe Checkout session for a subscription.

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BillingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BillingApi apiInstance = new BillingApi(defaultClient);
    BillingCheckoutRequest billingCheckoutRequest = new BillingCheckoutRequest(); // BillingCheckoutRequest | 
    try {
      BillingCheckoutResponse result = apiInstance.createCheckoutApiV1BillingCheckoutSessionPost(billingCheckoutRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BillingApi#createCheckoutApiV1BillingCheckoutSessionPost");
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
| **billingCheckoutRequest** | [**BillingCheckoutRequest**](BillingCheckoutRequest.md)|  | |

### Return type

[**BillingCheckoutResponse**](BillingCheckoutResponse.md)

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

<a id="createPortalApiV1BillingPortalSessionPost"></a>
# **createPortalApiV1BillingPortalSessionPost**
> BillingPortalResponse createPortalApiV1BillingPortalSessionPost()

Create Portal

Create a Stripe Customer Portal session for self-service management.

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BillingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BillingApi apiInstance = new BillingApi(defaultClient);
    try {
      BillingPortalResponse result = apiInstance.createPortalApiV1BillingPortalSessionPost();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BillingApi#createPortalApiV1BillingPortalSessionPost");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**BillingPortalResponse**](BillingPortalResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="getSubscriptionApiV1BillingSubscriptionGet"></a>
# **getSubscriptionApiV1BillingSubscriptionGet**
> BillingSubscriptionResponse getSubscriptionApiV1BillingSubscriptionGet()

Get Subscription

Get current subscription status (from DB, no Stripe API call).

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BillingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BillingApi apiInstance = new BillingApi(defaultClient);
    try {
      BillingSubscriptionResponse result = apiInstance.getSubscriptionApiV1BillingSubscriptionGet();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BillingApi#getSubscriptionApiV1BillingSubscriptionGet");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**BillingSubscriptionResponse**](BillingSubscriptionResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="listPlansApiV1BillingPlansGet"></a>
# **listPlansApiV1BillingPlansGet**
> BillingPlansListResponse listPlansApiV1BillingPlansGet()

List Plans

Purchasable plans — the ones wired to a Stripe price.

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.BillingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    BillingApi apiInstance = new BillingApi(defaultClient);
    try {
      BillingPlansListResponse result = apiInstance.listPlansApiV1BillingPlansGet();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BillingApi#listPlansApiV1BillingPlansGet");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**BillingPlansListResponse**](BillingPlansListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |


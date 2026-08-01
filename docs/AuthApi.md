# AuthApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**forgotPasswordApiV1AuthForgotPasswordPost**](AuthApi.md#forgotPasswordApiV1AuthForgotPasswordPost) | **POST** /api/v1/auth/forgot-password | Forgot Password |
| [**logoutApiV1AuthLogoutPost**](AuthApi.md#logoutApiV1AuthLogoutPost) | **POST** /api/v1/auth/logout | Logout |
| [**meApiV1AuthMeGet**](AuthApi.md#meApiV1AuthMeGet) | **GET** /api/v1/auth/me | Me |
| [**patchMeApiV1AuthMePatch**](AuthApi.md#patchMeApiV1AuthMePatch) | **PATCH** /api/v1/auth/me | Patch Me |
| [**refreshApiV1AuthRefreshPost**](AuthApi.md#refreshApiV1AuthRefreshPost) | **POST** /api/v1/auth/refresh | Refresh |
| [**registerApiV1AuthRegisterPost**](AuthApi.md#registerApiV1AuthRegisterPost) | **POST** /api/v1/auth/register | Register |
| [**resetPasswordApiV1AuthResetPasswordPost**](AuthApi.md#resetPasswordApiV1AuthResetPasswordPost) | **POST** /api/v1/auth/reset-password | Reset Password |
| [**tokenExchangeApiV1AuthTokenPost**](AuthApi.md#tokenExchangeApiV1AuthTokenPost) | **POST** /api/v1/auth/token | Token Exchange |


<a id="forgotPasswordApiV1AuthForgotPasswordPost"></a>
# **forgotPasswordApiV1AuthForgotPasswordPost**
> AuthMessageResponse forgotPasswordApiV1AuthForgotPasswordPost(authForgotPasswordRequest)

Forgot Password

Send a password reset email via Firebase.

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.AuthApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AuthApi apiInstance = new AuthApi(defaultClient);
    AuthForgotPasswordRequest authForgotPasswordRequest = new AuthForgotPasswordRequest(); // AuthForgotPasswordRequest | 
    try {
      AuthMessageResponse result = apiInstance.forgotPasswordApiV1AuthForgotPasswordPost(authForgotPasswordRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthApi#forgotPasswordApiV1AuthForgotPasswordPost");
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
| **authForgotPasswordRequest** | [**AuthForgotPasswordRequest**](AuthForgotPasswordRequest.md)|  | |

### Return type

[**AuthMessageResponse**](AuthMessageResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="logoutApiV1AuthLogoutPost"></a>
# **logoutApiV1AuthLogoutPost**
> AuthMessageResponse logoutApiV1AuthLogoutPost()

Logout

Revoke all Firebase refresh tokens for the authenticated user.

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.AuthApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    AuthApi apiInstance = new AuthApi(defaultClient);
    try {
      AuthMessageResponse result = apiInstance.logoutApiV1AuthLogoutPost();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthApi#logoutApiV1AuthLogoutPost");
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

[**AuthMessageResponse**](AuthMessageResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="meApiV1AuthMeGet"></a>
# **meApiV1AuthMeGet**
> AuthMeResponse meApiV1AuthMeGet()

Me

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.AuthApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    AuthApi apiInstance = new AuthApi(defaultClient);
    try {
      AuthMeResponse result = apiInstance.meApiV1AuthMeGet();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthApi#meApiV1AuthMeGet");
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

[**AuthMeResponse**](AuthMeResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="patchMeApiV1AuthMePatch"></a>
# **patchMeApiV1AuthMePatch**
> AuthMeResponse patchMeApiV1AuthMePatch(authMePatchRequest)

Patch Me

Update the authenticated account&#39;s name or email.

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.AuthApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    AuthApi apiInstance = new AuthApi(defaultClient);
    AuthMePatchRequest authMePatchRequest = new AuthMePatchRequest(); // AuthMePatchRequest | 
    try {
      AuthMeResponse result = apiInstance.patchMeApiV1AuthMePatch(authMePatchRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthApi#patchMeApiV1AuthMePatch");
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
| **authMePatchRequest** | [**AuthMePatchRequest**](AuthMePatchRequest.md)|  | |

### Return type

[**AuthMeResponse**](AuthMeResponse.md)

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

<a id="refreshApiV1AuthRefreshPost"></a>
# **refreshApiV1AuthRefreshPost**
> AuthRefreshResponse refreshApiV1AuthRefreshPost(authRefreshRequest)

Refresh

Exchange a Firebase refresh token for a new ID token.

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.AuthApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AuthApi apiInstance = new AuthApi(defaultClient);
    AuthRefreshRequest authRefreshRequest = new AuthRefreshRequest(); // AuthRefreshRequest | 
    try {
      AuthRefreshResponse result = apiInstance.refreshApiV1AuthRefreshPost(authRefreshRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthApi#refreshApiV1AuthRefreshPost");
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
| **authRefreshRequest** | [**AuthRefreshRequest**](AuthRefreshRequest.md)|  | |

### Return type

[**AuthRefreshResponse**](AuthRefreshResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="registerApiV1AuthRegisterPost"></a>
# **registerApiV1AuthRegisterPost**
> AuthRegisterResponse registerApiV1AuthRegisterPost(authRegisterRequest)

Register

Register a new account using a Firebase ID token.  The client authenticates with Firebase (email/password, Google, etc.) and sends the resulting ID token here to create an InvoicePDFs account.

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.AuthApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AuthApi apiInstance = new AuthApi(defaultClient);
    AuthRegisterRequest authRegisterRequest = new AuthRegisterRequest(); // AuthRegisterRequest | 
    try {
      AuthRegisterResponse result = apiInstance.registerApiV1AuthRegisterPost(authRegisterRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthApi#registerApiV1AuthRegisterPost");
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
| **authRegisterRequest** | [**AuthRegisterRequest**](AuthRegisterRequest.md)|  | |

### Return type

[**AuthRegisterResponse**](AuthRegisterResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="resetPasswordApiV1AuthResetPasswordPost"></a>
# **resetPasswordApiV1AuthResetPasswordPost**
> AuthMessageResponse resetPasswordApiV1AuthResetPasswordPost(authResetPasswordRequest)

Reset Password

Confirm a password reset using the code from the reset email.

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.AuthApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AuthApi apiInstance = new AuthApi(defaultClient);
    AuthResetPasswordRequest authResetPasswordRequest = new AuthResetPasswordRequest(); // AuthResetPasswordRequest | 
    try {
      AuthMessageResponse result = apiInstance.resetPasswordApiV1AuthResetPasswordPost(authResetPasswordRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthApi#resetPasswordApiV1AuthResetPasswordPost");
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
| **authResetPasswordRequest** | [**AuthResetPasswordRequest**](AuthResetPasswordRequest.md)|  | |

### Return type

[**AuthMessageResponse**](AuthMessageResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="tokenExchangeApiV1AuthTokenPost"></a>
# **tokenExchangeApiV1AuthTokenPost**
> AuthTokenResponse tokenExchangeApiV1AuthTokenPost(authTokenRequest)

Token Exchange

Exchange a Firebase ID token for account info.  Use this on login: the client authenticates with Firebase, sends the ID token here, and receives the InvoicePDFs account details. The Firebase token itself is used as the Bearer token for subsequent API calls.

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.AuthApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");

    AuthApi apiInstance = new AuthApi(defaultClient);
    AuthTokenRequest authTokenRequest = new AuthTokenRequest(); // AuthTokenRequest | 
    try {
      AuthTokenResponse result = apiInstance.tokenExchangeApiV1AuthTokenPost(authTokenRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AuthApi#tokenExchangeApiV1AuthTokenPost");
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
| **authTokenRequest** | [**AuthTokenRequest**](AuthTokenRequest.md)|  | |

### Return type

[**AuthTokenResponse**](AuthTokenResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |


# Swagger\Client\DefaultApi

All URIs are relative to *https://localhost/api/v2/operations*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getTicket**](DefaultApi.md#getTicket) | **GET** /tickets/{ticket_id} | 
[**getTickets**](DefaultApi.md#getTickets) | **GET** /tickets | 
[**postMessages**](DefaultApi.md#postMessages) | **POST** /tickets/{ticket_id}/messages | 
[**postTickets**](DefaultApi.md#postTickets) | **POST** /tickets | 
[**putTickets**](DefaultApi.md#putTickets) | **PUT** /tickets | 


# **getTicket**
> \Swagger\Client\Model\Ticket getTicket($ticket_id, $authentication_token, $category, $statuses, $ordered_column, $ordered_by, $client_id, $client_secret)



Retrievs a ticket

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\DefaultApi();
$ticket_id = "ticket_id_example"; // string | 
$authentication_token = "authentication_token_example"; // string | 
$category = "category_example"; // string | 
$statuses = "statuses_example"; // string | 
$ordered_column = "ordered_column_example"; // string | 
$ordered_by = "ordered_by_example"; // string | 
$client_id = "client_id_example"; // string | 
$client_secret = "client_secret_example"; // string | 

try {
    $result = $api_instance->getTicket($ticket_id, $authentication_token, $category, $statuses, $ordered_column, $ordered_by, $client_id, $client_secret);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->getTicket: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ticket_id** | **string**|  |
 **authentication_token** | **string**|  | [optional]
 **category** | **string**|  | [optional]
 **statuses** | **string**|  | [optional]
 **ordered_column** | **string**|  | [optional]
 **ordered_by** | **string**|  | [optional]
 **client_id** | **string**|  | [optional]
 **client_secret** | **string**|  | [optional]

### Return type

[**\Swagger\Client\Model\Ticket**](../Model/Ticket.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getTickets**
> \Swagger\Client\Model\Ticket[] getTickets($authentication_token, $start, $length, $draw, $q, $sort_by, $sort_by_order, $passed_account_id, $passed_user_id, $view_id, $client_id, $client_secret)



Retrieve tickets

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\DefaultApi();
$authentication_token = 3.4; // float | User athentication uuid
$start = 56; // int | Start query value
$length = 56; // int | Number of rows query
$draw = 56; // int | Number of times table has been reloaded
$q = "q_example"; // string | Values provided in q are tokenized and search on columns: TICKET_ID,SUBJECT,REQUESTOR_UERNAME, REQUESTOR_EMAIL, TICKET_MESSAGES
$sort_by = "sort_by_example"; // string | Column name to order table by
$sort_by_order = "sort_by_order_example"; // string | Sort by ascending or descending
$passed_account_id = "passed_account_id_example"; // string | 
$passed_user_id = "passed_user_id_example"; // string | 
$view_id = 56; // int | View Id
$client_id = "client_id_example"; // string | API ID
$client_secret = "client_secret_example"; // string | API Secret

try {
    $result = $api_instance->getTickets($authentication_token, $start, $length, $draw, $q, $sort_by, $sort_by_order, $passed_account_id, $passed_user_id, $view_id, $client_id, $client_secret);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->getTickets: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authentication_token** | **float**| User athentication uuid | [optional]
 **start** | **int**| Start query value | [optional]
 **length** | **int**| Number of rows query | [optional]
 **draw** | **int**| Number of times table has been reloaded | [optional]
 **q** | **string**| Values provided in q are tokenized and search on columns: TICKET_ID,SUBJECT,REQUESTOR_UERNAME, REQUESTOR_EMAIL, TICKET_MESSAGES | [optional]
 **sort_by** | **string**| Column name to order table by | [optional]
 **sort_by_order** | **string**| Sort by ascending or descending | [optional]
 **passed_account_id** | **string**|  | [optional]
 **passed_user_id** | **string**|  | [optional]
 **view_id** | **int**| View Id | [optional]
 **client_id** | **string**| API ID | [optional]
 **client_secret** | **string**| API Secret | [optional]

### Return type

[**\Swagger\Client\Model\Ticket[]**](../Model/Ticket.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postMessages**
> postMessages($body, $ticket_id, $authentication_token, $client_id, $client_secret)



Insert a messages

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\DefaultApi();
$body = new \Swagger\Client\Model\Ticket(); // \Swagger\Client\Model\Ticket | The request body for the operation
$ticket_id = "ticket_id_example"; // string | 
$authentication_token = "authentication_token_example"; // string | User athentication
$client_id = "client_id_example"; // string | api client
$client_secret = "client_secret_example"; // string | api secret

try {
    $api_instance->postMessages($body, $ticket_id, $authentication_token, $client_id, $client_secret);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->postMessages: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\Ticket**](../Model/Ticket.md)| The request body for the operation |
 **ticket_id** | **string**|  |
 **authentication_token** | **string**| User athentication | [optional]
 **client_id** | **string**| api client | [optional]
 **client_secret** | **string**| api secret | [optional]

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **postTickets**
> \Swagger\Client\Model\Ticket postTickets($body, $authentication_token, $client_id, $client_secret)



Insert a tickets

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\DefaultApi();
$body = array(new \Swagger\Client\Model\TicketMessage()); // \Swagger\Client\Model\TicketMessage[] | The request body for the operation
$authentication_token = 3.4; // float | User athentication uuid
$client_id = "client_id_example"; // string | 
$client_secret = "client_secret_example"; // string | 

try {
    $result = $api_instance->postTickets($body, $authentication_token, $client_id, $client_secret);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->postTickets: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\TicketMessage[]**](../Model/TicketMessage.md)| The request body for the operation |
 **authentication_token** | **float**| User athentication uuid | [optional]
 **client_id** | **string**|  | [optional]
 **client_secret** | **string**|  | [optional]

### Return type

[**\Swagger\Client\Model\Ticket**](../Model/Ticket.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **putTickets**
> \Swagger\Client\Model\Ticket[] putTickets($body, $authentication_token, $client_id, $client_secret)



Update tickets

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$api_instance = new Swagger\Client\Api\DefaultApi();
$body = array(new \Swagger\Client\Model\Ticket()); // \Swagger\Client\Model\Ticket[] | The request body for the operation
$authentication_token = true; // bool | User athentication uuid
$client_id = "client_id_example"; // string | 
$client_secret = "client_secret_example"; // string | 

try {
    $result = $api_instance->putTickets($body, $authentication_token, $client_id, $client_secret);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->putTickets: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\Ticket[]**](../Model/Ticket.md)| The request body for the operation |
 **authentication_token** | **bool**| User athentication uuid | [optional]
 **client_id** | **string**|  | [optional]
 **client_secret** | **string**|  | [optional]

### Return type

[**\Swagger\Client\Model\Ticket[]**](../Model/Ticket.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)


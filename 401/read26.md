#  DRF Permissions
---
#### Permission checks are always run at the very start of the view, before any other code is allowed to proceed. Permission checks will typically use the authentication information in the request.user and request.auth properties to determine if the incoming request should be permitted.

#### Permissions are used to grant or deny access for different classes of users to different parts of the API.

#### The simplest style of permission would be to allow access to any authenticated user, and deny access to any unauthenticated user. This corresponds to the IsAuthenticated class in REST framework.


### Permissions works 

#### Before running the main body of the view each permission in the list is checked. If any permission check fails an exceptions.PermissionDenied or exceptions.NotAuthenticated exception will be raised, and the main body of the view will not run.

### Rules


- The request was successfully authenticated, but permission was denied. — An HTTP 403 Forbidden response will be returned.
- The request was not successfully authenticated, and the highest priority authentication class does not use WWW-Authenticate headers. — An HTTP 403 Forbidden response will be returned.
- The request was not successfully authenticated, and the highest priority authentication class does use WWW-Authenticate headers. — An HTTP 401 Unauthorized response, with an appropriate WWW-Authenticate header will be returned.


#### Object level permissions are used to determine if a user should be allowed to act on a particular object, which will typically be a model instance.

### Setting the permission policy
```
REST_FRAMEWORK = {
    'DEFAULT_PERMISSION_CLASSES': [
        'rest_framework.permissions.IsAuthenticated',
    ]
}
```
### If not specified, this setting defaults to allowing unrestricted access:
```
'DEFAULT_PERMISSION_CLASSES': [
   'rest_framework.permissions.AllowAny',
]
```
### API Reference

- IsAuthenticated
- IsAdminUser
- IsAuthenticatedOrReadOnly
- DjangoModelPermissions

- POST requests require the user to have the add permission on the model.
- PUT and PATCH requests require the user to have the change permission on the model.
- DELETE requests require the user to have the delete permission on the model.


### Overview of access restriction methods

- queryset/get_queryset(): Limits the general visibility of existing objects from the database. The queryset limits which objects will be listed and which objects can be modified or deleted. The get_queryset() method can apply different querysets based on the current action.
- permission_classes/get_permissions(): General permission checks based on the current action, request and targeted object. Object level permissions can only be applied to retrieve, modify and deletion actions. Permission checks for list and create will be applied to the entire object type. (In case of list: subject to restrictions in the queryset.)
- serializer_class/get_serializer(): Instance level restrictions that apply to all objects on input and output. The serializer may have access to the request context. The get_serializer() method can apply different serializers based on the current action.


### Third party packages
- DRF - Access Policy
- Composed Permissions
- REST Condition
- DRY Rest Permissions
- Django Rest Framework Roles
- Django REST Framework API Key
- Django Rest Framework Role Filters
- Django Rest Framework PSQ




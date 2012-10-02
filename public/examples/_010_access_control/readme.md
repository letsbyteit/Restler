Access Control <requires>PHP >= 5.3</requires>
--------------

<tag>access-control acl secure</tag>

This example shows how you can extend the authentication system to create
a robust access control sytem. As a adaed bonus we also restrict api
documentatation based on the same.

When the `api_key` is
- blank you will see the public api
- `12345` will show the api that is accessible by an user
- `67890` will show all api with the admin rights

Try it out yourself [here](explorer/index.html#!/authors-v1)

> This API Server is made using the following php files/folders

> * index.php      (gateway)
> * Resources.php      (api)
> * RateLimit.php      (helper)
> * Access.php      (api)
> * AccessControl.php      (auth)
> * restler.php      (framework)
> * JsonFormat.php      (format)

This API Server exposes the following URIs

    GET all                       ⇠ Access::all()
    GET user                      ⇠ Access::user()
    GET admin                     ⇠ Access::admin()
    GET resources/{id}-v{version} ⇠ Resources::get()
    GET resources/v{version}      ⇠ Resources::get()
    GET resources                 ⇠ Resources::index()







*[index.php]: _010_access_control/index.php
*[Resources.php]: ../../vendor/Luracast/Restler/Resources.php
*[RateLimit.php]: ../../vendor/Luracast/Restler/Filter/RateLimit.php
*[Access.php]: _010_access_control/Access.php
*[AccessControl.php]: _010_access_control/AccessControl.php
*[restler.php]: ../../vendor/restler.php
*[JsonFormat.php]: ../../vendor/Luracast/Restler/Format/JsonFormat.php

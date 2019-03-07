##This package is adopted from another project by https://github.com/kimkha/, which is not longer in support.
##The intention of this package is to do minor patches in order for projects to run with new version of react-admin (https://github.com/marmelab/admin-on-rest). No grantee of support.

##Please read following section for other/ newer/ better alternative solutions to use loopback with react-admin.

===>
# Loopback-style REST Client for Admin-on-rest

Loopback-style REST Client for [admin-on-rest](https://github.com/marmelab/admin-on-rest), the frontend framework for building admin applications on top of REST services.


## Not maintained anymore

With new [react-admin](), please use [loopback-component-react-admin](https://github.com/kimkha/loopback-component-react-admin) instead.

Because of recent changes of **admin-on-rest**, this module will only support version 0.9.0 (or later) of admin-on-rest.

## Prerequisite

* Your loopback server must response `X-Total-Count` header when querying list. Please use [loopback3-xTotalCount](https://github.com/kimkha/loopback3-xTotalCount) on your server end.

## How to use

1. `yarn add aor-loopback`
2. On your `App.js`, add this:

```
import loopbackRestClient from 'aor-loopback';

...

    <Admin restClient={loopbackRestClient('http://my.api.url/api')} ...>
```

3. If you want this module handle authentication, add this:

```
import loopbackRestClient, {authClient} from 'aor-loopback';

...

    <Admin restClient={loopbackRestClient('http://my.api.url/api')} authClient={authClient('http://my.api.url/api/users/login')} ...>
```

## Example

Please check example here: [loopback-aor-boilerplate](https://github.com/kimkha/loopback-aor-boilerplate), you should clone it and change your model later.

## License

This module is licensed under the [MIT Licence](LICENSE).

# Meteor Router Layer

This project helps package authors to support multiple routers.

The layer supports:

- [Iron Router](https://github.com/iron-meteor/iron-router)

Requires: ```iron:router```

- [Flow Router](https://github.com/kadirahq/flow-router)

Requires: ```kadira:flow-router``` ```kadira:blaze-layout```

## Api

#### RouterLayer.route(url, options)

Creates a new route

**Parameters**

**url**: `String`, The path of the route

**options**

**options.template**: `String`, The template for this route

**options.layout**: `String`, Optional. The layout for this route

**options.name**: `String`, Optional. The name of the route



#### RouterLayer.pathFor(routeName, params)

Returns the path for a route

**Parameters**

**routeName**: `String`, The name of the route

**params**: `Object`, Parameters for the route

**Returns**: `String`, The requested url


#### RouterLayer.isActiveRoute(routeName, params)

Check if the current route has the specified name and params (if set)

**Parameters**

**routeName**: `String`, The name of the route

**params**: `Object`, Optional. The parameters of the route

**Returns**: `Boolean`, True if the route is active


#### RouterLayer.isActiveRoutePartial(routeName)

Check if the current route name, divided by dots, starts with the specified name

**Parameters**

**routeName**: `String`, The name of the route

**Returns**: `Boolean`, True if the route is active

#### RouterLayer.go(routeName, params)

Redirects the user to the specified route

**Parameters**

**routeName**: `String`, The name of the route

**params**: `Object`, Optional. The parameters of the route

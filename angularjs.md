# ANGULARJS

# Sommaire
* [Controller](#controller)
* [Factory](#factory)
* [Route](#route)
* [Defer](#defer)
* [Récupérer une promesse : then()](#then)

## <a name="controller"></a>Controller
Créer un controller dans un fichier externe.

Raccourcis : **controller**

(*notation netbeans*)
```
(function () {
    angular.module(${'app'}).controller(${'ControllerName'}, ["$scope" ,
        function ($scope) {
            function init() {

            };
            
            init();
        }]);
})();
```
**notation
## <a name="factory"></a>Factory
Créer une factory dans un fichier externe

Raccourcis : **factory**

(*notation netbeans*)
```
(function () {
    angular.module(${'app'}).factory(${'name_factory'}, ['$http','$q', function ($http, $q) {
            var factory = {
                ${cursor}
            };

            return factory;
        }]);
})();
```

## <a name="route"></a>Route
Ajoute when() au $routeProvider pour ajouter une route

Raccourcis : **route_when**

(*notation netbeans*)
```
.when(${'url'}, {
  templateUrl: ${'template.html'},
  controller: ${'Controller'},
})
```
## <a name="defer">Defer
Récupérer les informations depuis le serveur de façon asynchrone avec le service $q

Raccourcis : **defer**

(*notation netbeans*)
```
var deferred = $q.defer();
$http.get(${'url'})
    .success(function (data, status) {
        deferred.resolve(data);
    })
    .error(function (data, status) {
        deferred.reject("${Error message}");
    });
return deferred.promise;
```

## <a name="then"></a>Récupérer une promesse : then()
Après avoir récupérer une promesse il faut la traiter avec *then()*

Raccourcis : **then**

(*notation netbeans*)
```
.then(function (${data}) {
    $scope.${variable} = ${data};
}, function (msg) {
    
});
```

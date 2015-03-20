# ANGULARJS

## Controller
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
## Factory
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

## Route
Ajoute when() au $routeProvider pour ajouter une route
Raccourcis : **route_when**

(*notation netbeans*)
```
.when(${'url'}, {
  templateUrl: ${'template.html'},
  controller: ${'Controller'},
})
```

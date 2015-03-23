# Symfony 2.5

# Sommaire
* [Json Response](#json_response)
* [Controller Action](#controller_action)
* [Controller Redirect](#controller_redirect)
* [Repository](#repository)
* [Query builder](#querybuilder)
* [Form](#form)
* [ManyToMany Annotation](#manytomany)
* [ManyToOne Annotation](#manytoone)
* [OneToMany Annotation](#onetomany)

## <a name="json_response"></a>Json Response 
Créer une réponse Json.

Raccourcis : **json**

(*notation netbeans*)

```
$serializer = $this->container->get('jms_serializer');
$jsonData = $serializer->serialize(${$data}, 'json');
$response = new JsonResponse();
$response->setContent($jsonData);
```

## <a name="controller_action"></a>Controller Action 
Créer une action pour controller.

Raccourcis : **sfaction**

(*notation netbeans*)

```
/**
* @Route("/${url}", name="${route_name}",options={"expose"=true})
* 
*/
public function ${name}Action(){
    
  return $this->render('${Bundle:Default:template.html.twig}');
}
```

## <a name="controller_redirect"></a>Controller redirect
Rediriger vers une URL dans un controller.

Raccourcis : **redirect**

(*notation netbeans*)

```
return $this->redirect($this->generateUrl(${'homepage'}));
```

## <a name="repository"></a>Repository 
Utiliser un repository dans un controller

Raccourcis : **repo**

(*notation netbeans*)

```
${$data} = $this->getDoctrine()
            ->getRepository(${'AppBundle:Product'})
                ${->findAll()}
            ;
```

## <a name="querybuilder"></a>QueryBuilder
Utiliser le query builder dans un repository.

Raccourcis : **querybuilder**

(*notation netbeans*)

```
${$data} = $this->createQueryBuilder('a')
            ->where('a.id=:id')
            ->setParameter('id', $id)
            ->orderBy('a.id', 'ASC')
            ->getQuery()
            ->getResult()
            ;
```

## <a name="form"></a>Form
Créer un formulaire directement dans le controller.

Raccourcis : **createform**

(*notation netbeans*)

```
${$form} = $this->createFormBuilder(${$object})
            ->add('field', 'text')
            ->getForm()
        ;
```

## <a name="manytomany"></a>ManyToMany Doctrine annotation
Annotation pour créer une relation *many to many* entre 2 entités.

Raccourcis : **manytomany**

(*notation netbeans*)

```
/**
* @ORM\ManyToMany(targetEntity="${Entity}",inversedBy="${current_entities}")
* @ORM\JoinTable(
*  joinColumns={@ORM\JoinColumn(name="${current_entity_id}",referencedColumnName="id")},
*  inverseJoinColumns={@ORM\JoinColumn(name="${target_entity_id}",referencedColumnName="id" )}
* )
*/
```

## <a name="manytoone"></a>ManyToOne Doctrine annotation
Annotation pour créer une relation *many to one*

Raccourcis : **manytoone**

(*notation netbeans*)

```
/**
* @Orm\ManyToOne(targetEntity="${Entity}", inversedBy="${current}")
*/
```

## <a name="onetomany"></a>OneToMany Doctrine annotation
Annotation pour créer une relation *one to many*

Raccourcis : **onetomany**

(*notation netbeans*)

```
/**
* @Orm\OneToMany(targetEntity="${Entity}", mappedBy="${current}")
*/
```

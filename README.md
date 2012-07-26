# SPARQL - JS - JQUERY

With this JavaScript class you can easily create sparql requests, and perform the request to an endpoint.

## Example

Here is a quick and easy request. Other examples are in the index.html file.

	var request = new SPARQL();
	request.info = "hello world";

	request.variable("?x").variable("?y").where("<http://dbpedia.org/resource/Metallica>", "?x", "?y");
			
	request.execute(function(data, info){
		
		console.log(data); //Json by default
		console.log(info); //Print hello world
		
	});

## Methods

	prefixe(namespace, url)

	distinct(trueOrFalse)

	variable(aVariableName)

	where(subject, predicate, object)

	optionalWhere(subject, predicate, object)

	union(SPARQLobject)

	filter(filter)

	orderBy(order)

	limit(limitNumber)

	offset(offsetNumber)

## Defaults

There are some values set by default in this classe :

	baseUrl //dbpedia endpoint

	format //json

	method // GET

	queryParam //parameter name for the query (GET or POST)

	formatParam //parameter name to ask the returned format
# Jazz Collaboration Graph for Neo4J

This is an experimental jazz collaboration graph for Neo4J created with data pulled from the open music encyclopedia Musicbrainz (musicbrainz.org). The file "jazz.cypher" contains cypher statements to load the graph into any Neo4J instance. 

Nodes represent individual musicians. Edges were derived by looking at whether two musicians had collaborated in the same album release.

Here is a query to get you started:

MATCH p = (a:Artist)-[:PLAYED_WITH]-(a2:Artist)
WHERE a.name = 'Miles Davis'
RETURN p


##### Node attributes include:

name: string,  
deceased: boolean,  
gender: boolean,    <--- 1 for male, 0 for female  
country: string,  
genre: string       <--- will always equal to "jazz" in this case  

Nodes: 12720
Edges: 139187

Feel free to get in touch with me at nfleig@hotmail.com if you would like me to add any additional attributes or if you have any ideas about how to make this graph even better. Also please be so kind to credit me if you use this graph in any way. And of course share your findings with me! :-) 

-- Nelson Fleig

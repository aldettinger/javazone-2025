# Javazone 2025

## How to prepare the demo ?

 + Create a terminator with 3 shells splitted horizontally
 + In each shell, scroll up x9
 + In each shell, `cd ~/dev/projects/camel-quarkus-examples-upstream/data-extract-langchain4j/`
 + In shell 2, `docker run --rm -it -v cqex-data-extract-ollama:/root/.ollama -p 11434:11434 --name cqex-data-extract-ollama ollama/ollama:0.9.3`
 + In shell 3, `docker exec -it cqex-data-extract-ollama ollama pull granite3.3:2b`
 + In shell 1, `mvn clean package -DskipTests`
 + In shell 1, `export QUARKUS_LANGCHAIN4J_OLLAMA_LOG_REQUESTS=true`
 + In shell 1, `java -jar target/quarkus-app/quarkus-run.jar`
 + In shell 3, prepare command `./send-conversations-to-camel-route.sh`
 + In eclipse, open `camel-quarkus-examples-upstream/data-extract-langchain4j`
    + `application.properties`
    + `CustomPojoExtractionService.java`
    + `Routes.java`
 + In eclipse, zoom in, CTRL+SHIFT+PLUS 3 times
 + In another workspace (CTRL+ALT+RIGHT), open `~/dev/projects/javazone-2025/JavaZone 2025.odp`

## Plan

 + Intro (1 min)
 + Contexts and definitions (4 min)
 + Explanation of AI related code (6 min)
 + Explanation of Integration related code (3 min)
 + Lessons learned and next steps (4 min)
 + Conclusion (1 min)

## TODO
 + Change the balance, too much time to explain the code, be more direct
 + Try to repeat without network
 + What are the key elements (unstructured data, structured output...)

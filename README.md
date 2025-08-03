# summarization-agent

Code sample from this [article](https://www.the-main-thread.com/p/build-ai-agent-java-quarkus-langchain4j-a2a).

Run agent (needs docker for ollama) : 
```shell script
./mvnw quarkus:dev
```

Run inspector (for wls) : 
```shell script
docker run --rm --add-host=host.docker.internal:$(cat /etc/resolv.conf | grep nameserver | awk '{print $2}') -p 8081:8080 srozange/a2a-inspector
```

Go to : ```http://localhost:8081/```   

Agent card url : ```host.docker.internal:8080```   

Message example : 
```
Shorten below text: Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old. Richard McClintock, a Latin professor at Hampden-Sydney College in Virginia, looked up one of the more obscure Latin words, consectetur, from a Lorem Ipsum passage, and going through the cites of the word in classical literature, discovered the undoubtable source. Lorem Ipsum comes from sections 1.10.32 and 1.10.33 of \"de Finibus Bonorum et Malorum\" (The Extremes of Good and Evil) by Cicero, written in 45 BC. This book is a treatise on the theory of ethics, very popular during the Renaissance. The first line of Lorem Ipsum, \"Lorem ipsum dolor sit amet..\", comes from a line in section 1.10.32.  The standard chunk of Lorem Ipsum used since the 1500s is reproduced below for those interested. Sections 1.10.32 and 1.10.33 from \"de Finibus Bonorum et Malorum\" by Cicero are also reproduced in their exact original form, accompanied by English versions from the 1914 translation by H. Rackham.
```
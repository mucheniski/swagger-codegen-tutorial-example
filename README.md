# swagger-codegen-tutorial-example
https://howtodoinjava.com/swagger2/code-generation-for-rest-api/  

## Swagger Editor  
https://editor.swagger.io/  

A documentacao precisa estar no formato yaml, caso no esteja o swagger editor converte, clicar em file > seva as YAML.  

Baixar o jar do swagger code gen https://repo1.maven.org/maven2/io/swagger/swagger-codegen-cli/2.3.1/ o swagger-codegen-cli-2.3.1.jar  

Usar o comando abaixo para gerar, pelo terminal, no mesmo diretório do jar e do arquivo YAML.  
~~~
Command to create api code
java -jar swagger-codegen-cli-2.3.1.jar generate \
  -i employee.yaml \
  --api-package com.howtodoinjava.example.employee.api \
  --model-package com.howtodoinjava.example.employee.model \
  --group-id com.howtodoinjava.example \
  --artifact-id spring-swagger-codegen-employee \
  --artifact-version 0.0.1-SNAPSHOT \
  -l spring \
  -o spring-swagger-codegen-employee
~~~  

Description of arguments:  

i: Swagger specification source file  
api-package: Package information for generated API class  
model-package: Package information for generated model class  
group-id: Maven properties  
artifact-id: Maven properties  
artifact-version: Maven properties  
l: Implementation framework, here Spring is used, which by default provides spring-boot  
o: Output directory  

Depois disso o projeto é criado, basta importar na IDE desejada.  

Com o projeto executando a api pode ser testada com o swagger html  http://localhost:8080/v1/swagger-ui.html  


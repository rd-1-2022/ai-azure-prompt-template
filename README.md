# Simple Spring AI Application with Azure OpenAI

This project contains a web service that will accept HTTP GET requests at
`http://localhost:8080/ai/simple`

There is optional `message` parameter whose default value is "Tell me a joke".

The response to the request is from the Azure OpenAI Service.

Look at the section below on **prerequisites** before continuing

## Building and running

```
./mvnw spring-boot:run
```

## Access the endpoint

To get a response for a funny joke about a cow.

```shell
$ http GET localhost:8080/ai/prompt?adjective=funny?topic=cow
```

A sample response is

```json
{
    "info": {},
    "text": "Why did the cow go to outer space? \n\nTo see the moooon!"
}
```

## Prerequisite

Obtain your Azure OpenAI `endpoint` and `api-key` from the Azure OpenAI Service section on [Azure Portal](https://portal.azure.com)

The Spring AI project defines a configuration property named `spring.ai.azure.openai.api-key` that you should set to the value of the `API Key` obtained from Azure.

Exporting an environment variables is one way to set these configuration properties.
```shell
export SPRING_AI_AZURE_OPENAI_API_KEY=<INSERT KEY HERE>
export SPRING_AI_AZURE_OPENAI_ENDPOINT=<INSERT ENDPOINT URL HERE>
```

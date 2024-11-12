# Spring AI with OpenAI Demo Project

This project contains a web service that will accept HTTP GET requests at
`http://localhost:8080/ai`.

There is optional `message` parameter whose default value is "Tell me a joke".

The response to the request is from the OpenAI ChatGPT Service.

The current default Chat Model used is GPT-4o.
The configuration property `spring.ai.openai.chat.options.model` is set to `gpt-3.5-turbo` to override the default Chat Model.

## Prerequisites

Before using the AI commands, make sure you have a developer token from OpenAI.

Create an account at [OpenAI Signup](https://platform.openai.com/signup) and generate the token at [API Keys](https://platform.openai.com/account/api-keys).

This demo project defines a configuration property named `spring.ai.openai.api-key` that you should set to the value of the `API Key` obtained from `openai.com`.

```
spring.ai.openai.api-key=<INSERT API KEY>
```

Set the API key before you run the application.

## Building and running

```
./mvnw spring-boot:run
```

## Access the endpoint

To get a response to the default request of "Tell me a joke"

```shell 
curl localhost:8080/ai
```

A sample response is

```text
Sure, here's a classic one for you:

Why don't scientists trust atoms?

Because they make up everything!
```

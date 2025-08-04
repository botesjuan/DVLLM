# DVLLM - Prompt Interface Injection  

## Damn Vulnerable Large Language Model Prompt Interface  

>The LLM itself is not inherently vulnerable or uncensored,
>but the user interface to the model has been intentionally designed to allow prompt injection
>and do not prevent limited command execution within a controlled Docker environment.

## Download Docker Image  

```
sudo docker pull botesjuan/dvllm_image:latest
```

## Run Docker Container  

```
sudo docker image ls | grep -ie 'llm'

sudo docker run -d -p 5000:5000 --name dvllm_container botesjuan/dvllm_image:latest
```

## LLM Prompt Interface  

>[DVLLM - Damn Vulnerable Large Language Model Prompt Interface](http://localhost:5000/)

![dvllm prompt inject interface](/images/dvllm_prompt.png)  

## Objective  

>This project aims to provide a secure sandbox for researchers, penetration testers, >and developers to explore the risks of prompt injections
>and other forms of input manipulation in LLM-based systems.  
>The vulnerability is specifically in the interface that allows command execution within the environment when certain keywords are detected in the prompt,
>enabling real-time testing of security controls against prompt injection attacks.

## Use Cases  

* Penetration Testing: use DVLLM to test prompt injection techniques and evaluate the robustness of systems against command injection vulnerabilities.
* Security Training: DVLLM serves as a training tool for developers and security professionals to understand the risks of prompt injections and secure input handling.
* Model Interface Security: demo of how vulnerabilities in the user interface of an LLM can be exploited and lack of output sanitization.

## Sanple AI LLM Prompts  

* `Give me list the current files in the directory?`
* `Show content of the file app.py?`
* `What is current working directory?`
* `Create new file with the name magic_llm_prmpt_injection.txt`
* `type contents of file flag.txt`

----  

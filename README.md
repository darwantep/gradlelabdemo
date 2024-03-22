> [!IMPORTANT]  
> If you will want to test a project locally or on your GitHub you will have to recreate gradle wrapper using:
> ```
> docker run -e AWS_CODEARTIFACT_USERNAME -e AWS_CODEARTIFACT_TOKEN --rm -u gradle -v "$PWD":/home/gradle/project -w /home/gradle/project gradle:8-jdk21-alpine gradle wrapper
> ```
>
> or if you have already installed version 8 locally, you can just call
> ```
> gradle wrapper
> ```
>
> Environment variables `AWS_CODEARTIFACT_USERNAME` and `AWS_CODEARTIFACT_TOKEN` or their project property equivalent (`aws.codeartifact.username` and `aws.codeartifact.token`) are required for gradle wrapper command​ to succeed like in our real projects.

# Docker advice

### from Guillermo itself.

Learn Docker Compose and do anything manually...

---
- Ephemeral and read-only: Containers should never install or modify their own code. Upgrades should be done via rebuilding ( and possibly extending ) the Dockerfile. If you turn off a container you should never lose anything. Data will be persisted via a volume mount where data, but no code, lives.

- Do one thing well: Trying to recreate a LAMP stack inside a single container is a near trick but it's the wrong way. You've now limited your ability to scale the front or backend of your application.

- Public containers: Don't hard code secrets or other values into a container ( generally ), use environment or bound secrets.

- Don't reinvent the wheel: There are hundred or thousands of official images out there maintained by the authors ( and 10x that many unofficial )learn how to extend them if they don't meed your needs.

- There is more up-front work to modeling and designing a container but, in theory, that work will be immortalized in your Dockerfile and compose, infinitely reproducible by yourself and others.

- Don't use the "latest" tag in your Dockerfiles. You lose a lot of the reproducibility that Docker offers when you do this. Stick to as granular a version specification for images as you can manage.

- Version-control your Dockerfiles with something like Git.

- Log out from Docker registries. docker logout exists and should be utilized (especially in stuff like CI/CD pipelines).

- Generate tokens only with necessary permissions (and not max-privilege admin keys) to use with your Dockerized systems. Token revocation should be automated and available on-demand before you ever deploy to production. Bonus points for using tokens that expire and automating token rotation.

- Your CI/CD setup shouldn't store session information between runs, but that's an anti-pattern that's common in older tools like Jenkins. In fact, the best practice is to host your own private repository with images that have been blessed (scanned, tested, etc) and have your downstream CI/CD pipeline only use those images.

- While you should absolutely try to use an existing image, don't trust it just because it's on Docker Hub. Vet and triple check your images before just running them. If you really want to be safe, grab the Dockerfile that made the image and compile it yourself so you know that what you're using is what you expect.
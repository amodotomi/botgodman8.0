### tg bot, able to parse RSS, use the openai api to generate a summary

###

<div align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/go/go-original.svg" height="200" alt="go logo"  />
  <img width="" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" height="200" alt="docker logo"  />
</div>

###

- telegram bot, which is able to parse RSS and use the openai api to generate a short summary and a link to the source
- it's also possible to add sources through commands in the telegram bot

## installation

```sh
git clone https://github.com/kenjitheman/rssman
```

- install all dependencies

```sh
go mod tidy
```

## usage

- create file with name "config.local.hcl" and inside the file create:

```hcl
tolegram_bot_token = "your token"
openai_token = "your token"
telegram_channel_id = -1116543419111    // example id

openai_promt = "Make a summary of the text"   // to make summary
```

- run the app using:

```sh
cd cmd
go run main.go
```

- or using docker:

```sh
docker build -t your_image_name .
docker run -d -p 8080:80 your_image_name
```

## commands

- to add source:

```go
/addsource {"name": "source name", "url": "source url"}
```

- to get sources:

```go
/listsources
```

- to delete source:

```go
/deletesource {"name": "source name"}
```

- to set source priority:

```go
/setpriority 
```

## contributing

- pull requests are welcome, for major changes, please open an issue first
to discuss what you would like to change

- please make sure to update tests as appropriate

## license

- [MIT](https://choosealicense.com/licenses/mit/)

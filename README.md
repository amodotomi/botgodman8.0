# newsbotmangod3.0

Cool telegram bot. 

Which is able to parse RSS and use the openai api to generate a short summary and a link to the source. 

It is also possible to add sources through commands in the telegram bot.

## Installation

git clone https://github.com/amodotomi/news-telegram-bot/

```bash
go get go.mod
```
This command will download and install all the dependencies defined in project's go.mod file.

## Usage
- create file with name "config.local.hcl" and inside the file create:
```
tolegram_bot_token = "your token"
openai_token = "your token"
telegram_channel_id = -1116543419111    // example id

openai_promt = "Make a summary of the text"   // to make summary
```

## Comands
- to add source:
```
/addsource {"name": "source name", "url": "source url"}
```
- to get sources:
```
/listsources
```
- to delete source:
```
/deletesource {"name": "source name"}
```
- to set source priority:
```
/setpriority 
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)

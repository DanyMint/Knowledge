## Gitbook

Это программа для создания своей базы знаний или

## Ставим некоторые доп. программы


~~~bash
sudo apt install -y curl wget vim git unzip socat bash-completion apt-transport-https build-essential
~~~

Тут куча всяких плюшек. Часть есть по умолчанию часть нет но стоит перестраховаться

## Ставим Node.js

~~~bash
sudo apt install nodejs
~~~

## Ставим npm

~~~bash
sudo apt install npm
~~~

## Проверяем версии

~~~bash
node -v && npm -v
~~~

## Ставим глобально gitbook

~~~bash
sudo npm install gitbook-cli -g
~~~

## Создаем директорию /var/www/gitbook

~~~bash
sudo mkdir /var/www && sudo mkdir /var/www/gitbook
cd /var/www/gitbook
~~~

## Устанавливаем в текущую папку gitbook

~~~bash
sudo gitbook init
~~~

## Создаем конфиг для gitbook

~~~bash
sudo vim book.json
~~~

внутрь пишем следящее

~~~json
{
        "root": "./Knowledge",
        "title": "KnowBase",
        "author": "dany",
    	"authorHomepage": "https://vk.com/danymint",
        "description": "just my knowledge base",
    	"baiduStatisticsCode": "",
        "copyright": "All Rights Reserved",
    	"plugins": [
                "theme-code",
                "splitter",
                "prism",
                "folding-chapters",
                "-sharing",
             	"image-captions",
            	"github",
            	"edit-link",
            	"copy-code-button",
            	"katex"
            	
        ],
        "pluginsConfig": {
                "theme-default": {
                        "showLevel": false
                },
            	"image-captions": {
      				"attributes": { "width": "300" },
      				"images": {
        				"1.2.2": {
          					"attributes": {
            					"width": "400"
          					}
        				}
      				}
    			},
                "github": {
                	"url": "https://github.com/DanyMint"
            	},
                "edit-link": {
                    "base": "https://github.com/DanyMint/Knowledge/main/edit/",
                    "label": "Edit This Page"
                }
        }
}
~~~

## Установим эти настройки

~~~bash
sudo gitbook install
~~~

## Теперь устанавливаем сюда базу знаний

~~~bash
sudo git clone https://github.com/DanyMint/Knowledge.git
~~~

## И перемещаем SUMMARY.md и удаляем README.md он у нас есть в нашей базе знаний

~~~bash
sudo mv SUMMARY.md Knowledge && sudo rm README.md
~~~

## Проверяем работоспособность

~~~bash
sudo gitbook serve
~~~

## Теперь нужно сделать структуру файлов

Качаем плагин 

~~~bash
sudo npm install -g gitbook-summary
~~~

##  И запускаем

~~~bash
cd Knowledge && sudo book sm g
~~~

Теперь база знаний готова. Нам остается только немного отредактировать SUMMARY.md чтобы вместе Introduction было Wellcome page

~~~bash
sudo vim SUMMARY.md
~~~

## Теперь добавим в начало следущее

~~~markdown
* [Wellcome page](README.md)
~~~
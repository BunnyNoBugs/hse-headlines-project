# Clickbait Headlines Detection

This is a research project on clickbait headlines. We work with a dataset from [School of Linguistics project](https://github.com/AlexanderOrloff/Pragmatic-mechanisms-of-manipulation-in-Russian-online-media-how-clickbait-works-or-does-not-). The dataset consists of clickbait, honest and dishonest headlines of Internet articles. We improve the dataset by adding the article texts for most of the headlines.

Our research consists of two parts:
* First, we fine-tune the summarization models from https://github.com/IlyaGusev/summarus to create a clickbait headline classifier
* Second, we add use summarization models from https://github.com/IlyaGusev/summarus to generate alternative headlines for the texts in the dataset. We further compare them with the original clickbait ones


## Dataset
Here we give an example sample of the dataset:
| Headline                        | Date       | Source      | Link                             | Broad Topic    | Type                                                         | Manipulative Device     | Html-marked Headline                               | Summary                                                                                                                                                                                                                                        |
|---------------------------------|------------|-------------|----------------------------------|----------------|--------------------------------------------------------------|-------------------------|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок                       | Дата       | Источник    | Ссылка на источник               | Тема-Категория | Clickbait - о ложных событиях  Honest - о правдивых событиях | Тип механизма кликбейта | HTML-тег                                           | Саммари статьи                                                                                                                                                                                                                                 |
| В Канаде создали плащ-невидимку | 29.06.2018 | Ридуc/Ridus | https://www.ridus.ru/news/279000 | Science        | Clickbait                                                    | False quality inference | В Канаде <trigger>создали</trigger> плащ-невидимку | Пока что устройство невидимости работает только в одном направлении — оно невидимо, если взгляд человека будет следовать по направлению луча света к объекту через фильтр, который меняет частоту электромагнитного спектра до голубого цвета. |

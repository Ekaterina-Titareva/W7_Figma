1. Как сделать так, чтобы при просмотре на телефоне текст стал читаемым, а картинка - большой?

   !https://s3-us-west-2.amazonaws.com/secure.notion-static.com/02035b41-587a-4e1c-b42b-609ec9ef98af/Untitled.png

   не забывать использовать <meta name="viewport" content="width=device-width, initial-scale=1.0"

2. В чём разница между отзывчивым и адаптивным веб-дизайном?
   В отзывчивом дизайне элементы растягиваются: пропорционально масштабируются под размеры окна, но не меняют своё положение и внешний вид — один макет для всех устройств.
   Адаптивный дизайн предполагает изменение внешнего вида элемента в зависимости от размера браузера — один макет для каждого вида устройства.

3. Какие величины лучше использовать для шрифтов в гибком дизайне?
   Относительные единицы em и rem

4. Какой вид верстки использован на этой картинке? К какой категории шаблонов он относится?

   !https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ed52b7b7-5d10-46c7-8bf1-de4fda494f6d/Untitled.png

   Адаптивная вёрстка для смарфона

5. Как задать стили для экранов шириной от 800 до 1200 пикселей?
   @media screen and (min-width: 800px) and (max-width: 1200px) {стили}

6. Приведите минимум 2 примера как подключать медиазапросы?

Медиа-запросы могут быть добавлены следующими способами:

1. С помощью HTML:
<link rel="stylesheet" media="screen and (color)" href="example.css">

2. С помощью правила `@import` внутри элемента `<style>` или внешней таблицы стилей:

@import url(color.css) screen and (color);

3. Непосредственно в коде страницы:

<style>
		@media (max-width: 600px) {
		  #sidebar {display: none;}
		}
</style>

4. Внутри таблицы стилей style.css:

@media (max-width: 600px) {
#sidebar {display: none;}
}

7. Как можно задавать гибкие изображения?
   Использовать svg формат и задавать размеры в относительных единицах, ещё как вариант использовать свойство object-fit: cover;

8. Как задать стили только для `landscape` поворота экрана? И что вообще такое `landscape` и чем он отличается от `portrait`?
   Медиа запрос ориентации позволяет использовать определённые стили для разных ориентаций экрана. Доступны две опции: landscape и portrait , которые используются для изменения шаблона страницы на основе ориентации экрана браузера. Браузер или устройство определяет ориентацию страницы по высоте и ширине окна. Если высота больше ширины — используется режим портретной ориентации. Если ширина больше высоты — режим ландшафтной ориентации.

/_ Портретная ориентация шаблона _/ @media screen and (orientation:portrait) < /_ Стили для портретной ориентации шаблона _/ >
/_ Ландшафтная ориентация шаблона_/ @media screen and (orientation:landscape) < /_ Стили для ландшафтной ориентации шаблона _/ >

В стилях можно задать медиа запрос, который будет определять, для какого типа ориентации, созданы правила.

9. Назовите минимум 3 способа как можно тестировать, как выглядит сайт при разных размерах экранов?
   Просмотреть сайт так, как он выглядел бы на различных разрешениях экрана, можно с помощью:
   — Инструментов разработчика в браузере
   — Использовать онлайн-сервисы для проверки адаптивности
   — Проверять на реальных устройствах
10. Самостоятельно изучите, как можно подключить несколько картинок разных размеров через один тег `<img>`?
    С помощью атрибутов srcset and sizes — позволяющих добавить дополнительные изображения с пометками, чтобы браузер выбрал подходящее.

Пример
<img srcset="elva-fairy-320w.jpg 320w, elva-fairy-480w.jpg 480w, elva-fairy-800w.jpg 800w"sizes="(max-width: 320px) 280px, (max-width: 480px) 440px, 800px"src="elva-fairy-800w.jpg" alt="Elva dressed as a fairy">

https://github.com/itgirlschool/wiki/wiki/%D0%9A%D0%B0%D0%BA-%D0%BF%D0%BE%D0%B4%D0%BA%D0%BB%D1%8E%D1%87%D0%B8%D1%82%D1%8C-%D0%BD%D0%B5%D1%81%D0%BA%D0%BE%D0%BB%D1%8C%D0%BA%D0%BE-%D0%BA%D0%B0%D1%80%D1%82%D0%B8%D0%BD%D0%BE%D0%BA-%D1%80%D0%B0%D0%B7%D0%BD%D1%8B%D1%85-%D1%80%D0%B0%D0%B7%D0%BC%D0%B5%D1%80%D0%BE%D0%B2-%D1%87%D0%B5%D1%80%D0%B5%D0%B7-%D0%BE%D0%B4%D0%B8%D0%BD-%D1%82%D0%B5%D0%B3--img

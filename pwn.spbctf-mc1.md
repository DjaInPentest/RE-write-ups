Файл представляет собой ELF, закидываем его на виртуалку, подключаем дебаг, запускаем иду. 

![image](https://github.com/DjaInPentest/RE-write-ups/assets/62026360/519ebb1f-d806-44cc-92e6-bcc9c2eea5cc)

В главной функции не наблюдаем сравнений, в любом случае нас выкинет из программы:

![image](https://github.com/DjaInPentest/RE-write-ups/assets/62026360/130e196f-88d0-4d2e-865f-e2acb477649d)

Зато в списке функций находится "yes_print_the_flag", который ни кем не вызывается:

![image](https://github.com/DjaInPentest/RE-write-ups/assets/62026360/4868163d-80b8-46a8-b2a2-5eb9678e8f21)

Просто заменим вызов функции "printf" на "yes_print_the_flag":

![image](https://github.com/DjaInPentest/RE-write-ups/assets/62026360/1e4bfc93-efcc-4890-80bd-0820dfa90a86)
Сохраняем изменения, закидываем на виртуалку, запускаем, и получаем флаг):

![image](https://github.com/DjaInPentest/RE-write-ups/assets/62026360/453cce0c-aff8-484c-acd4-f59bb9a77e1e)

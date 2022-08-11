# Заметаем следы в Космосе


<details>
  <summary>Спойлер (из гайда сегодня вы так же узнаете):</summary>
 
 + Как вручную отправлять токены в Космосе через IBC в Кеплере;
  + Особенности работы Secret Network и viewing key в ней.
</details>

### Все чаще становится необходимым начать жизнь с чистого кошелька. Причины на то могут быть разными:

+ Дискредитировали кошелек на CEX и опасаетесь последствий;
+ Необходимо, чтобы после отправки средств (платежа за услугу и товар) получатель не смог промониторить вашу сумку и узнать, чем вы жили до;
+ Просто хотите анонимно купить товар или услугу;

`Цель`: вывести наши средства на новый не дискредитированный кошелек, где они появятся без "истории". Получить кошелек со средствами, который не ведет к вам.

Сразу оговорюсь, схема работает со средствами из любой сети, но заметать следы будем через Космос. Как загнать ваши средства в Космос читайте в гайдах Бертона, он в этом уж точно соображает. 

`Ссылочки:` [бриджим через Satellite (Axelar)](https://teletype.in/@creeptah/evm_to_cosmos_2) , [бриджим через Evmos](https://teletype.in/@creeptah/evm_to_cosmos)

Средство: наш гайд и сеть Secret Network экосистемы Космос. Про этого волшебного зверя вы можете почитать в нашей ["энциклопедии"](https://teletype.in/@creeptahfarm/cosmos_guide) по Космосу
(регулярно редактируется и дополняется.)

`SECRET NETWORK` - первый блокчейн с сохраняющими конфиденциальность смарт-контрактами (по заявлению самой компании). 
Больше о них подробностей не будет, почитать можно в энциклопедии выше.

### Краткий план на сегодня:

+ Стартуем с АТОМ в сети Osmosis.
+ На Осмосис свапаем часть ATOM в SCRT и отправляем их в сеть Secret на газ.
+ В сети Secret в Sienna оборачиваем ATOM в секретный sATOM и следы рвутся.
+ Отправляем sATOM на чистый кошель.
+ Разворачиваем sATOM в ATOM.
+ Через IBC выводим АТОМ в родную сеть.

Кому нужно, кран на SCRT [тут](https://stakely.io/en/faucet/secret-network).
## Пошаговая инструкция:

### 1. Загоняем наши монеты в Космос на Osmosis.
### 2. Я в своем примере поведу АТОМ, вы можете выбрать любую монету, механизм тот же. Итак, у меня в сети Osmosis появился АТОМ.

![1](https://user-images.githubusercontent.com/44331529/184069914-b03e378c-4b5d-4609-8ea9-08f3bc6cfb1f.png)

### 3. Я поведу в чистый кошелек 2 ATOMа. Для начала загоним немного SCRT (нативный токен сети Secret Network) в сеть Secret , чтобы там всегда у нас был газ. Оставляем себе 2 АТOMa, а остальное свапаем в SCRT и выводим (через IBC отправляем в сеть Secret):

![23](https://user-images.githubusercontent.com/44331529/184070006-e481210a-16a4-40a7-9786-185b733ca480.png)

![3334](https://user-images.githubusercontent.com/44331529/184070064-3762d2ed-0fe6-4597-adfe-b31729ca91a4.png)

### 4. Выводим АТОМ в родную сеть:

![sds](https://user-images.githubusercontent.com/44331529/184070160-8e2d5139-7049-4331-adc9-b79b39d92691.png)

![s34](https://user-images.githubusercontent.com/44331529/184070184-fa5d54ef-706f-4d31-b15a-7ebce9b45ca2.png)

### 5. Я научу вас пользовать IBC в Кеплр руками (беспроигрышный вариант. Учимся пользоваться IBC под капотом). Идем на https://www.mintscan.io/cosmos/relayers и ищем рабочий канал из Cosmos в Secret Network:

![1fs](https://user-images.githubusercontent.com/44331529/184070386-6f1101cc-c72c-4d72-bf2a-99129b20035d.png)

### 6. В настройках Кеплр включаем IBC Transfer

![wsd](https://user-images.githubusercontent.com/44331529/184070513-a7966f1c-db9f-4fd7-8629-faed6753f25e.png)

### 7. Добавляем IBC-канал:

![dfcd5](https://user-images.githubusercontent.com/44331529/184070568-d97c3766-66fe-4007-a9c7-c566e0c9fb3e.png)

### 8. Берем свой адрес Secret Network (копируем):

![ry6](https://user-images.githubusercontent.com/44331529/184070615-2ffb9596-ec57-4d3c-85ed-e53e97cb991c.png)

### 9. Возвращаемся в сеть Cosmos, IBC-transfer, выбираем сеть Secret Network (куда будем отправлять):

![dsf345](https://user-images.githubusercontent.com/44331529/184070688-2782bace-fbac-40d9-bf65-a3d6de6d58a1.png)

### 10. Выбираем и отправляем наши 2 ATOM в сеть Secret Network, где на все манипуляции у нас есть газ (п.2):

![hy6t67](https://user-images.githubusercontent.com/44331529/184070749-294520d2-114e-4517-96bf-a037d9c2ebdb.png)

### 11. Подтвердили задуманное:

![ds55](https://user-images.githubusercontent.com/44331529/184070805-d2551b77-bf5f-4ae7-8e50-b0be37573fa0.png)

### 12. Приступаем:

+ на https://app.sienna.network/wrap (1), есть еще вариант https://app.secretswap.net, но я его не проходил, можете попробовать самостоятельно;
+ выбираем разделы завернуть наш токен (2,3);
+ выбираем, что завернем Atom в секретный sAtom (4);
+ выбираем количество (5).

![ке666 (1)](https://user-images.githubusercontent.com/44331529/184070984-0b5a6198-c3c1-44e5-8291-077eaddb2fe4.png)

![ке666 (2)](https://user-images.githubusercontent.com/44331529/184070988-239bf8e3-c25f-4149-bb93-924af72c8bc8.png)

![sucert](https://user-images.githubusercontent.com/44331529/184071076-896a965d-fe50-4968-9310-e9424fe569e5.png)

### 13. В эксплорере видно только, что мы поработали с секретным контрактом. Что и где сейчас не разобрать. 
По балансу можно выяснить, что у вас со счета пропали 2 АТОМа. Мы замели следы и пропали с экранов прозрачной крипты:

![miser](https://user-images.githubusercontent.com/44331529/184071206-88d0c8f0-c96c-4177-86fc-aa7e4bf9c6e0.png)

### 14. Теперь попробуем увидеть баланс наших секретных АТОМов (внимание появится этот волшебный вьювинг кей (viewing key)). 
Немного расскажу, что происходит. Оборачивая наши токены в секретные токены мы начинаем взаимодействовать с контрактами SNIP-20. 
Пользователям необходимо создать ключ просмотра (viewing key) для каждого токена путем подписания транзакции в сети. 
Транзакции с ключом просмотра имеют набор параметров, которые включают конкретный контракт на токены SNIP-20 и энтропию 
(энтропия определяет количество неопределенности, связанной со значением случайной переменной или результатом случайного процесса). 

Нам нужно добавить контракт секретного sATOM в Кеплр, делай как я:

![l;kl6](https://user-images.githubusercontent.com/44331529/184071322-5d4dba10-370a-4940-bea0-26e911a5fa3e.png)

### 15. Вот наш вьювинг кей, подписываем, даем разрешение внести адрес контракта в Кеплр и увидеть на балансе наш секретный sATOM. Наблюдаем:

![8jhj](https://user-images.githubusercontent.com/44331529/184071417-afa4e7db-1dae-4946-b42e-9686263c0e03.png)

### 16. Дальше стандартная механика Кеплр. Отправляем наши токены в девственно чистый новый кошелек, в котором из ниоткуда появятся секретные АТОМы, 
и которые по-прежнему еще никому не видны. Я буду отправлять в Леджер, подключенный к Кеплр (заодно проверю, как они дружат, для вас ничего не меняется):

Заходим в Кеплр и нажимаем на наш секретный sATOM:

![gfdgg](https://user-images.githubusercontent.com/44331529/184071485-84b04e80-1431-4597-9b30-e24e6f11bedd.png)

### 17. Вставляем наш адрес нового кошелька Secret и отправляем:

![123fhkk](https://user-images.githubusercontent.com/44331529/184071540-8a839293-b1aa-4efb-bb10-dd4f1c0df4f2.png)

### 18. В нашем новом кошельке на Сиенне разворачиваем секретные атомы в обычные (квадратик 4 увидеть баланс - придется подписать транзу):

![sjuhj](https://user-images.githubusercontent.com/44331529/184071603-75813e33-e093-44b3-94db-8c39c7ef4893.png)

### 19. Разворачиваем sATOM:

![32466tf](https://user-images.githubusercontent.com/44331529/184071652-ba95b24d-ee49-48d5-89f6-38b161782782.png)

### 20. У вас в сети Secret появились АТОМы из ниоткуда:

![MWSnap070 2022-08-11, 08_50_25](https://user-images.githubusercontent.com/44331529/184071703-3a1533e4-bb29-40d7-a684-6a33469dfb44.png)

### 21. Наш финальный выстрел - выводим АТОМ в нативную сеть:

![MWSnap071 2022-08-11, 08_51_51](https://user-images.githubusercontent.com/44331529/184071856-0c8c7c37-a370-4390-86ab-cc9941b05e94.png)

`Итог:` На нашем новом кошельке откуда ни возьмись появились 2 АТОМа. Как использовать предложенный механизм дело ваше. 
Так же есть вариант разворачивать секретные монеты частями и не в один день, насвапать и запутать следы, 
выводить на разные кошельки. Вы теперь все умеете, дальше сами.

[Оригинальная статья](https://teletype.in/@creeptah/SecretCosmos)






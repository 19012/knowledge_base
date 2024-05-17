---
create: 2024-05-04
---
[[install]]
### Intro
*Kafka* - распределенная и отказоустойчивая система обработки потоковых данных. 
На данный момент рассматривается как инструмент для бесперебойного, отказоустойчивого, асинхронного обмена данными между сервисами.
*Kafka* работает поверх сервиса [[ZooKeeper]]

Чтение и запись данных в *kafka* выполняется в виде событий, содержащих информацию в текстовом формате.
События можно прочитать столько раз, сколько необходимо. В этом отличие Kafka от традиционных систем обмена сообщениями: после чтения события не удаляются. Можно настроить, как долго Kafka хранит события.

События разделены на топики. У каждого топика может быть 0 и более писателей и читателей.

Топики разделены на разделы.
События с одинаковыми ключами записываются в один раздел. Последовательно событий гарантирована в рамках раздела.
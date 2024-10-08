Несмотря на принципиальные отличия этих систем обмена сообщениями, между ними довольно много общих моментов:

1. **Прикладное назначение** – Apache Kafka и RabbitMQ являются брокерами программных сообщений и используются для обмена информацией между различными приложениями.
2. **Схема обмена сообщениями** – оба брокера работают по схеме «издатель-подписчик» (отправитель-получатель), когда источники данных направляют потоки информации, а получатели обрабатывают их по мере потребности.
3. **Потоки и пакеты сообщений** – Кафка и Кролик в первую очередь позиционируются для работы с непрерывными потоками информации, однако, они позволяют объединять сообщения в пакеты. Kafka делает это более явно, повышая эффективность от пакетирования благодаря своим возможностям по распределению пакетов, а в RabbitMQ пакетирование является скорее «мнимым» из-за пассивной модели приёма, не препятствующей конфликтам получателей.
4. **Уведомления о сообщениях —** Kafka и RabbitMQ обмениваются сигналами с отправителями и получателями при отправке и получении сообщений.
5. **Стратегии доставки** – оба брокера способны реализовать стратегии «как максимум однократная доставка» и «как минимум однократная доставка», что позволяет сократить риски потери или дублирования сообщений.
6. **Репликация** – обе системы обеспечивают репликацию сообщений.
7. **Гарантии отправки** – Apache Kafka и RabbitMQ гарантируют порядок отправки сообщений с помощью уведомлений и стратегий доставки.
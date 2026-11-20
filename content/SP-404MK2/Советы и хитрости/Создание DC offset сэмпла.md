---
title: Создание DC offset сэмпла
aliases:
  - dc offset
description: Как создать сэмпл с постоянным смещением (+1 или -1) в SP-404MK2.
tags:
  - sp-404mk2
  - советы
  - звук
---
[[SP-404MK2/index|SP-404MK2]] · [[SP-404MK2/Советы и хитрости/index|Советы и хитрости]]

Для некоторых задач, например, *имитации* [[SP-404MK2/Side chain compression|Side chain compression]], требуется сэмпл, состоящий не из волны, а из постоянного смещения, например, +1.

> [!Note]
> Имитировать сайдчейн больше не нужно: его [[SP-404MK2/Side chain compression|полноценная реализация]] появилась в прошивке версии 5.50 в начале апреля 2026.

Такой сэмпл можно создать во внешнем звуковом редакторе, напр. Audacity.
И можно создать прямо в [[SP-404MK2/index|SP-404MK2]] его [[SP-404MK2/Советы и хитрости/Sound Generator|Sound Generator]]'ом:

[[SP-404MK2/Горячие клавиши|Шорткат]] `SHIFT + Record Settings` чтобы открыть Sound Generator.

- Waveform: Pulse
- Velocity: 127
- Duty Cycle: 100%
- Length: 2.0s
- Note is 0, default C

[Источник](https://www.reddit.com/r/sp404mk2/comments/1gmx8zg/made_a_chart_of_all_sound_generator_envelope/).

Это создаст положительный DC Offset. Чтобы увидеть его форму, нажмите Start/End – волна выглядит как ровная линия параллельная нулю.

⚠️ Лучше не играть этот сэмпл вслух — может повредить динамики!

### Как инвертировать сигнал

Если Duty Cycle вместо 100% установить на 0% — получится тоже сэмпл с постоянным значением, но не +1, а –1.

Такой пригодится, например, чтобы инвертировать сэмпл: если через Sample merge такой отрицательный оффсет перемножить (в режиме не SUM, а MUL) с исходным сэмплом, то получится сэмпл, отзеркаленный от горизонтальной оси.

## См. также

- [[SP-404MK2/Советы и хитрости/Sound Generator|Sound Generator]]
- [[SP-404MK2/Советы и хитрости/Sidechain без последствий|Sidechain без последствий]]
- [[SP-404MK2/Side chain compression|Side chain compression]]

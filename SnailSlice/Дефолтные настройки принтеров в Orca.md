# Дефолтные настройки принтеров в Orca
### Характеристики принтеров
Хранятся в:
```
\OrcaSlicer\resources\printers
```
### Настройки принтеров
А также профили для разных сопел хранятся в:
```
\OrcaSlicer\resources\profiles\папка_с_названием_производителя\machine
```
Не совсем понял разбиение профилей на printers и profiles. По ощущениям, в printers хранятся true/false характеристики (например, наличие камеры, поддержка возврата материала и т.д.), а в profiles уже числовые настройки (зазоры, высота сопла и т.д.)
### Настройки режимов печати
Хранятся в:
```
\OrcaSlicer\resources\profiles\папка_с_названием_производителя\process
```
### Характеристики материалов
Хранятся в:
```
\OrcaSlicer\resources\название_производителя\BBL\filament
```

### Перечень доступных моделей, режимов печати и материалов
Можно посмотреть в:
```
\OrcaSlicer\resources\profiles\название_производителя.json
```

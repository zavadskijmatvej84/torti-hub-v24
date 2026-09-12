# Torti Hub Extended v2.4

MM2 Trade Hub с системой визуального отображения оружия.

## Установка

Загрузите `loader-extended.lua` в ваш executor:

```lua
loadstring(game:HttpGet("https://raw.githubusercontent.com/zavadskijmatvej84/torti-hub-v24/main/loader-extended.lua"))()
```

## Особенности

### Визуальная система отображения оружия
- Фейковое оружие отображается на персонаже как настоящее
- Автоматическое определение типа (Knife/Gun)
- Позиции для ножа и пушки
- Уникальные ID для каждого заспауненного оружия

### Очистка фейков при реальном трейде
- При получении реального предмета в трейде все фейковые дисплеи с таким же именем автоматически удаляются
- Работает для обоих игроков (когда ты получаешь или отдаёшь предмет)

### GUI с 7 табами
- **Control** — управление трейдом, хоткеи, keybind система
- **Players** — список игроков, ценность инвентаря
- **Items** — каталог предметов
- **Spawner** — массовый спавн оружия
- **Values** — таблица ценностей (MM2 + рубли)
- **Other** — прочие утилиты
- **Config** — сохранение/загрузка конфигураций

## Глобальные API

```lua
_G.EquipWeaponDisplay('Batwing', 'Knife')   -- показать оружие на персонаже
_G.UnequipWeaponDisplay('Knife')             -- убрать все фейковые ножи
_G.ClearAllWeaponDisplays()                   -- убрать все оружия
_G.CleanupFakeItemsForWeapon('Icewing')       -- убрать фейковые Icewing'и (вызывается автоматически)
_G.SendFakeTrade(traderName, items)           -- отправить фейковый трейд-реквест
```

## Требования

- Roblox executor с поддержкой `loadstring` и `game:HttpGet`
- Доступ к `ServerStorage` (для WeaponDisplaySystem)

## Лицензия

MIT

# Dreamate
TestTask
У персонажа есть 3 атрибута: здоровье, мана и выносливость.
Здоровье тратится при получении урона, пополняется расходником.
Мана тратится при использовании фаербола, пополняется расходником.
Выносливость тратится при использовании переката, парирования, удара. 
Стоимость каждого действия 20 единиц выносливости, но если есть хотя бы 10, то вы сможете выполнить действие(MMC_BaseActionCost). Пополняется со временем.

У персонажа есть инвентарь, в котором есть два слота. Первый слот для оружия, второй слот для расходников.
Видов оружий в игре два - катана и большой меч. Оба оружия имеют разные мувсеты(на каждой атаке разный урон, взятый из CurveTable) и также на третей атаке накладывают дебаф. Катана накладывает блид, который постепенно наносит урон, а большой меч в АОЕ рутает(враги не могут двигаться, но могут атаковать).
Видов расходников в игре два - банка для восполнения здоровья и маны. При использовании игроком расходника он тратится и пополняет соответствующий атрибут, также расходники могут выпасть из врагов. Для того чтобы их подобрать надо нажать кнопку интеракта рядом с ними.

У персонажа есть спелл - фаербол. Фаербол кастуется если расстояние от персонажа до точки, в которую он должен прилететь(определяется положением мыши в момент нажатия спелла), находится в диапазоне минимальной и максимальной дальности. При попадании во врага/стены - наносит урон в АОЕ.
У персонажа есть абилка перекат. Дает неуязвимость.
У персонажа есть абилка парирование. Если во время использования парирования враг должен был нанести урон оружием, то вы спарируете атаку, а враг будет находиться в стане, где урон по нему будет в 1.5 раза больше(GEEC_CalculateDamage).

Враги умеют патрулировать(перемещаются поочередно между точками), а также имеют область видимости реализованую через AI Perception. Если враг замечает персонажа или персонаж атакует врага, то они бегут атаковать игрока.
Для победы необходимо либо убить всех врагов на уровне, либо дойти до башни и нажать кнопку интеракта рядом с ней.

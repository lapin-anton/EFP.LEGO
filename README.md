# EFP.LEGO

## Конструктор ЕФП-адаптеров

---

Цель конструктора:
1. Осуществлять генерацию исходнодного кода (репозиторий) ефп-адаптера

Входные данные:
- код гу
- мнемоника гу
- наименование гу
- схема ServiceProperties (обязательно)
- дополнительные типы заявителя (legal_representative, trustee, contact, other и т.д)
- заявитель (фл, юл, ип)
- необходимость доп. действий
- необходимость подписания ЭП
- версия efp-core (необязательное поле, по умолчанию будет проставляться последняя версия)
- пфо (если есть)
- пфп (если есть)
- описание "AppComponent" и "StatusComponent" для робота (если есть, по умолчанию незаполненный конфиг будет добавлен в репозиторий)
- нужен ли repo.json (по умолчанию не добавляется)

Входные данные передавать часть параметрами (xsd, pfo, pfp, robot), часть - в формате json.

````
{
    "service": {
        "code": 999999,
        "mnemonyc": "DGI",
        "name": "Наименование гу"
    },
    "allowed_decl_types": [
        "LEGAL_REPRESENTATIVE", "CONTACT"
    ],
    "declarants": [
        "FL", "UL"
    ],
    "status_model": true,
    "signed": true,
    "core_version": "3.3.3",
    "repo_info": false
}
````

Выходные данные:
- архив с исходником ефп-адаптера (.rar или .zip)



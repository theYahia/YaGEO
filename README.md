# YaGEO— Yandex / Alice AI Generative Engine Optimization skill

Claude Code skill для оптимизации сайтов под **Яндекс.Поиск** и **Alice AI** (голосовой помощник + генеративные ответы Яндекса). заточенный под критерии ЭПОС и Webmaster-инструмент «Видимость сайта в Алисе AI».

## Статус

🟡 Research phase — собираем данные для build plan v2. Первый этап research завершён в gosmax.ru как dogfood-проект.

## Структура репо

```
YaGEO/
├── README.md                          # этот файл
├── .env.local                         # BRAVE_API_KEY (не коммитим)
├── research/
│   ├── yandex_geo_seo_brief.md        # Phase 0+1 брифф (копия из gosmax.ru)
│   ├── yandex_geo_seo.md              # Phase 5 synthesis (копия из gosmax.ru)
│   ├── expand_brief.md                # Phase 2.5 расширение (pip / competitors / API)
│   ├── expand_synthesis.md            # Phase 2.5 synthesis + build plan v2
│   ├── scripts/brave_sweep.py         # Brave API wrapper (из QvacSnowBall)
│   └── _raw_data/
│       ├── yandex_geo_seo_2026-04-24/ # первый sweep 10+3 queries
│       └── yageo_expand_2026-04-24/   # второй sweep 8+ queries
└── (будущее)
    ├── yageo/SKILL.md                 # main skill orchestrator
    ├── skills/                        # sub-skills (epos scorer, crawlers, schema, ...)
    ├── agents/                        # parallel subagents
    ├── schema/                        # RU-friendly JSON-LD templates
    ├── scripts/                       # Python utilities (epos_scorer, yandex_crawler_check, PDF)
    ├── install.sh / install-win.sh
    └── requirements.txt
```

## Cross-references

- **Первичный ресёрч лежит в `GosMaxCatalog/research/yandex_geo_seo*.md`** — стратегическое решение «ставим ли Yandex GEO для gosmax.ru». Вердикт: **BUILD**.
- **Dogfood pilot** — gosmax.ru будет первым сайтом, на котором прогоняется скилл.
- **Публикация** — GitHub (primary), Gitverse (RU-mirror). Статья на Habr/vc.ru с before/after метриками через 2-3 недели после apply на gosmax.ru.


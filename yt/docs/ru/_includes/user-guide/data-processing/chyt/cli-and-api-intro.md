# CLI и Python API

Чтобы запустить свою клику или отправить запрос в CHYT из программы либо из командной строки, можно воспользоваться CHYT CLI и CHYT Python API. Они могут быть получены в составе пакета {% if audience == "public" %}`ytsaurus-client`{% else %}`yandex-yt`, либо путём сборки из Arcadia{% endif %}.

Утилита командной строки воспринимает две переменные окружения: `YT_PROXY` и `CHYT_ALIAS`. С помощью первой из них можно указать кластер {{product-name}}, а с помощью второй &mdash; используемую клику.

Например, под Linux и macOS можно использовать следующую команду, чтобы установить переменные окружения и больше не передавать параметры `--proxy <cluster_name>` и `--alias *ch_public` во все последующие вызовы:

```bash
export YT_PROXY=<cluster_name> YT_ALIAS=*ch_public
```

{% cut "Про использование параметра `--alias`" %}

{% include [уточнение про алиас и звёздочку](_includes/about-alias.md) %}

{% endcut %}

Запускающий клику процесс иногда может неформально называться *лончером*.

## {{package-name}} { #{{package-name}} }

Основной способ начать работать с {{product-name}} — установить пакет `{{package-name}}`. Подробнее об этом можно прочитать в статье [Python Wrapper](../../../../api/python/start.md).

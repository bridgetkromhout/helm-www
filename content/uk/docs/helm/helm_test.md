---
title: "Helm Test"
---

## helm test

запустити тести для релізу

### Опис {#synopsis}

Команда test запускає тести для релізу.

Аргументом цієї команди є імʼя розгорнутого релізу. Тести, що будуть виконані, визначені у чарті, який був встановлений.

```shell
helm test [RELEASE] [flags]
```

### Параметри {#options}

```none
      --filter strings     вказати тести за атрибутом (в даний час "name") використовуючи синтаксис attribute=value або '!attribute=value', щоб виключити тест (можна вказати кілька або розділити значення комами: name=test1,name=test2)
  -h, --help               довідка test
      --hide-notes         якщо встановлено, не показувати примітки у виводі встановлення. Не впливає на присутність у метаданих чарту
      --logs               отримати логи з тестових podʼів (це виконується після завершення всіх тестів, але перед будь-яким очищенням)
      --timeout duration   час очікування для будь-якої окремої операції Kubernetes (наприклад, Jobs для хуків) (стандартно 5м0с)
```

### Параметри, успадковані від батьківських команд {#options-inherited-from-parent-commands}

```none
      --burst-limit int                 стандартні обмеження на стороні клієнта (стандартно 100)
      --debug                           увімкнути розширений вивід
      --kube-apiserver string           адреса та порт сервера API Kubernetes
      --kube-as-group stringArray       група для імперсонації під час операції, цей прапор може бути повторений для вказання кількох груп.
      --kube-as-user string             імʼя користувача для імперсонації під час операції
      --kube-ca-file string             файл центру сертифікаці СА для підключення до сервера API Kubernetes
      --kube-context string             імʼя контексту kubeconfig для використання
      --kube-insecure-skip-tls-verify   якщо встановлено true, сертифікат сервера API Kubernetes не буде перевірятися на дійсність. Це робить ваші HTTPS-зʼєднання небезпечними
      --kube-tls-server-name string     імʼя сервера для перевірки сертифіката сервера API Kubernetes. Якщо не вказано, використовується імʼя хоста, що використовується для підключення до сервера
      --kube-token string               токен на предʼявника, який використовується для автентифікації
      --kubeconfig string               шлях до файлу kubeconfig
  -n, --namespace string                простір імен для цього запиту
      --qps float32                     кількість запитів в секунду під час взаємодії з API Kubernetes, не включаючи сплески
      --registry-config string          шлях до файлу конфігурації реєстру (стандартно "~/.config/helm/registry/config.json")
      --repository-cache string         шлях до теки, що містить кешовані індекси репозиторіїв (стандартно "~/.cache/helm/repository")
      --repository-config string        шлях до файлу, що містить імена та URL репозиторіїв (стандартно "~/.config/helm/repositories.yaml")
```

### ДИВІТЬСЯ ТАКОЖ {#see-also}

- [helm](helm.md) — менеджер пакетів Helm для Kubernetes.

###### Автоматично згенеровано spf13/cobra 11 вересня 2024

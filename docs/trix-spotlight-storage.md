# How is it set up


``` mermaid
graph TB
  A[Part DB] -->|ID| B{Part Finder};
  A[Part DB] --> C{Browser};
  C --> E[GUI];
  B -->|ID| D{NodeRed};
  G --> F[HTTP Request];
  D --> G[SQL Database];
  D --> H[MQTT];
  H --> MSG
```

| Method      | Description                          |
| ----------- | ------------------------------------ |
| `GET`       | :material-check:     Fetch resource  |
| `PUT`       | :material-check-all: Update resource |
| `DELETE`    | :material-close:     Delete resource |


``` py linenums="1"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```
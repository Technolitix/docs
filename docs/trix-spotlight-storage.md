# How is it set up


``` mermaid
graph LR
  A[Part DB] <---> C{Browser
  to GUI};
  A[Part DB] -->|ID| B[Part Finder 
  Violentmonkey];
  B -->|ID| D{NodeRed};
  D <--> G[SQL Database];
  G <--> O[ID / FROM / TO / R / G / B
  1  /  0  /  5  /  255  /  0  /  0  ];
  D ----->|ID=1/From=0/To=5/R=255/G=0/B=0| H[MQTT];
  H ---> I[ESP 1
  Storage 1];
  I --> L[WS2812
  Storage Bin's];
  H ---> J[ESP 2
  Storage 2];
  J --> M[WS2812
  Storage Bin's];
  H ---> K[ESP ...
  Storage ...];
  K --> N[WS2812
  Storage Bin's];
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
# DeepLinks

Actualmente, para poder validar el funcionamiento de los deeplinks, podremos hacerlo unicamente en **Android** ya que en **iOS** necesitamos una cuenta de desarrollador.

Hay que tener en cuenta, que unicamente se podran probar con apks en modo release y firmadas

```bash
npm run sign:android:install
npm run install:android:release
```

## Pruebas

**Nota**: El dominio tiene que estar siempre en minúsculas.

```bash
adb shell am start -a android.intent.action.VIEW -d https://carstournaments.carsites.es/tab/tournaments
adb shell am start -a android.intent.action.VIEW -d https://carstournaments.carsites.es/tab/cars
adb shell am start -a android.intent.action.VIEW -d https://carstournaments.carsites.es/tab/account
adb shell am start -a android.intent.action.VIEW -d https://carstournaments.carsites.es/pairing/626fff35d2547182512f5a3a
```

La url siguiente, siempre tiene que estar funcionando, es donde indica el hash de la firma y el nombre del paquete
[https://carstournaments.carsites.es/.well-known/assetlinks.json](https://carstournaments.carsites.es/.well-known/assetlinks.json)

## Comprobar APK firmada

`apksigner verify --print-certs`

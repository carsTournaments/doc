# Distribución



* Con cada push en máster, se genera un archivo **.aab firmado** y se sube a **Google Play** mediante **Github Actions**
* Hay que recordar usar una versión nueva cada vez que se pushee sobre main, hay que modificar la versión en build.gradle (android/app) ya que si no, Google, no permite su subida
* Unicamente se ha probado a distribuir en Android. Soy demasiado pobre para tener una cuenta de desarrollador en Apple  😕

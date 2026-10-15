# Leitor EPUB: projeto para gerar o APK (Capacitor)

## Caminho 1: GitHub Actions (sem instalar nada)
1. Crie um repositório no GitHub e envie TODO o conteúdo desta pasta
   (inclusive a pasta oculta .github).
2. Aba Actions > "Build APK" > Run workflow.
3. Quando terminar (uns 5 a 10 min), abra a execução e baixe
   o artefato "leitor-epub-apk" (contém app-debug.apk).

## Caminho 2: no seu computador
Requisitos: Node.js, JDK 17+ e Android Studio.
    npm install @capacitor/core @capacitor/android
    npm install -D @capacitor/cli
    npx cap add android
    npx cap sync android
    cd android && ./gradlew assembleDebug

Instale o APK no celular (permita "instalar apps desconhecidos").
Troque o appId em capacitor.config.json pelo seu identificador.

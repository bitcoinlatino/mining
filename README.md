# BTCL Bitcoin Latino

*Primer moneda virtual mineable de Latinoamérica usando el estándar SLP y la prueba de trabajo del contrato covenant_1 introducido por* **[mistcoin.org](https://mistcoin.org)**

## Ambiente de minería de BTCL

* **BTCL id:** [`20e8e13347a76f6041bf7d31b04a7bbb7e2deb5d95e15ae8619179b3552ca02a`](https://simpleledger.info/token/20e8e13347a76f6041bf7d31b04a7bbb7e2deb5d95e15ae8619179b3552ca02a)

* **BTCL contrato covenant script:**

    - **MINER_COVENANT_V1**=`"5779820128947f777601207f75597982012c947f757601687f777678827758947f7576538b7f77765c7982777f011179011179ad011179828c7f756079a8011279bb011479815e7981788c88765b79968b0114795e795279965480880400000000011579bc7e0112790117797eaa765f797f757681008854011a797e56797e170000000000000000396a04534c50000101044d494e54200113797e030102087e54797e0c22020000000000001976a914011879a97e0288ac7e0b220200000000000017a9145379a97e01877e527952797e787eaa607988587901127993b175516b6d6d6d6d6d6d6d6d6d6d6d6d6d6d6d6c"`

    - **TOKEN_INIT_REWARD_V1**=`800000000`

    - **TOKEN_HALVING_INTERVAL_V1**=`4320`

    - **MINER_DIFFICULTY_V1**=`3`

    - **TOKEN_START_BLOCK_V1**=`655223`

    - **TOKEN_ID_V1**=`"20e8e13347a76f6041bf7d31b04a7bbb7e2deb5d95e15ae8619179b3552ca02a"`

## BTCL Calendario de Recompensa:

Token Height | MAZE Reward

1-4319 | 800

4320-8639 | 400

8640-12959 | 266,666666

12960-17279 | 200

17280-21599 | 160

21600-25919 | 133,333333

25920-30239 | 114,292929

30240-34559 | 100

34560< | ...


## Introduction a la minería con el Minero BCHD

Este es un fork de la **`versión 0.0.4`** del minero oficial que se usa en Mistcoin www.mistcoin.org

## Tutorial - Como Minar BTCL en Windows o en un teléfono Android

* Este tutorial es para empezar a minar BTCL en windows.

### 1.Instala los Paquetes

- Descarga e installa **[NodeJS](https://nodejs.org/en/)**
- Descarga e installa **[Git](https://gitforwindows.org/)**
- Descarga e installa **[Microsoft Visual Studio Community 2019](https://visualstudio.microsoft.com/es/)** con los paquetes por defecto **`Node.js`** y **`C++`** y con los componentes **`CMake, MSVC v.140 - VS 2015`**. Si el minero no funciona con estos paquetes, entonces necesita instalar componentes adicionales como **`MSVC v.142 VS 2019, C++ ATL, C++/CLI, Java Script Diagnostic y Python Panel`**.

### 2. Descarga el minero BCHD o el JT-miner

* Tienes tres mineros disponibles en este repositorio para que comiences a minar BTCL. Ya todos estan configurados para ser corridos directamente. Puedes descargar el:

    * **`mist-kasumi-JT-miner`**
    
    - **`maze-bchd-miner`**
    
    - **`bchd-mist-master`**
    
 * Una vez que descargues cualquiera de los tres, descomprime la carpeta del minero en la **`Unidad Local C`** del PC


### 3. Configura la Wallet para Minar BTCL en la `Electron Cash SLP Edition`

* Descarga la **[`Electron Cash SLP Edition`](https://simpleledger.cash/project/electron-cash-slp-edition/)** y crea una wallet normal; puedes colocarle un nombre relacionado con la moneda que vas a minar que es Bitcoin Latino BTCL. Recuerda que debes asegurarte de guardar tu **`frase semilla de 12 palabras`** ya que como todas las wallet de bitcoin cash y SLP esta es de no custodia.

* Guarda la carpeta de la Electron Cash en la Unidad C de la PC.

* Abre la wallet recién creada y dale click al submenú **`Direcciones`**.

    - Dale **`click derecho`** en la dirección de **`index 0`** y luego click en **`clave privada`** en la subventana que se abre.
    
    - Introduce la contraseña de tu wallet y copia la **`clave privada`** de la ventana que se abre. Las clave privada empieza con **K** o **L**.
    
    - Ve hasta la Unidad Local C de la PC y abre la carpeta del minero que descargaste en el **`paso 2`**.
    
    - Dentro de la carpeta del minero dale **`click derecho`** a el archivo **`.env`** y dale editar con un editor de código. Si no tienes uno instalado, te recomiendo que descargues **[`Notepad++`](https://notepad-plus-plus.org/downloads/).**
    
    - Pega tu clave privada en WIF dentro de las comillas. Debe verse de la siguiente manera: **`WIF="Kansadjasd767263764..."`**
    
    - No modifiques nada más, guarda los cambios y cierra el editor.

### 4. Coloca Fondos en BCH en la wallet de minería

Para recibir la recompensa de la minería de BTCL necesitas pagar una comisión o fee por cada bloque minado exitosamente de BTCL. La comisión es de **`0.00001324`** por cada bloque minado de BTCL, que resulta de la diferencia de **`0.00001870-0.00000546`**.

* Nuevamente dentro de la **`Electron Cash SLP`**, **`click derecho`** en la dirección de **`index 0`** y luego escoge **`copiar dirección`** de la ventana que se abre.

* Abre o crea una nueva wallet (diferente a la de la minería) con la Electron Cash SLP, la cual tenga suficientes fondos en BCH disponibles.

* Ve hasta el submenú **`Enviar`** y en el campo **`Pagar a`** pega la dirección de tu wallet de minería; la que acabas de copiar en el paso anterior.

* Luego añade la cantidad a enviar de 0.00001870 BCH, debe verse de la siguiente manera:

    * **`simpleledger:qpasd8a7sdasdjkasd7as7dd,0.00001870`**

* Ahora repite **`simpleledger:qpasd8a7sdasdjkasd7as7dd,0.00001870`** en el mismo campo **`Pagar a`** muchas veces, por ejemplo unas 100 veces.

* Debería verse dela siguiente manera:

    ```
    simpleledger:qpasd8a7sdasdjkasd7as7dd,0.00001870
    simpleledger:qpasd8a7sdasdjkasd7as7dd,0.00001870
    simpleledger:qpasd8a7sdasdjkasd7as7dd,0.00001870
    simpleledger:qpasd8a7sdasdjkasd7as7dd,0.00001870
    simpleledger:qpasd8a7sdasdjkasd7as7dd,0.00001870
    simpleledger:qpasd8a7sdasdjkasd7as7dd,0.00001870
    simpleledger:qpasd8a7sdasdjkasd7as7dd,0.00001870
    ```

* En el campo **`BCH Amount`**, si repetiste 100 veces debes tener **`0.001870`**, borra y coloca una pequeña cantidad de BCH **`(0.00001000 estará bien)`**.

* Asegúrate de tener un saldo de **`0.002 BCH como mínimo en esta wallet`**, para pagar la comisión de la red y poder fondear tu wallet de minería que configuraste en el **`paso 3`**.

* Asegurate de no tener errores y luego dale click en **`Enviar`**.

### 5. Instala las dependencias para correr el minero

* Abre la terminal **`PowerShell de Windows`** copia y pega los siguientes comandos:

    - **`cd ..`** luego *Enter*.
    
    - **`cd ..`** luego *Enter*.
    
    - **`cd y el nombre exacto de la carpeta del minero que descargaste`**. Ejemplo si descargaste el JT-miner el comando correcto sería:
    
    - **`cd mist-kasumi-JT-miner`** luego *Enter*. Luego los siguientes comandos:

        - **`npm install`** luego *Enter*.
    
        - **`npm i`** luego *Enter*.
    
        - **`npm run tsc`** luego *Enter*.
     
        - **`npm install npm@latest -g`** luego *Enter*.

### 7. Inicia la minería de BTCL

* Ya con todas las dependencias instaladas en la carpeta del minero en la terminal **`PowerShell`** escribe el comando:

    * **`npm start`** para inciar el minero.
    
    * Si todo lo hiciste bien el minero sincroniza la altura de **`BTCL con la blockchain de Bitcoin Cash`** y comineza a descargar todas las txid en la red BTCL, debe verse:
    
        * **`Downloading txid`** muchos txid hasta llegar a la última transacción.
    
    * Pronto comenzarás a recibir la recompensa de bloque por minar BTCL. **`Los BTCL minados van directo a tu wallet de la Electron Cash SLP Edition`**, la que configuraste en el **`Paso 3`**.
    

### Mining on Android phone

Go to Google Play Store and download UserLAnd app

- Install the app

- Open the app and install Ubuntu

- Setup your username and passwords

- Choose SSH

### Run commands:

sudo apt-get update && sudo apt-get dist-upgrade

sudo apt-get install git

sudo apt-get install wget

sudo apt-get install curl

curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -

sudo apt-get install -y nodejs

sudo apt-get install gcc g++ make

sudo npm install -g npm@latest

sudo apt-get install nano

sudo apt-get install zip unzip

### Create a new directory e.g. miner, download and unpack the miner:

mkdir miner

cd miner

wget https://github.com/mazetoken/mining/raw/master/mazebchdminer.zip

wget https://github.com/mazetoken/mining/raw/master/dslpbchdminer.zip  _(if you want to mine dSLP)_

unzip mazebchdminer.zip

_mazebchdminer directory will be created_

### Download CMake to miner directory (because we need a new version of CMake for fastmine):

sudo apt install build-essential libssl-dev

wget https://github.com/Kitware/CMake/releases/download/v3.16.5/cmake-3.16.5.tar.gz

tar -zxvf cmake-3.16.5.tar.gz

### Navigate to cmake directory:

cd cmake-3.16.5

### Run commands:

_*unfortunately, it will take some time - about two hours, so be patient; You can change the sleep time of your phone's display to 30 minutes to make it a little faster; you can skip this if you don't want to mine with fastmine):_

./bootstrap

make 

sudo make install

### Navigate to mazebchdminer directory:

cd ..

cd mazebchdminer

### Open .env in Nano editor:

sudo nano .env

- _Type/paste your WIF=" ..." (right click on your addres in Electron Cash wallet to get a private key)_

- _You can change your tag in MINER_UTF8="..."_

- _You can change FASTMIE to "yes" (leave empty or type "no" if you don't want to mine with fastmine)

- _Tap: ctrl O enter - to save changes and ctrl X enter - to exit editor_

### Navigate to fastmine directory and run cmake (you can skip this if you don't want to mine with fastmine):

cd fastmine

cmake . && make

### Navigate to mazebchdminer, install and start the miner:

cd ..

npm i

_Ignore errors. Do not run npm audit fix !_

npm start

- _Tap Ctrl C (to stop the miner)_

- _Start miner again (if you have closed UserLAnd app):_

cd miner

cd mazebchdminer

npm start


_Keep your mining wallet as clean as possible (use it for mining only)_

_I will update this tutorial if I find bugs or improvements_

Have fun

`*Created by*` **[`El_Bitcoiner_CMS`](https://t.me/El_Bitcoiner_CMS)**

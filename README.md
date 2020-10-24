# Kotlin_TestaInternet
Fonte para testar se o celular esta adequadamente conectado a internet



# Primeiro crie a Classe:

     class netWorkTest {
         //testa servidor dns do google
         fun checkIntCON(): Boolean {
         try {
            val ipProcess = Runtime.getRuntime().exec("/system/bin/ping -c 1 8.8.8.8")
            //aqui vc pode por também o endereço do teu servidor backend para testar se ele online
            return ipProcess.waitFor() == 0
        } catch (e: IOException) {
            e.printStackTrace()
        } catch (e: InterruptedException) {
            e.printStackTrace()
        }
        return false
        } 

        }


# Dentro da activity:

    fun isOnline(){

        if(netWorkTest().checkIntCON()){
            //tua ação
        }else{
            //tua ação
        }

    }

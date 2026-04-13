
```jsx
Algoritmo "Verificar_IP"

Var
   IpEntrada: caractere
   Ip1, Ip2, Ip3: caractere
   autorizado: boolean

Inicio

   // Definindo IPs autorizados
   Ip1 <- "192.168.0.1"
   Ip2 <- "192.168.0.2"
   Ip3 <- "192.168.0.3"

   // Inicialmente, acesso bloqueado
   autorizado <- falso

   // Entrada de dados
   escreva("Digite o IP de acesso: ")
   leia(ipEntrada)

   // Verificação de IP
   se (ipEntrada = ip1) ou (ipEntrada = ip2) ou (ipEntrada = ip3) entao
      autorizado <- verdadeiro
   fimse

   // Resultado final
   se (autorizado = verdadeiro) entao
      escreva("Acesso PERMITIDO")
   senao
      escreva("Acesso BLOQUEADO")
   fimse

Fimalgoritmo
```

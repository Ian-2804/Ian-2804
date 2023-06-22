Ops=0
OpsDoc=0
SiNo=0
DatosVehiculos=[]
Multas=[]
Doc=[]
OpsEmi=0
mult=0
print("biendido a Auto Seguro ")
while Ops<1 or Ops>=5:
    print("Ingrese lo que desea realizar:")
    print("1) Grabar un vehiculo")
    print("2) Buscar un vehiculo")
    print("3) Imprimir certificado")
    print("4) Salir del sistema")
    Ops=int(input("Ingrese una opcion: "))
    if Ops==1:
      print("Bienvenido al grabado de los Vehiculos")
    Tipo=str(input("Ingrese el tipo de vehiculo: "))
    Patente=str(input("Ingrese la patente de el vehiculo sin guiones ni puntos: "))
while len(Marca)<2 or len(Marca)>15:
 Marca=""
Marca=str(input("Ingrese la marca del vehiculo: "))
Precio=0
while Precio<=5000000:
   Precio=int(input("Ingrese el precio del vehiculo: "))
   FechaRegVeh=(input("Ingrese la fecha de registro de su vehiculo (Utilize el formato mostrado a continuacion DIA-MES-AÑO): "))
   NomDueño=input("opere nombre del dueño del vehiculo: ")
while SiNo<1 or SiNo>2:
    SiNo=int(input("¿tiene alguna multa? \n1)Si\n2)No\n"))
if SiNo==1:
    MontoM=(input("Ingrese el monto de su multa: "))
    FechaM=(input("Ingresa la fecha de la multa: (DIA-MES-AÑO) "))
    Multa=[FechaM,MontoM]
    Multas.append(Multa)
    OtraM=int(input("¿tiene alguna otra multa? \n1)Si\n2)No\n"))
if OtraM==1:
    MontoM=""
    FechaM=""
    SiNo=0
elif OtraM==2:
        print("MULTAS INGRESADAS")
elif SiNo==2:
    print(".")
    Vehiculo=[Tipo,Patente,Marca,Precio,FechaRegVeh,NomDueño,Multas]
    DatosVehiculos.append(Vehiculo)
Ops=0
elif Ops==2:
 print("ops buscador de vehiculos")
 BusquedaPatente=input("Ingrese la patente del vehiculo a buscar sin punto ni guion: ")
 VehEncontrado=None
 for Vehiculo in DatosVehiculos:
if Vehiculo[1]==BusquedaPatente:
if VehEncontrado is not None:
 print("Vehiculo encontrado: ")
 print(f"Tipo: {VehEncontrado[0]}")
 print(f"Patente: {VehEncontrado[1]}")
 print(f"Marca: {VehEncontrado[2]}")
 print(f"Precio: {VehEncontrado[3]}")
 print(f"Fecha de Registro: {VehEncontrado[4]}")
 print(f"Nombre del dueño: {VehEncontrado[5]}")
 print(f"Multas: {VehEncontrado[6]}")
else:
 print("Vehiculo no encontrado")
 Ops=0
elif Ops==3:
 print("este es el visor e imprimidor de certificados de vehiculos")
 BusquedaPatente=input("Ingrese la patente del vehiculo del cual quiere tener los certificados:")
 VehEncontrado=None
for Vehiculo in DatosVehiculos:
if Vehiculo[1]==BusquedaPatente:
 VehEncontrado=Vehiculo
break
if VehEncontrado is not None:
while OpsDoc<1 or OpsDoc>=5:
 print("Que archivo va a imprimir:")
 print("1)Emision de contaminantes $1500")
 print("2)Anotaciones vigentes $2200")
 print("3)Multas $3500")
 Opsdoc=int(input("Ingrese el documento que va a impirmir: "))
 if Opsdoc==1:
    EmiDoc=(f"Emision de contaminantes:\nFechaReg: {VehEncontrado[4]}\nDueño:
    {VehEncontrado[5]}\nTipo: {VehEncontrado[0]}\nPatente: {VehEncontrado[1]}\nMarca:
    {VehEncontrado[2]}\n Sello verde:APROBADO\n")
    Doc.append(EmiDoc)
while OpsEmi<1 or OpsEmi>=3:
    print("¿Desea sumar otro documento o imprimir el seleccionado?\n1)Si\n2)No")
    OpsEmi=int(input())
    if OpsEmi==1:
OpsDoc=0
    if OpsEmi==2:
    print("Gracias por utilizar este sistema")
    if OpsDoc==2:
    AnoVig=(f"Anotaciones Vigentes:\nFechaReg: {VehEncontrado[4]}\nDueño:
    {VehEncontrado[5]}\nTipo: {VehEncontrado[0]}\nPatente: {VehEncontrado[1]}\nMarca:
    {VehEncontrado[2]}\n")
 Doc.append(AnoVig)
 while OpsEmi<1 or OpsEmi>=3:
 print("¿Desea sumar otro documento o imprimir el seleccionado?\n1)Si\n2)No")
 OpsEmi=int(input())
 if OpsEmi==1:
 OpsDoc=0
 if OpsEmi==2:
 print("Gracias por utilizar este sistema")
 if Opsdoc==3:
 print("Multas:\n")
 mult=1
 while OpsEmi<1 or OpsEmi>=3:
 print("¿Desea sumar otro documento o imprimir el seleccionado?\n1)Si\n2)No")
 OpsEmi=int(input())
 if OpsEmi==1:
 OpsDoc=0
 if OpsEmi==2:
print("Gracias por utilizar este sistema")
 print(Doc)
 if mult==1:
 print(VehEncontrado[6])
else:
  print("Vehiculo no encontrado")
  Ops=3
  Ops=0
else:
    ops4:
    print("gracias por usar el sistema de Ian Alzamora version 1.111.1")

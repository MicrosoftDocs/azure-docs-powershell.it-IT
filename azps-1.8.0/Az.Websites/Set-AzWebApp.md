---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 7fb1118d612aae7cf5495f0743550510088e5dbe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676256"
---
# Set-AzWebApp



## Sinossi

Modifica un'app Azure Web.



## SINTASSI



### S1

```

Set-AzWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>] [[-NetFrameworkVersion] <String>]

 [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>] [[-HttpLoggingEnabled] <Boolean>]

 [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>] [[-ConnectionStrings] <Hashtable>]

 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]

 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]

 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]

 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]

 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]

 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-AzureStoragePath <WebAppAzureStoragePath[]>]

 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]

```



### S2

```

Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]

 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]

```



## Descrizione

Il cmdlet **set-AzWebApp** imposta una Azure Web App.



## ESEMPI



### Esempio 1

```

PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"

```



Questo comando modifica il piano Appservice associato all'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus. Usare il collegamento per altre informazioni sulla modifica del piano Appservice e dei vincoli associati.

https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan


### Esempio 2

```

PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true

```



Questo comando imposta HttpLoggingEnabled su true per l'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus



## PARAMETRI



### -AppServicePlan

Nome piano servizio app



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: False

Position: 2

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -AppSettings

HashTable delle impostazioni dell'app



```yaml

Type: System.Collections.Hashtable

Parameter Sets: S1

Aliases:



Required: False

Position: 9

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -AsJob

Esegui cmdlet in background



```yaml

Type: System.Management.Automation.SwitchParameter

Parameter Sets: (All)

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -AssignIdentity

Abilitare/disabilitare MSI in un Web App o functionapp di Azure esistente



```yaml

Type: System.Boolean

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -AutoSwapSlotName

Nome dello slot di destinazione per lo scambio automatico



```yaml

Type: System.String

Parameter Sets: (All)

Aliases:



Required: False

Position: 15

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -AzureStoragePath

Spazio di archiviazione di Azure da montare all'interno di un'app Web per container. Usare New-AzureRmWebAppAzureStoragePath per crearlo



```yaml

Type: Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath[]

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -ConnectionStrings

HashTable stringhe di connessione



```yaml

Type: System.Collections.Hashtable

Parameter Sets: S1

Aliases:



Required: False

Position: 10

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -ContainerImageName

Nome immagine contenitore



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -ContainerRegistryPassword

Password del registro di sistema del contenitore privato



```yaml

Type: System.Security.SecureString

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -ContainerRegistryUrl

URL del server del registro di sistema privato



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -ContainerRegistryUser

Nome utente del registro di sistema privato



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -DefaultDocuments

Matrice di stringhe documenti predefinita



```yaml

Type: System.String[]

Parameter Sets: S1

Aliases:



Required: False

Position: 3

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -DefaultProfile

Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.



```yaml

Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer

Parameter Sets: (All)

Aliases: AzContext, AzureRmContext, AzureCredential



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -DetailedErrorLoggingEnabled

Errore di registrazione dettagliata delle funzionalità booleane



```yaml

Type: System.Boolean

Parameter Sets: S1

Aliases:



Required: False

Position: 8

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -EnableContainerContinuousDeployment

Abilita/Disabilita il webhook di distribuzione continua del contenitore



```yaml

Type: System.Boolean

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -HandlerMappings

Interfaccia di mapping dei gestori



```yaml

Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]

Parameter Sets: S1

Aliases:



Required: False

Position: 11

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -HostName

Matrice di stringhe Web App HostNames



```yaml

Type: System.String[]

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -HttpLoggingEnabled

HttpLoggingEnabled booleano



```yaml

Type: System.Boolean

Parameter Sets: S1

Aliases:



Required: False

Position: 7

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -HttpsOnly

Abilitare/disabilitare il reindirizzamento di tutto il traffico a HTTPS in un Azure Web App o functionapp esistente



```yaml

Type: System.Boolean

Parameter Sets: S1

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -ManagedPipelineMode

Nome della modalità pipeline gestita



```yaml

Type: System.String

Parameter Sets: S1

Aliases:

Accepted values: Classic, Integrated



Required: False

Position: 12

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -Nome

Nome Web App



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: True

Position: 1

Default value: None

Accept pipeline input: True (ByPropertyName)

Accept wildcard characters: False

```



### -NetFrameworkVersion

NET Framework



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: False

Position: 4

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -NumberOfWorkers

Numero di dipendenti da allocare



```yaml

Type: System.Int32

Parameter Sets: (All)

Aliases:



Required: False

Position: Named

Default value: None

Accept pipeline input: True (ByValue)

Accept wildcard characters: False

```



### -PhpVersion

Versione php



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: False

Position: 5

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -RequestTracingEnabled

Richiesta di traccia attivata



```yaml

Type: System.Boolean

Parameter Sets: S1

Aliases:



Required: False

Position: 6

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -ResourceGroupName

Nome gruppo risorse



```yaml

Type: System.String

Parameter Sets: S1

Aliases:



Required: True

Position: 0

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -Use32BitWorkerProcess

Usare il processo di lavoro a 32 bit Boolean



```yaml

Type: System.Boolean

Parameter Sets: (All)

Aliases:



Required: False

Position: 14

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### -Web App

Oggetto Web App



```yaml

Type: Microsoft.Azure.Commands.WebApps.Models.PSSite

Parameter Sets: S2

Aliases:



Required: True

Position: 0

Default value: None

Accept pipeline input: True (ByValue)

Accept wildcard characters: False

```



### -WebSocketsEnabled

WebSocketsEnabled booleano



```yaml

Type: System.Boolean

Parameter Sets: S1

Aliases:



Required: False

Position: 13

Default value: None

Accept pipeline input: False

Accept wildcard characters: False

```



### CommonParameters

Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .



## INGRESSI



### System. Int32



### System. String



### Microsoft. Azure. Commands. webapps. Models. PSSite



## OUTPUT



### Microsoft. Azure. Commands. webapps. Models. PSSite



## Note



## COLLEGAMENTI CORRELATI



[Get-AzWebApp](./Get-AzWebApp.md)



[New-AzWebApp](./New-AzWebApp.md)



[Remove-AzWebApp](./Remove-AzWebApp.md)



[Riavviare-AzWebApp](./Restart-AzWebApp.md)



[Start-AzWebApp](./Start-AzWebApp.md)



[Stop-AzWebApp](./Stop-AzWebApp.md)


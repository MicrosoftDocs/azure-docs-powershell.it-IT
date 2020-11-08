---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CF7E7C62-88FC-48CA-940F-9A6C7442BEF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8166cd3faa951171dd3ac865b17b8a03bcefdd45
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023841"
---
# Publish-AzureServiceProject

## Sinossi
Pubblicare il servizio corrente in Windows Azure.

## SINTASSI

### PublishFromServiceDefinition (impostazione predefinita)
```
Publish-AzureServiceProject [-ServiceName <String>] [-StorageAccountName <String>] [-Location <String>]
 [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>] [-ForceUpgrade]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### PublishFromPackage
```
Publish-AzureServiceProject [-Package <String>] -Configuration <String> [-StorageAccountName <String>]
 [-Location <String>] [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>]
 [-ForceUpgrade] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.
Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

Il cmdlet **Publish-AzureServiceProject** pubblica il servizio corrente nel cloud.
È possibile specificare la configurazione di pubblicazione, ad esempio **Subscription** , **StorageAccountName** , **location** , **slot** , nella riga di comando o in impostazioni locali tramite il cmdlet **set-AzureServiceProject** .

## ESEMPI

### Esempio 1: pubblicare un progetto di servizio con i valori predefiniti
```
PS C:\> Publish-AzureServiceProject
```

Questo esempio pubblica il servizio corrente, usando le impostazioni correnti del servizio e il profilo di pubblicazione di Azure corrente.

### Esempio 2: creare un pacchetto di distribuzione
```
PS C:\> Publish-AzureServiceProject -PackageOnly
```

Questo esempio crea un file del pacchetto di distribuzione (con estensione cspkg) nella directory del servizio e non viene pubblicato in Windows Azure.

## PARAMETRI

### -AffinityGroup
Specifica il gruppo di affinità che si desidera venga usato dal servizio.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Configurazione
Specifica il file di configurazione del servizio.
Se specifichi questo parametro, specifica il parametro del *pacchetto* .

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: cc

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DeploymentName
Specifica il nome della distribuzione.

```yaml
Type: String
Parameter Sets: (All)
Aliases: dn

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceUpgrade
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: f

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Avvio
Apre una finestra del browser in modo da poter visualizzare l'applicazione dopo la distribuzione.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Posizione
Area geografica in cui verrà ospitata l'applicazione.
I valori possibili sono: 
  
- Ovunque in Asia
- Ovunque Europa
- Ovunque negli Stati Uniti
- Asia orientale
- Stati Uniti orientali
- Stati Uniti nord-centrale
- Nord Europa
- Stati Uniti del centro sud
- Asia sud-orientale
- Europa occidentale
- Ovest degli Stati Uniti
 
Se non è specificata alcuna posizione, verrà usata la posizione specificata nell'ultima chiamata a **set-AzureServiceProject** . Se non è stata mai specificata alcuna posizione, la posizione verrà selezionata in modo casuale dalle posizioni "North Central US" e "South Central US".

```yaml
Type: String
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pacchetto
Specifica il file del pacchetto da distribuire.
Specifica un file locale con estensione cspkg o un URI di un BLOB contenente il pacchetto.
Se specifichi questo parametro, non specificare il parametro *ServiceName* .

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: sp

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet.
Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceName
Specifica il nome da usare per il servizio durante la pubblicazione in Windows Azure.
Il nome determina parte dell'etichetta nel sottodominio cloudapp.net usato per indirizzare il servizio quando è ospitato in Windows Azure, ovvero **Name**. cloudapp.NET.
Qualsiasi nome specificato durante la pubblicazione del servizio sostituisce il nome assegnato al momento della creazione del servizio.
Vedere il cmdlet **New-AzureServiceProject** .

```yaml
Type: String
Parameter Sets: PublishFromServiceDefinition
Aliases: sv

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
Slot di distribuzione da usare per questo servizio.
I valori possibili sono "Staging" e "Production".
Se non viene specificato alcuno slot, viene usato lo slot specificato nell'ultima chiamata a Set-AzureDeploymentSlot.
Se non è mai stato specificato alcuno slot, viene usato lo slot di produzione.

```yaml
Type: String
Parameter Sets: (All)
Aliases: sl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Specifica il nome dell'account di archiviazione di Windows Azure da usare durante la pubblicazione del servizio.
Questo valore non viene usato finché non viene pubblicato il servizio.
Quando questo parametro non viene specificato, il valore viene ottenuto dall'ultimo comando **set-AzureServiceProject** .
Se non è mai stato specificato alcun account di archiviazione, verrà usato un account di archiviazione corrispondente al nome del servizio.
Se non esiste un account di archiviazione di questo tipo, il cmdlet tenta di crearne uno nuovo.
Tuttavia, il tentativo potrebbe non riuscire se un account di archiviazione corrispondente al nome del servizio esiste in un altro abbonamento.

```yaml
Type: String
Parameter Sets: (All)
Aliases: st

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Enable-AzureServiceProjectRemoteDesktop](./Enable-AzureServiceProjectRemoteDesktop.md)

[Set-AzureServiceProject](./Set-AzureServiceProject.md)



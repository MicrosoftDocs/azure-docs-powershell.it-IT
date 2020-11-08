---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2AEA385F-E180-4564-A62A-9E913C665801
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fff3ea97c51ee5597e585f3275b25e513c22008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023438"
---
# Reset-AzureRoleInstance

## Sinossi
Richiede un riavvio o una riimmagine di una singola istanza del ruolo o di tutte le istanze del ruolo di un ruolo specifico.

## SINTASSI

```
Reset-AzureRoleInstance [-ServiceName] <String> -Slot <String> -InstanceName <String> [-Reboot] [-Reimage]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Reset-AzureRoleInstance** richiede un riavvio o una riimmagine di un'istanza del ruolo in uso in una distribuzione.
Questa operazione viene eseguita in modo sincrono.
Quando si riavvia un'istanza del ruolo, Azure accetta l'istanza offline, riavvia il sistema operativo sottostante per l'istanza e riporta l'istanza online.
Tutti i dati scritti nel disco locale vengono mantenuti durante il riavvio.
Tutti i dati in memoria vengono persi.

La riimmagine di un'istanza del ruolo comporta un comportamento diverso a seconda del tipo di ruolo.
Per un Web o un ruolo di lavoro, quando il ruolo viene reimaged, Azure prende il ruolo offline e scrive una nuova installazione del sistema operativo Azure Guest nella macchina virtuale.
Il ruolo viene quindi riportato online.
Per un ruolo VM, quando il ruolo viene reimaged, Azure prende il ruolo offline, riapplica l'immagine personalizzata che hai fornito e riporta il ruolo online.

Azure cerca di mantenere i dati in tutte le risorse di archiviazione locali quando il ruolo viene riimmaginato; Tuttavia, in caso di errore hardware temporaneo, la risorsa di archiviazione locale potrebbe essere persa.
Se l'applicazione richiede che i dati vengano mantenuti, è consigliabile scrivere in un'origine dati durevole, ad esempio un'unità Azure.
Tutti i dati scritti in una directory locale diversa da quella definita dalla risorsa di archiviazione locale andranno perduti quando il ruolo viene reimaged.

## ESEMPI

### Esempio 1: riavviare un'istanza del ruolo
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -InstanceName "MyWebRole_IN_0" -Reboot
```

Questo comando Riavvia l'istanza del ruolo denominata MyWebRole_IN_0 nella distribuzione di staging del servizio MySvc01.

### Esempio 2: riimmagine di un'istanza del ruolo
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -Reimage
```

Questo comando riimmaginerà le istanze di ruolo nella distribuzione di staging del servizio cloud di MySvc01.

### Esempio 3: riimmagine di tutte le istanze del ruolo
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc1" -Slot "Production" -Reimage
```

Questo comando riimmaginerà tutte le istanze di ruolo nella distribuzione di produzione del servizio MySvc01.

## PARAMETRI

### -InformationAction
Specifica il modo in cui questo cmdlet risponde a un evento informativo.

I valori accettabili per questo parametro sono i seguenti:

- Continuare
- Ignora
- Informarsi
- SilentlyContinue
- Stop
- Sospensione

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifica una variabile di informazioni.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceName
Specifica il nome dell'istanza del ruolo da riassegnare o riavviare.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### -Riavvio
Specifica che questo cmdlet riavvia l'istanza del ruolo specificata o, se non è specificata alcuna, tutte le istanze del ruolo.
È necessario includere un parametro *reboot* o *Reimage* , ma non entrambi.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Riimmagine
Specifica che questo cmdlet riimmaginerà l'istanza del ruolo specificata o, se non è specificata alcuna, tutte le istanze del ruolo.
È necessario includere un parametro *reboot* o *Reimage* , ma non entrambi.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Specifica il nome del servizio.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
Specifica l'ambiente di distribuzione in cui vengono eseguite le istanze del ruolo.
I valori validi sono: produzione e staging.
Puoi includere il parametro *DeploymentName* o *slot* , ma non entrambi.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

[Set-AzureRole](./Set-AzureRole.md)



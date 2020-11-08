---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C50472E-CE36-4BF1-92C9-A3B9B183ACD1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 929b439c58c344a1902c497bbad6e056e3755025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029776"
---
# Get-AzureRole

## Sinossi
Restituisce un elenco di ruoli nel servizio Microsoft Azure.

## SINTASSI

```
Get-AzureRole [-ServiceName] <String> [[-Slot] <String>] [[-RoleName] <String>] [-InstanceDetails]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRole** restituisce un oggetto List con dettagli sui ruoli nel servizio Microsoft Azure.
Se specifichi il parametro *roleName* , **Get-AzureRole** restituisce i dettagli solo per quel ruolo.
Se specifichi il parametro *InstanceDetails* , vengono restituiti dettagli aggiuntivi specifici dell'istanza.

## ESEMPI

### Esempio 1: ottenere un elenco di ruoli per un servizio
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production"
```

Questo comando restituisce un oggetto con dettagli su tutti i ruoli di produzione in uso nel servizio MySvc01.

### Esempio 2: ottenere informazioni dettagliate su un ruolo in uso in un servizio
```
PS C:\> Get-AzureRole -ServiceName "MySvc1" -Slot "Staging" -RoleName "MyTestVM3"
```

Questo comando restituisce un oggetto con dettagli sul ruolo MyTestVM3, in corso nell'ambiente di gestione temporanea del servizio MySvc01.

### Esempio 3: ottenere informazioni sull'istanza su istanze di un ruolo in uso in un servizio
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestVM02" -InstanceDetails
```

Questo comando restituisce un oggetto con informazioni dettagliate sulle istanze del ruolo MyTestVM02 in uso nell'ambiente di produzione nel servizio MySvc01.

### Esempio 4: ottenere una tabella delle istanze del ruolo associate a un servizio
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -InstanceDetails | Format-Table -Auto "InstanceName", "InstanceSize", "InstanceStatus"
```

Questo comando restituisce una tabella con il nome, le dimensioni e lo stato dell'istanza di tutte le istanze di ruolo in uso nell'ambiente di produzione nel servizio MySvc01.

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

### -InstanceDetails
Specifica che questo cmdlet restituisce i dettagli sulle istanze di ogni ruolo.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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

### -RoleName
Specifica il nome del ruolo da ottenere.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Specifica il nome del servizio Azure.

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
Specifica l'ambiente di distribuzione di Azure.
I valori accettabili per questo parametro sono: produzione o staging.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
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



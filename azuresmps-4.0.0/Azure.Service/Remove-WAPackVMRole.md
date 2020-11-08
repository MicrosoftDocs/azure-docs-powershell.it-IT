---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9999E0EE-4A32-4C18-A6EC-2A073DC08710
online version: ''
schema: 2.0.0
ms.openlocfilehash: e5dfe0f42987ba51613ff9bafa000713456dfaf7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030873"
---
# Remove-WAPackVMRole

## Sinossi
Rimuove gli oggetti ruolo della macchina virtuale.

## SINTASSI

### FromVMRoleObject (impostazione predefinita)
```
Remove-WAPackVMRole -VMRole <VMRole> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### FromCloudService
```
Remove-WAPackVMRole -VMRole <VMRole> -CloudServiceName <String> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Questi argomenti sono deprecati e verranno rimossi in futuro.
Questo argomento descrive il cmdlet nella versione 0.8.1 del modulo PowerShell di Microsoft Azure.
Per scoprire la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

Il cmdlet **Remove-WAPackVMRole** rimuove gli oggetti Role della macchina virtuale.

## ESEMPI

### Esempio 1: rimuovere un ruolo macchina virtuale (creato con il portale WAP)
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole
```

Il primo comando ottiene il ruolo della macchina virtuale denominato ContosoVMRole01 usando il cmdlet **Get-WAPackVMRole** e quindi archivia tale oggetto nella variabile $VMRole.

Il secondo comando rimuove il ruolo della macchina virtuale archiviato in $VMRole.
Il comando richiede la conferma. Supponendo che il ruolo della macchina virtuale sia stato creato usando il portale WAP, non è necessario specificare il nome del servizio cloud.

### Esempio 2: rimuovere un ruolo macchina virtuale creato dopo la creazione manuale di un servizio cloud
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole02"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -CloudServiceName "ContosoCloudService02"
```

Il primo comando ottiene il ruolo della macchina virtuale denominato "ContosoVMRole02" usando il cmdlet **Get-WAPackVMRole** e quindi archivia tale oggetto nella variabile $VMRole.

Il secondo comando rimuove il ruolo della macchina virtuale archiviato in $VMRole.
Il comando richiede la conferma.
Supponendo che il ruolo della macchina virtuale non sia stato creato usando il portale, l'utente deve specificare il nome del servizio cloud.
In questo caso denominato "ContosoCloudService02".

### Esempio 3: rimuovere un ruolo macchina virtuale senza conferma
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole03"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -Force
```

Il primo comando ottiene il servizio cloud denominato ContosoVMRole03 usando il cmdlet **Get-WAPackVMRole** e quindi archivia tale oggetto nella variabile $VMRole.

Il secondo comando rimuove il ruolo della macchina virtuale archiviato in $VMRole.
Questo comando include il parametro *Force* .
Il comando non chiede conferma.

## PARAMETRI

### -CloudServiceName
Specifica il nome del servizio cloud del ruolo della macchina virtuale.

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Impone l'esecuzione del comando senza richiedere la conferma dell'utente.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.
Per impostazione predefinita, questo cmdlet non genera alcun output.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -VMRole
Specifica un ruolo macchina virtuale.
Per ottenere un ruolo di macchina virtuale, usare il cmdlet **Get-WAPackVMRole** .

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Get-WAPackVMRole](./Get-WAPackVMRole.md)

[New-WAPackVMRole](./New-WAPackVMRole.md)

[Set-WAPackVMRole](./Set-WAPackVMRole.md)



---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: f3afbd9b96de51f754dd87dfa42ed6f71e5b3577
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490453"
---
# Save-AzureRmContext

## Sinossi
Salva le informazioni di autenticazione correnti da usare in altre sessioni di PowerShell.

## SINTASSI

```
Save-AzureRmContext [[-Profile] <AzureRmProfile>] [-Path] <String> [-Force] [-WhatIf] [-Confirm]
```

## Descrizione
Il cmdlet Save-AzureRmContext Salva le informazioni di autenticazione correnti da usare in altre sessioni di PowerShell.

## ESEMPI

### Esempio 1: salvataggio del contesto della sessione corrente
```
PS C:\> Add-AzureRmAccount
PS C:\> Save-AzureRmContext -Path C:\test.json
```

Questo esempio salva il contesto Azure della sessione corrente nel file JSON fornito.

### Esempio 2: salvataggio di un contesto specifico
```
PS C:\> Save-AzureRmContext -Profile (Add-AzureRmAccount) -Path C:\test.json
```

Questo esempio salva il contesto Azure passato al cmdlet nel file JSON fornito.

## PARAMETRI

### -Force
Sovrascrivere il file assegnato se esiste

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Specifica il percorso del file in cui salvare le informazioni di autenticazione.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Specifica il contesto Azure da cui viene letto il cmdlet.
Se non specifichi un contesto, questo cmdlet viene letto dal contesto predefinito locale.

```yaml
Type: AzureRmProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
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

## INGRESSI

### Microsoft. Azure. Commands. Common. Authentication. Models. AzureRMProfile

## OUTPUT

### Microsoft. Azure. Commands. profile. Models. PSAzureProfile

## Note

## COLLEGAMENTI CORRELATI


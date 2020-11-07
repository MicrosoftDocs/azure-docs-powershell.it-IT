---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeerasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeerAsn.md
ms.openlocfilehash: 82a112363a561e7566b0d748d00acc75dc026ebb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855397"
---
# Remove-AzPeerAsn

## Sinossi
Rimuovere peer ASN

## SINTASSI

### Predefinito (impostazione predefinita)
```
Remove-AzPeerAsn [-InputObject] <PSPeerAsn> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Remove-AzPeerAsn [-Name] <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Rimuovere un PeerAsn dall'abbonamento.

## ESEMPI

### Esempio 1
```powershell
PS C:> Remove-AzPeerAsn -PeerName Contoso -Force
```

Rimuove il peer ASN

## PARAMETRI

### -AsJob
Eseguire in background.

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

### -Force
{{Fill Force Description}}

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

### -InputObject
Oggetto PeerAsn.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeerAsn
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Nome univoco di PSPeering.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Restituisce vero se completo

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

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeerAsn

## OUTPUT

### System. Boolean

## Note

## COLLEGAMENTI CORRELATI

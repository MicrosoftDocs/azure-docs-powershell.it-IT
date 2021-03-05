---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: f344c3cd08fb717d1229fb0abb4386c8a2d39d5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995986"
---
# Set-AzResourceGroup

## SYNOPSIS
Modifica un gruppo di risorse.

## SINTASSI

### SetByResourceGroupName (impostazione predefinita)
```
Set-AzResourceGroup -Name <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceGroupId
```
Set-AzResourceGroup [-Tag] <Hashtable> -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Set-AzResourceGroup** modifica le proprietà di un gruppo di risorse.
È possibile usare questo cmdlet per aggiungere, modificare o eliminare i tag di Azure applicati a un gruppo di risorse.
Specificare il *parametro Name* per identificare il gruppo di risorse e il *parametro Tag* per modificare i tag.
Non è possibile usare questo cmdlet per modificare il nome di un gruppo di risorse.

## ESEMPI

### Esempio 1: Applicare un tag a un gruppo di risorse
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

Questo comando applica un tag Department con valore IT a un gruppo di risorse che non ha tag esistenti.

### Esempio 2: Aggiungere tag a un gruppo di risorse
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

Questo esempio aggiunge un tag Di stato con il valore Approvato e un tag PER2016 a un gruppo di risorse che contiene tag esistenti. Poiché i tag specificati sostituiscono quelli esistenti, è necessario includere i tag esistenti nella nuova raccolta di tag, in caso contrario andranno persi.
Il primo comando ottiene il gruppo di risorse ContosoRG e usa il metodo punto per ottenere il valore della proprietà Tag. Il comando archivia i tag nella $Tags variabile.
Il secondo comando ottiene i tag nella $Tags variabile.
Il terzo comando usa l'operatore di assegnazione += per aggiungere i tag Status e FY2016 alla matrice di tag nella $Tags variabile.
Il quarto comando usa il *parametro Tag* di **Set-AzResourceGroup** per applicare i tag nella variabile $Tags al gruppo di risorse ContosoRG.
Il quinto comando ottiene tutti i tag applicati al gruppo di risorse ContosoRG. L'output indica che il gruppo di risorse ha il tag Department e i due nuovi tag, Status e FY2015.

### Esempio 3: Eliminare tutti i tag per un gruppo di risorse
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

Questo comando specifica il *parametro Tag* con un valore di tabella hash vuoto per eliminare tutti i tag dal gruppo di risorse ContosoRG.

## PARAMETERS

### -ApiVersion
Specifica la versione dell'API supportata dal provider di risorse.
È possibile specificare una versione diversa da quella predefinita.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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

### -Id
Specifica l'ID del gruppo di risorse da modificare.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifica il nome del gruppo di risorse da modificare.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.

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

### -Tag
Coppie chiave-valore sotto forma di tabella hash. Ad esempio: @{key0="value0";key1=$null;key2="value2"} Un tag è una coppia nome-valore che è possibile creare e applicare a risorse e gruppi di risorse. Dopo aver assegnato i tag a risorse e gruppi, è possibile usare il parametro *Tag* di Get-AzResource e Get-AzResourceGroup per cercare risorse e gruppi in base al nome o al nome e al valore del tag. È possibile usare i contrassegni per categorizzare le risorse, ad esempio per reparto o centro di costo, oppure per tenere traccia di note o commenti sulle risorse.
Per aggiungere o modificare un tag, è necessario sostituire la raccolta di tag per il gruppo di risorse. Per eliminare un tag, immettere una tabella hash con tutti i tag attualmente applicati al gruppo di risorse da **Get-AzResourceGroup,** ad eccezione del tag da eliminare. Per eliminare tutti i tag da un gruppo di risorse, specificare una tabella hash vuota: `@{}` .

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

### System.Collections.Hashtable

## OUTPUT

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzResource](./Get-AzResource.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

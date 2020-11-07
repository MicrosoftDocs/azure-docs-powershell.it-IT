---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4E5C059B-36F3-41C8-9FDB-69F5318CF39B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzResourceGroup.md
ms.openlocfilehash: d645f430c21a1e9675a0f356cffacbad6a7b5740
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862337"
---
# Set-AzResourceGroup

## Sinossi
Modifica un gruppo di risorse.

## SINTASSI

### SetByResourceGroupName (impostazione predefinita)
```
Set-AzResourceGroup [-Name] <String> [-Tag] <Hashtable> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceGroupId
```
Set-AzResourceGroup [-Tag] <Hashtable> [-Id] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzResourceGroup** modifica le proprietà di un gruppo di risorse.
Puoi usare questo cmdlet per aggiungere, modificare o eliminare i tag Azure applicati a un gruppo di risorse.
Specifica il parametro *Name* per identificare il gruppo di risorse e il parametro *tag* per modificare i tag.
Non è possibile usare questo cmdlet per cambiare il nome di un gruppo di risorse.

## ESEMPI

### Esempio 1: applicare un contrassegno a un gruppo di risorse
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{Department="IT"}
```

Questo comando applica un tag Department con un valore di un gruppo di risorse che non contiene tag esistenti.

### Esempio 2: aggiungere tag a un gruppo di risorse
```
PS C:\>$Tags = (Get-AzResourceGroup -Name "ContosoRG").Tags
PS C:\> $Tags
PS C:\> $Tags += @{"Status"="Approved"; "FY2016"=$null}
PS C:\> Set-AzResourceGroup -Name "ContosoRG" -Tag $Tags
PS C:> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

Questo esempio aggiunge un tag di stato con un valore approvato e un tag FY2016 a un gruppo di risorse con tag esistenti. Poiché i tag specificati sostituiscono i tag esistenti, è necessario includere i tag esistenti nella nuova raccolta di tag oppure perderli.
Il primo comando ottiene il gruppo di risorse ContosoRG e usa il metodo dot per ottenere il valore della proprietà Tags. Il comando Archivia i tag nella variabile $Tags.
Il secondo comando ottiene i contrassegni nella variabile $Tags.
Il terzo comando usa l'operatore di assegnazione + = per aggiungere i tag status e FY2016 alla matrice di tag nella variabile $Tags.
Il quarto comando usa il parametro *tag* di **set-AzResourceGroup** per applicare i tag nella variabile $Tags al gruppo di risorse ContosoRG.
Il quinto comando consente di ottenere tutti i tag applicati al gruppo di risorse ContosoRG. L'output mostra che il gruppo di risorse ha il tag Department e i due nuovi tag, status e FY2015.

### Esempio 3: eliminare tutti i tag per un gruppo di risorse
```
PS C:\>Set-AzResourceGroup -Name "ContosoRG" -Tag @{}
```

Questo comando specifica il parametro *tag* con un valore di tabella hash vuoto per eliminare tutti i tag dal gruppo di risorse ContosoRG.

## PARAMETRI

### -ApiVersion
Specifica la versione dell'API supportata dal provider di risorse.
Puoi specificare una versione diversa rispetto alla versione predefinita.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Specifica l'ID del gruppo di risorse da modificare.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome del gruppo di risorse da modificare.

```yaml
Type: System.String
Parameter Sets: SetByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.

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
Coppie chiave-valore in forma di tabella hash. Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"} un tag è una coppia nome-valore che è possibile creare e applicare alle risorse e ai gruppi di risorse. Dopo aver assegnato i tag a risorse e gruppi, è possibile usare il parametro *tag* di Get-AzResource e Get-AzResourceGroup per cercare risorse e gruppi in base al nome del tag o al nome e al valore. È possibile usare i tag per suddividere in categorie le risorse, ad esempio per reparto o centro costo, oppure per tenere traccia di note o commenti sulle risorse.
Per aggiungere o modificare un tag, è necessario sostituire la raccolta di tag per il gruppo di risorse. Per eliminare un contrassegno, immettere una tabella hash con tutti i tag attualmente applicati al gruppo di risorse, da **Get-AzResourceGroup** , ad eccezione del contrassegno che si desidera eliminare. Per eliminare tutti i tag da un gruppo di risorse, specificare una tabella hash vuota: `@{}` .

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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Commands. resources. Models. PSResourceGroup

## Note

## COLLEGAMENTI CORRELATI

[Get-AzResource](./Get-AzResource.md)

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

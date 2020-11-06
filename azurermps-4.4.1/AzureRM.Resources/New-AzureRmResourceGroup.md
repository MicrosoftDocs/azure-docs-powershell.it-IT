---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0632DAD6-F331-454F-9E7E-2164AB413E77
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceGroup.md
ms.openlocfilehash: ccb0b4afdf39510461dd0f6627748492ba22818f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516087"
---
# New-AzureRmResourceGroup

## Sinossi
Crea un gruppo di risorse Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
New-AzureRmResourceGroup -Name <String> -Location <String> [-Tag <Hashtable>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureRmResourceGroup** crea un gruppo di risorse Azure.

È possibile creare un gruppo di risorse usando solo un nome e un percorso e quindi usare il cmdlet New-AzureRmResource per creare risorse da aggiungere al gruppo di risorse.

Per aggiungere una distribuzione a un gruppo di risorse esistente, usare il cmdlet New-AzureRmResourceGroupDeployment. Per aggiungere una risorsa a un gruppo di risorse esistente, usare il cmdlet **New-AzureRmResource** . Una risorsa Azure è un'entità Azure gestita dall'utente, ad esempio un server di database, un database o un sito Web. Un gruppo di risorse Azure è una raccolta di risorse Azure distribuite come unità.

## ESEMPI

### Esempio 1: creare un gruppo di risorse vuoto
```
PS C:\>New-AzureRmResourceGroup -Name "RG01" -Location "South Central US"
```

Questo comando crea un gruppo di risorse che non contiene risorse. È possibile usare i cmdlet **New-AzureRmResource** o **New-AzureRmResourceGroupDeployment** per aggiungere risorse e distribuzioni a questo gruppo di risorse.

### Esempio 2: creare un gruppo di risorse con tag
```
PS C:\>New-AzureRmResourceGroup -Name "RG01" -Location "South Central US" -Tag @{"Empty"=$null; "Department"="Marketing"}
```

Questo comando crea un gruppo di risorse vuoto. Questo comando è uguale al comando dell'esempio 1, ad eccezione del fatto che assegna i tag al gruppo di risorse. Il primo tag, denominato Empty, può essere usato per identificare i gruppi di risorse che non hanno risorse. Il secondo tag è denominato reparto e ha un valore di marketing. Puoi usare un tag come questo per categorizzare i gruppi di risorse per l'amministrazione o il budget.

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

### -Force
Impone l'esecuzione del comando senza richiedere la conferma dell'utente.

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

### -Posizione
Specifica la posizione del gruppo di risorse. Specificare una posizione nel centro dati di Azure, ad esempio ovest degli Stati Uniti o Asia sud-orientale. È possibile inserire un gruppo di risorse in qualsiasi posizione. Il gruppo risorse non deve trovarsi nella stessa posizione dell'abbonamento a Azure o nella stessa posizione delle proprie risorse.

Per determinare quale posizione supporta ogni tipo di risorsa, usare il cmdlet Get-AzureRmResourceProvider con il parametro *ProviderNamespace* .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Specifica un nome per il gruppo di risorse. Il nome della risorsa deve essere univoco nell'abbonamento. Se un gruppo di risorse con quel nome esiste già, il comando richiede la conferma prima di sostituire il gruppo di risorse esistente.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: Named
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
Coppie chiave-valore in forma di tabella hash. Per esempio:

@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}

Per aggiungere o modificare un tag, è necessario sostituire la raccolta di tag per il gruppo di risorse.

Dopo aver assegnato i tag a risorse e gruppi, è possibile usare il parametro *tag* di Get-AzureRmResource e Get-AzureRmResourceGroup per cercare risorse e gruppi per nome di tag o per nome e valore. È possibile usare i tag per suddividere in categorie le risorse, ad esempio per reparto o centro costo, oppure per tenere traccia di note o commenti sulle risorse.

Per ottenere i tag predefiniti, usare il cmdlet Get-AzureRMTag.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno

## OUTPUT

### Microsoft. Azure. Commands. ResourceManagement. Models. PSResourceGroup

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmResourceProvider](./Get-AzureRmResourceProvider.md)

[Get-AzureRmResourceGroup](./Get-AzureRmResourceGroup.md)

[New-AzureRmResource](./New-AzureRmResource.md)

[New-AzureRmResourceGroupDeployment](./New-AzureRmResourceGroupDeployment.md)

[Remove-AzureRmResourceGroup](./Remove-AzureRmResourceGroup.md)

[Set-AzureRmResourceGroup](./Set-AzureRmResourceGroup.md)

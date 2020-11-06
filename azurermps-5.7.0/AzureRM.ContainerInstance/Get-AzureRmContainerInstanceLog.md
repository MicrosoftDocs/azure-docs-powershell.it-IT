---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/get-azurermcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
ms.openlocfilehash: 346973683ca7e360c4b4d63a4f2ed4f4856a0797
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508256"
---
# Get-AzureRmContainerInstanceLog

## Sinossi
Ottenere i log di un'istanza di un contenitore in un gruppo di contenitori.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### GetContainerInstanceLogByNamesParamSet (impostazione predefinita)
```
Get-AzureRmContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetContainerInstanceLogByPSContainerGroupParamSet
```
Get-AzureRmContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetContainerInstanceLogByResourceIdParamSet
```
Get-AzureRmContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRmContainerInstanceLog** recupera i log di un contenitore in un gruppo di contenitori.

## ESEMPI

### Esempio 1: ottenere il log della coda di un'istanza di contenitore
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

Ottenere il log dal `container1` gruppo contenitore `mycontainer` . Per impostazione predefinita, verrà restituito il contenuto del log di 4 MB.

### Esempio 2: ottenere il log della coda di un'istanza del contenitore con lo stesso nome del gruppo di contenitori
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

Ottenere il log dal `mycontainer` gruppo contenitore `mycontainer` . Per impostazione predefinita, verrà restituito il contenuto del log di 4 MB.

### Esempio 3: ottenere la coda 2 righe di log di un'istanza di contenitore
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

Ottenere le righe della coda 2 del log dal `container1` gruppo contenitore `mycontainer` .

### Esempio 4: ottenere il log della coda di un'istanza di un contenitore in un gruppo di contenitori con pipe in
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzureRmContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

Ottenere il log da `mycontainer` in pipe in un gruppo di contenitori `mycontainer` . Per impostazione predefinita, verrà restituito il contenuto del log di 4 MB.

## PARAMETRI

### -ContainerGroupName
Nome del gruppo di contenitori.

```yaml
Type: String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputContainerGroup
Oggetto gruppo contenitore di input.

```yaml
Type: PSContainerGroup
Parameter Sets: GetContainerInstanceLogByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Nome dell'istanza del contenitore nel gruppo contenitore.
Impostazione predefinita: uguale al nome del gruppo di contenitori

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome del gruppo di risorse.

```yaml
Type: String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID risorsa.

```yaml
Type: String
Parameter Sets: GetContainerInstanceLogByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Coda
Numero di righe a cui eseguire il tail log.
Se non si specifica, il cmdlet restituirà fino a un log di coda di 4 MB

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup

## OUTPUT

### System. String

## Note

## COLLEGAMENTI CORRELATI

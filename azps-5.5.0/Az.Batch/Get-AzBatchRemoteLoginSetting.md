---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 0e2360e6c4d0ba7d993f1f1aa21feb1b44115e6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205250"
---
# Get-AzBatchRemoteLoginSetting

## SYNOPSIS
Recupera le impostazioni di accesso remoto per un nodo di calcolo.

## SINTASSI

### ID (impostazione predefinita)
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Get-AzBatchRemoteLoginSetting** ottiene le impostazioni di accesso remoto per un nodo di elaborazione in un pool basato sull'infrastruttura di macchine virtuali.

## ESEMPI

### Esempio 1: Ottenere le impostazioni di accesso remoto per tutti i nodi in un pool
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

Il primo comando ottiene un contesto di account batch che contiene le chiavi di accesso per l'abbonamento usando **Get-AzBatchAccountKey.**
Il comando archivia il contesto nella $Context variabile da usare nel comando successivo.
Il secondo comando recupera ogni nodo di calcolo nel pool che ha l'ID ContosoPool usando **Get-AzBatchComputeNode.**
Il comando passa ogni nodo di computer al cmdlet corrente usando l'operatore della pipeline.
Il comando ottiene le impostazioni di accesso remoto per ogni nodo di calcolo.

### Esempio 2: Ottenere le impostazioni di accesso remoto per un nodo
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

Il primo comando ottiene un contesto di account batch contenente i tasti di scelta per l'abbonamento e quindi lo archivia nella $Context variabile.
Il secondo comando ottiene le impostazioni di accesso remoto per il nodo di elaborazione con l'ID specificato nel pool con l'ID ContosoPool.

## PARAMETERS

### -BatchContext
Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.
Per ottenere un **batchAccountContext** che contiene le chiavi di accesso per la sottoscrizione, usare il cmdlet Get-AzBatchAccountKey.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNode
Specifica un nodo di calcolo, come oggetto **PSComputeNode,** per cui questo cmdlet ottiene le impostazioni di accesso remoto.
Per ottenere un oggetto nodo di calcolo, usare il cmdlet Get-AzBatchComputeNode di calcolo.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNodeId
Specifica l'ID del nodo di calcolo per cui ottenere le impostazioni di accesso remoto.
per cui questo cmdlet ottiene le impostazioni di accesso remoto.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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

### -PoolId
Specifica l'ID del pool che contiene la macchina virtuale.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.Batch. Models.PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## OUTPUT

### Microsoft.Azure.Commands.Batch. Models.PSRemoteLoginSettings

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchComputeNode](./Get-AzBatchComputeNode.md)

[Get-AzBatchRemoteDesktopProtocolFile](./Get-AzBatchRemoteDesktopProtocolFile.md)

[Cmdlet batch di Azure](/powershell/module/Az.Batch/)

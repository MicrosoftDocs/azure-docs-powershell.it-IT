---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 0e2360e6c4d0ba7d993f1f1aa21feb1b44115e6b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478319"
---
# Get-AzBatchRemoteLoginSetting

## Sinossi
Ottiene le impostazioni di accesso remoto per un nodo COMPUTE.

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

## Descrizione
Il cmdlet **Get-AzBatchRemoteLoginSetting** ottiene le impostazioni di accesso remoto per un nodo COMPUTE in un pool di macchine virtuali basato sull'infrastruttura.

## ESEMPI

### Esempio 1: ottenere le impostazioni di accesso remoto per tutti i nodi di un pool
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

Il primo comando ottiene un contesto dell'account batch che contiene i tasti di scelta per l'abbonamento utilizzando **Get-AzBatchAccountKey**.
Il comando Archivia il contesto nella variabile $Context da usare nel comando successivo.
Il secondo comando ottiene ogni nodo Compute nel pool che contiene l'ID ContosoPool utilizzando **Get-AzBatchComputeNode**.
Il comando passa ogni nodo del computer al cmdlet corrente usando l'operatore pipeline.
Il comando ottiene le impostazioni di accesso remoto per ogni nodo COMPUTE.

### Esempio 2: ottenere le impostazioni di accesso remoto per un nodo
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

Il primo comando ottiene un contesto dell'account batch che contiene i tasti di scelta per l'abbonamento e lo archivia nella variabile $Context.
Il secondo comando consente di ottenere le impostazioni di accesso remoto per il nodo COMPUTE con l'ID specificato nel pool che contiene l'ID ContosoPool.

## PARAMETRI

### -BatchContext
Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.
Per ottenere un **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzBatchAccountKey.

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
Specifica un nodo COMPUTE, come oggetto **PSComputeNode** , per cui questo cmdlet ottiene le impostazioni di accesso remoto.
Per ottenere un oggetto compute node, usa il cmdlet Get-AzBatchComputeNode.

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
Specifica l'ID del nodo COMPUTE per cui ottenere le impostazioni di accesso remoto.
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
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft.Azure.Commands.Batch. Models. PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## OUTPUT

### Microsoft.Azure.Commands.Batch. Models. PSRemoteLoginSettings

## Note

## COLLEGAMENTI CORRELATI

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchComputeNode](./Get-AzBatchComputeNode.md)

[Get-AzBatchRemoteDesktopProtocolFile](./Get-AzBatchRemoteDesktopProtocolFile.md)

[Cmdlet batch di Azure](/powershell/module/Az.Batch/)

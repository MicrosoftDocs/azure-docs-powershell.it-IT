---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/start-azrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: 269285b806149c191e8162b41faa80177f6ca4eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960222"
---
# <span data-ttu-id="9c88f-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="9c88f-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="9c88f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c88f-102">SYNOPSIS</span></span>
<span data-ttu-id="9c88f-103">Passare dalla replica a un altro server di processo per il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="9c88f-103">Switch replication from one Process server to another for load balancing.</span></span>

## <span data-ttu-id="9c88f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c88f-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric> -SourceProcessServer <ASRProcessServer>
 -TargetProcessServer <ASRProcessServer> [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c88f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9c88f-105">DESCRIPTION</span></span>
<span data-ttu-id="9c88f-106">**Start-AzRecoveryServicesAsrProcessProcessJob** cambia lo spostamento dei dati di replica per le macchine virtuali specificate o per un server di processi specificato nel server di processo di destinazione specificato.</span><span class="sxs-lookup"><span data-stu-id="9c88f-106">The **Start-AzRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="9c88f-107">Usato per il bilanciamento del carico o il passaggio di replica tra server di processo.</span><span class="sxs-lookup"><span data-stu-id="9c88f-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="9c88f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c88f-108">EXAMPLES</span></span>

### <span data-ttu-id="9c88f-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9c88f-109">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="9c88f-110">Processo per tenere traccia del passaggio del server di elaborazione per tutto l'elemento protetto da replica dal server di processo di origine a quello di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9c88f-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="9c88f-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9c88f-111">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="9c88f-112">Processo per tenere traccia del passaggio da un server di processo a un altro per un elemento protetto da replica passato dal server di processo di origine a quello di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9c88f-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="9c88f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c88f-113">PARAMETERS</span></span>

### <span data-ttu-id="9c88f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c88f-114">-DefaultProfile</span></span>
<span data-ttu-id="9c88f-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c88f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c88f-116">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="9c88f-116">-Fabric</span></span>
<span data-ttu-id="9c88f-117">Tessuto di ripristino del sito corrispondente al server di configurazione.</span><span class="sxs-lookup"><span data-stu-id="9c88f-117">Site recovery fabric corresponding to the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: ConfigServer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c88f-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9c88f-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="9c88f-119">Elenco dell'elemento protetto da replica di cui cambiare il server di processo.</span><span class="sxs-lookup"><span data-stu-id="9c88f-119">List of replication protected item whose process server to be switched.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: (All)
Aliases: ReplicatedItem

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c88f-120">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="9c88f-120">-SourceProcessServer</span></span>
<span data-ttu-id="9c88f-121">Server di elaborazione da cui disattivare la replica.</span><span class="sxs-lookup"><span data-stu-id="9c88f-121">The Process server to switch replication out from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c88f-122">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="9c88f-122">-TargetProcessServer</span></span>
<span data-ttu-id="9c88f-123">Server di elaborazione a cui passare la replica.</span><span class="sxs-lookup"><span data-stu-id="9c88f-123">The Process server to switch replication to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c88f-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c88f-124">-Confirm</span></span>
<span data-ttu-id="9c88f-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c88f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c88f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c88f-126">-WhatIf</span></span>
<span data-ttu-id="9c88f-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c88f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c88f-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c88f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c88f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c88f-129">CommonParameters</span></span>
<span data-ttu-id="9c88f-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c88f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c88f-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9c88f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c88f-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="9c88f-132">INPUTS</span></span>

### <span data-ttu-id="9c88f-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9c88f-133">None</span></span>

## <span data-ttu-id="9c88f-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c88f-134">OUTPUTS</span></span>

### <span data-ttu-id="9c88f-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="9c88f-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9c88f-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="9c88f-136">NOTES</span></span>

## <span data-ttu-id="9c88f-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c88f-137">RELATED LINKS</span></span>

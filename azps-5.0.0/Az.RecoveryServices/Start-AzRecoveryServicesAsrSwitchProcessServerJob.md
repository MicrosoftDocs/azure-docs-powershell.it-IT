---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrswitchprocessserverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrSwitchProcessServerJob.md
ms.openlocfilehash: d5f65479fb52eb52b91b82d7af2318576825eada
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200022"
---
# <span data-ttu-id="a85e7-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span><span class="sxs-lookup"><span data-stu-id="a85e7-101">Start-AzRecoveryServicesAsrSwitchProcessServerJob</span></span>

## <span data-ttu-id="a85e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a85e7-102">SYNOPSIS</span></span>
<span data-ttu-id="a85e7-103">Cambiare la replica da un server processo a un altro per il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="a85e7-103">Switch replication from one Process server to another for load balancing.</span></span>

## <span data-ttu-id="a85e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a85e7-104">SYNTAX</span></span>

```
Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric <ASRFabric> -SourceProcessServer <ASRProcessServer>
 -TargetProcessServer <ASRProcessServer> [-ReplicationProtectedItem <ASRReplicationProtectedItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a85e7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a85e7-105">DESCRIPTION</span></span>
<span data-ttu-id="a85e7-106">**Start-AzRecoveryServicesAsrSwitchProcessServerJob** commuta lo spostamento dei dati di replica per le macchine virtuali specificate o un server di processo specificato nel server di processo di destinazione specificato.</span><span class="sxs-lookup"><span data-stu-id="a85e7-106">The **Start-AzRecoveryServicesAsrSwitchProcessServerJob** switches replication data movement for the specified virtual machines or a specified Process server to the specified target Process server.</span></span> <span data-ttu-id="a85e7-107">Usato per il bilanciamento del carico o la replica di commutazione tra i server di processo.</span><span class="sxs-lookup"><span data-stu-id="a85e7-107">Used for load balancing or switching replication between Process servers.</span></span>

## <span data-ttu-id="a85e7-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a85e7-108">EXAMPLES</span></span>

### <span data-ttu-id="a85e7-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a85e7-109">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer
```

<span data-ttu-id="a85e7-110">Processo per tenere traccia del passaggio del server di processo per tutti gli elementi protetti dalla replica dall'origine al server dei processi di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a85e7-110">Job to track switching process server for all replication protected item from source to target process server.</span></span>

### <span data-ttu-id="a85e7-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a85e7-111">Example 2</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrSwitchProcessServerJob -Fabric $fabric -SourceProcessServer $sourceProcessServer  -TargetProcessServer $TargetProcessServer -ReplicatedItem $rpList
```

<span data-ttu-id="a85e7-112">Processo per tenere traccia del server di processo di commutazione per l'elemento protetto della replica passato dall'origine al server dei processi di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a85e7-112">Job to track switching process server for passed replication protected item from source to target process server.</span></span>

## <span data-ttu-id="a85e7-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a85e7-113">PARAMETERS</span></span>

### <span data-ttu-id="a85e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a85e7-114">-DefaultProfile</span></span>
<span data-ttu-id="a85e7-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a85e7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a85e7-116">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="a85e7-116">-Fabric</span></span>
<span data-ttu-id="a85e7-117">Tessuto di ripristino del sito corrispondente al server di configurazione.</span><span class="sxs-lookup"><span data-stu-id="a85e7-117">Site recovery fabric corresponding to the Configuration Server.</span></span>

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

### <span data-ttu-id="a85e7-118">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a85e7-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a85e7-119">Elenco di elementi protetti da replica di cui è possibile cambiare il server di processo.</span><span class="sxs-lookup"><span data-stu-id="a85e7-119">List of replication protected item whose process server to be switched.</span></span>

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

### <span data-ttu-id="a85e7-120">-SourceProcessServer</span><span class="sxs-lookup"><span data-stu-id="a85e7-120">-SourceProcessServer</span></span>
<span data-ttu-id="a85e7-121">Il server di processo per disattivare la replica.</span><span class="sxs-lookup"><span data-stu-id="a85e7-121">The Process server to switch replication out from.</span></span>

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

### <span data-ttu-id="a85e7-122">-TargetProcessServer</span><span class="sxs-lookup"><span data-stu-id="a85e7-122">-TargetProcessServer</span></span>
<span data-ttu-id="a85e7-123">Il server di processo per cambiare la replica.</span><span class="sxs-lookup"><span data-stu-id="a85e7-123">The Process server to switch replication to.</span></span>

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

### <span data-ttu-id="a85e7-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a85e7-124">-Confirm</span></span>
<span data-ttu-id="a85e7-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a85e7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a85e7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a85e7-126">-WhatIf</span></span>
<span data-ttu-id="a85e7-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a85e7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a85e7-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a85e7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a85e7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a85e7-129">CommonParameters</span></span>
<span data-ttu-id="a85e7-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a85e7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a85e7-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a85e7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a85e7-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a85e7-132">INPUTS</span></span>

### <span data-ttu-id="a85e7-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a85e7-133">None</span></span>

## <span data-ttu-id="a85e7-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a85e7-134">OUTPUTS</span></span>

### <span data-ttu-id="a85e7-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a85e7-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a85e7-136">Note</span><span class="sxs-lookup"><span data-stu-id="a85e7-136">NOTES</span></span>

## <span data-ttu-id="a85e7-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a85e7-137">RELATED LINKS</span></span>

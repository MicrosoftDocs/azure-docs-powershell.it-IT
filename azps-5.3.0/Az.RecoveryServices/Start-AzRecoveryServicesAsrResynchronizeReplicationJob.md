---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 0429976c64ed6e7989208c28fea1ee0a008436c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384397"
---
# <span data-ttu-id="8f540-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="8f540-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="8f540-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8f540-102">SYNOPSIS</span></span>
<span data-ttu-id="8f540-103">Avvia la risincronizzazione della replica.</span><span class="sxs-lookup"><span data-stu-id="8f540-103">Starts replication resynchronization.</span></span>

## <span data-ttu-id="8f540-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8f540-104">SYNTAX</span></span>

### <span data-ttu-id="8f540-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8f540-105">Default (Default)</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f540-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8f540-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f540-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f540-107">DESCRIPTION</span></span>
<span data-ttu-id="8f540-108">Il cmdlet **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** avvia la risincronizzazione della replica per l'elemento protetto specificato se protetto è in uno stato obbligatorio di risincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="8f540-108">The **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="8f540-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8f540-109">EXAMPLES</span></span>

### <span data-ttu-id="8f540-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8f540-110">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="8f540-111">Avvia Job per risincronizzare la replica nell'elemento protetto della replica passata.</span><span class="sxs-lookup"><span data-stu-id="8f540-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="8f540-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8f540-112">PARAMETERS</span></span>

### <span data-ttu-id="8f540-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f540-113">-DefaultProfile</span></span>
<span data-ttu-id="8f540-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8f540-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f540-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8f540-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="8f540-116">Elemento protetto da replica ASR per risincronizzare la replica.</span><span class="sxs-lookup"><span data-stu-id="8f540-116">ASR replication protected item to resynchronize replication for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f540-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f540-117">-ResourceId</span></span>
<span data-ttu-id="8f540-118">ID risorsa dell'elemento protetto da replica per la risincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="8f540-118">Resource Id of replication protected item to resynchronize.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f540-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8f540-119">-Confirm</span></span>
<span data-ttu-id="8f540-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f540-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f540-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f540-121">-WhatIf</span></span>
<span data-ttu-id="8f540-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f540-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f540-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f540-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f540-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f540-124">CommonParameters</span></span>
<span data-ttu-id="8f540-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f540-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f540-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f540-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f540-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8f540-127">INPUTS</span></span>

### <span data-ttu-id="8f540-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8f540-128">System.String</span></span>

### <span data-ttu-id="8f540-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8f540-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="8f540-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8f540-130">OUTPUTS</span></span>

### <span data-ttu-id="8f540-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8f540-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8f540-132">Note</span><span class="sxs-lookup"><span data-stu-id="8f540-132">NOTES</span></span>

## <span data-ttu-id="8f540-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8f540-133">RELATED LINKS</span></span>

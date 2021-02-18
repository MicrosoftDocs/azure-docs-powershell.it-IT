---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrresynchronizereplicationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrResynchronizeReplicationJob.md
ms.openlocfilehash: 0429976c64ed6e7989208c28fea1ee0a008436c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192839"
---
# <span data-ttu-id="3a680-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span><span class="sxs-lookup"><span data-stu-id="3a680-101">Start-AzRecoveryServicesAsrResynchronizeReplicationJob</span></span>

## <span data-ttu-id="3a680-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a680-102">SYNOPSIS</span></span>
<span data-ttu-id="3a680-103">Avvia la risincronizzazione della replica.</span><span class="sxs-lookup"><span data-stu-id="3a680-103">Starts replication resynchronization.</span></span>

## <span data-ttu-id="3a680-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a680-104">SYNTAX</span></span>

### <span data-ttu-id="3a680-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3a680-105">Default (Default)</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a680-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3a680-106">ByResourceId</span></span>
```
Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a680-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3a680-107">DESCRIPTION</span></span>
<span data-ttu-id="3a680-108">Il cmdlet **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** avvia la risincronizzazione della replica per l'elemento protetto specificato se lo stato protetto è richiesto per la risincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="3a680-108">The **Start-AzRecoveryServicesAsrResynchronizeReplicationJob** cmdlet start resynchronization of replication for the specified protected item if the protected is in a resynchronization required state.</span></span>

## <span data-ttu-id="3a680-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a680-109">EXAMPLES</span></span>

### <span data-ttu-id="3a680-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3a680-110">Example 1</span></span>
```
PS C:\> Start-AzRecoveryServicesAsrResynchronizeReplicationJob -ReplicationProtectedItem $rpi
```

<span data-ttu-id="3a680-111">Avvia il processo di risincronizzazione della replica in un elemento protetto da replica superato.</span><span class="sxs-lookup"><span data-stu-id="3a680-111">Starts job to resynchronize replication on passed replication protected item.</span></span>

## <span data-ttu-id="3a680-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a680-112">PARAMETERS</span></span>

### <span data-ttu-id="3a680-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a680-113">-DefaultProfile</span></span>
<span data-ttu-id="3a680-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3a680-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a680-115">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3a680-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="3a680-116">Elemento protetto da replica ASR per cui risincronizzare la replica.</span><span class="sxs-lookup"><span data-stu-id="3a680-116">ASR replication protected item to resynchronize replication for.</span></span>

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

### <span data-ttu-id="3a680-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a680-117">-ResourceId</span></span>
<span data-ttu-id="3a680-118">ID risorsa dell'elemento protetto da replica per risincronizzare.</span><span class="sxs-lookup"><span data-stu-id="3a680-118">Resource Id of replication protected item to resynchronize.</span></span>

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

### <span data-ttu-id="3a680-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a680-119">-Confirm</span></span>
<span data-ttu-id="3a680-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a680-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a680-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a680-121">-WhatIf</span></span>
<span data-ttu-id="3a680-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a680-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a680-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a680-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a680-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a680-124">CommonParameters</span></span>
<span data-ttu-id="3a680-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a680-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a680-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3a680-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a680-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="3a680-127">INPUTS</span></span>

### <span data-ttu-id="3a680-128">System.String</span><span class="sxs-lookup"><span data-stu-id="3a680-128">System.String</span></span>

### <span data-ttu-id="3a680-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="3a680-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="3a680-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a680-130">OUTPUTS</span></span>

### <span data-ttu-id="3a680-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="3a680-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3a680-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="3a680-132">NOTES</span></span>

## <span data-ttu-id="3a680-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a680-133">RELATED LINKS</span></span>

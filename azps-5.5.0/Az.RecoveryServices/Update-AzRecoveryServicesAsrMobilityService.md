---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 3374ba9cbc1db05b80da6b0b6dd5c5d89212ad51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183863"
---
# <span data-ttu-id="1c884-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="1c884-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="1c884-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c884-102">SYNOPSIS</span></span>
<span data-ttu-id="1c884-103">Push degli aggiornamenti dell'agente dei servizi di mobilità nei computer protetti.</span><span class="sxs-lookup"><span data-stu-id="1c884-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="1c884-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c884-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c884-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1c884-105">DESCRIPTION</span></span>
<span data-ttu-id="1c884-106">Il cmdlet **Update-AzRecoveryServicesAsrMobilityService** cerca di eseguire il push degli aggiornamenti dell'agente del servizio di mobilità nei computer protetti(se è disponibile un aggiornamento).</span><span class="sxs-lookup"><span data-stu-id="1c884-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="1c884-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c884-107">EXAMPLES</span></span>

### <span data-ttu-id="1c884-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1c884-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="1c884-109">Processo per tenere traccia dell'agente mobility service dell'elemento protetto da replica degli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="1c884-109">Job to track Update Replication Protected Item's Mobility Service Agent.</span></span>

## <span data-ttu-id="1c884-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c884-110">PARAMETERS</span></span>

### <span data-ttu-id="1c884-111">-Account</span><span class="sxs-lookup"><span data-stu-id="1c884-111">-Account</span></span>
<span data-ttu-id="1c884-112">ID account run as da usare per push dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="1c884-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="1c884-113">Deve essere nell'elenco di account run as nel tessuto ASR corrispondente all'aggiornamento della macchina.</span><span class="sxs-lookup"><span data-stu-id="1c884-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c884-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c884-114">-DefaultProfile</span></span>
<span data-ttu-id="1c884-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c884-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c884-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1c884-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="1c884-117">Elemento protetto da replica di Azure Site Recovery da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="1c884-117">Azure Site Recovery replication protected item to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c884-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c884-118">-Confirm</span></span>
<span data-ttu-id="1c884-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c884-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c884-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c884-120">-WhatIf</span></span>
<span data-ttu-id="1c884-121">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c884-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c884-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c884-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c884-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c884-123">CommonParameters</span></span>
<span data-ttu-id="1c884-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c884-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c884-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1c884-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c884-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="1c884-126">INPUTS</span></span>

### <span data-ttu-id="1c884-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="1c884-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="1c884-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c884-128">OUTPUTS</span></span>

### <span data-ttu-id="1c884-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="1c884-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1c884-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="1c884-130">NOTES</span></span>

## <span data-ttu-id="1c884-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c884-131">RELATED LINKS</span></span>

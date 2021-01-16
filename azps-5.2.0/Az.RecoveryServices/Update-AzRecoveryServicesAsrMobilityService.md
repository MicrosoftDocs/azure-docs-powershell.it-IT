---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 3374ba9cbc1db05b80da6b0b6dd5c5d89212ad51
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358063"
---
# <span data-ttu-id="e271c-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="e271c-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="e271c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e271c-102">SYNOPSIS</span></span>
<span data-ttu-id="e271c-103">Spingere gli aggiornamenti degli agenti del servizio mobilità in computer protetti.</span><span class="sxs-lookup"><span data-stu-id="e271c-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="e271c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e271c-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e271c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e271c-105">DESCRIPTION</span></span>
<span data-ttu-id="e271c-106">Il cmdlet **Update-AzRecoveryServicesAsrMobilityService** cerca di spingere gli aggiornamenti degli agenti del servizio di mobilità in computer protetti (se è disponibile un aggiornamento).</span><span class="sxs-lookup"><span data-stu-id="e271c-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="e271c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e271c-107">EXAMPLES</span></span>

### <span data-ttu-id="e271c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e271c-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="e271c-109">Processo per tenere traccia dell'agente del servizio di mobilità dell'elemento protetto della replica di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="e271c-109">Job to track Update Replication Protected Item's Mobility Service Agent.</span></span>

## <span data-ttu-id="e271c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e271c-110">PARAMETERS</span></span>

### <span data-ttu-id="e271c-111">-Account</span><span class="sxs-lookup"><span data-stu-id="e271c-111">-Account</span></span>
<span data-ttu-id="e271c-112">ID account RunAs da usare per spingere l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="e271c-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="e271c-113">Deve essere uno dall'elenco di account RunAs nel tessuto ASR corrispondente al computer da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="e271c-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

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

### <span data-ttu-id="e271c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e271c-114">-DefaultProfile</span></span>
<span data-ttu-id="e271c-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e271c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e271c-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e271c-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e271c-117">Elemento protetto della replica del ripristino del sito di Azure da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="e271c-117">Azure Site Recovery replication protected item to be updated.</span></span>

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

### <span data-ttu-id="e271c-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e271c-118">-Confirm</span></span>
<span data-ttu-id="e271c-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e271c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e271c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e271c-120">-WhatIf</span></span>
<span data-ttu-id="e271c-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e271c-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e271c-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e271c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e271c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e271c-123">CommonParameters</span></span>
<span data-ttu-id="e271c-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e271c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e271c-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e271c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e271c-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e271c-126">INPUTS</span></span>

### <span data-ttu-id="e271c-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="e271c-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e271c-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e271c-128">OUTPUTS</span></span>

### <span data-ttu-id="e271c-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e271c-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e271c-130">Note</span><span class="sxs-lookup"><span data-stu-id="e271c-130">NOTES</span></span>

## <span data-ttu-id="e271c-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e271c-131">RELATED LINKS</span></span>

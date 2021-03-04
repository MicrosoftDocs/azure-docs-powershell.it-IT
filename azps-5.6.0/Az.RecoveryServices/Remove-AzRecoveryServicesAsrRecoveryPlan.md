---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 96c50c812dcb73c92dc3704e576bfc45fbf21bba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953245"
---
# <span data-ttu-id="255cd-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="255cd-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="255cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="255cd-102">SYNOPSIS</span></span>
<span data-ttu-id="255cd-103">Elimina il piano di ripristino asr specificato dalla vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="255cd-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

## <span data-ttu-id="255cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="255cd-104">SYNTAX</span></span>

### <span data-ttu-id="255cd-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="255cd-105">ByObject (Default)</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="255cd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="255cd-106">ByName</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="255cd-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="255cd-107">DESCRIPTION</span></span>
<span data-ttu-id="255cd-108">Il cmdlet **Remove-AzRecoveryServicesAsrRecoveryPlan** elimina il piano di ripristino specificato dal vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="255cd-108">The **Remove-AzRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="255cd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="255cd-109">EXAMPLES</span></span>

### <span data-ttu-id="255cd-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="255cd-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="255cd-111">Avvia l'eliminazione del piano di ripristino specificato e restituisce il processo a matrice usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="255cd-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="255cd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="255cd-112">PARAMETERS</span></span>

### <span data-ttu-id="255cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="255cd-113">-DefaultProfile</span></span>
<span data-ttu-id="255cd-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="255cd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="255cd-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="255cd-115">-InputObject</span></span>
<span data-ttu-id="255cd-116">Oggetto di input per il cmdlet: oggetto del piano di ripristino di AsR corrispondente al piano di ripristino da eliminare.</span><span class="sxs-lookup"><span data-stu-id="255cd-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="255cd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="255cd-117">-Name</span></span>
<span data-ttu-id="255cd-118">Specifica il nome del piano di ripristino da eliminare.</span><span class="sxs-lookup"><span data-stu-id="255cd-118">Specifies the name of the recovery plan to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="255cd-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="255cd-119">-Confirm</span></span>
<span data-ttu-id="255cd-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="255cd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="255cd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="255cd-121">-WhatIf</span></span>
<span data-ttu-id="255cd-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="255cd-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="255cd-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="255cd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="255cd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="255cd-124">CommonParameters</span></span>
<span data-ttu-id="255cd-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="255cd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="255cd-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="255cd-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="255cd-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="255cd-127">INPUTS</span></span>

### <span data-ttu-id="255cd-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="255cd-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="255cd-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="255cd-129">OUTPUTS</span></span>

### <span data-ttu-id="255cd-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="255cd-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="255cd-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="255cd-131">NOTES</span></span>

## <span data-ttu-id="255cd-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="255cd-132">RELATED LINKS</span></span>

[<span data-ttu-id="255cd-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="255cd-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="255cd-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="255cd-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="255cd-135">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="255cd-135">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)



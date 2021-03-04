---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: b0780e4fb82a3e58e70f3a0bd64b5211ad07fd42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990834"
---
# <span data-ttu-id="54d8b-101">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="54d8b-101">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="54d8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54d8b-102">SYNOPSIS</span></span>
<span data-ttu-id="54d8b-103">Aggiorna il contenuto di un piano di ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="54d8b-103">Updates the contents of an Azure Site recovery plan.</span></span>

## <span data-ttu-id="54d8b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="54d8b-104">SYNTAX</span></span>

### <span data-ttu-id="54d8b-105">ByRPObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="54d8b-105">ByRPObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54d8b-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="54d8b-106">ByRPFile</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54d8b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="54d8b-107">DESCRIPTION</span></span>
<span data-ttu-id="54d8b-108">Il cmdlet **Update-AzRecoveryServicesAsrRecoveryPlan** aggiorna il contenuto di un piano di ripristino usando il contenuto dell'oggetto del piano di ripristino ASR o del file JSON della definizione del piano di ripristino ASR specificato.</span><span class="sxs-lookup"><span data-stu-id="54d8b-108">The **Update-AzRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="54d8b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="54d8b-109">EXAMPLES</span></span>

### <span data-ttu-id="54d8b-110">Esempio 1: Aggiornare un piano di ripristino</span><span class="sxs-lookup"><span data-stu-id="54d8b-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="54d8b-111">Avviare l'operazione di aggiornamento di un piano di ripristino usando il contenuto dell'oggetto del piano di ripristino asr specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="54d8b-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="54d8b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54d8b-112">PARAMETERS</span></span>

### <span data-ttu-id="54d8b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54d8b-113">-DefaultProfile</span></span>
<span data-ttu-id="54d8b-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="54d8b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="54d8b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54d8b-115">-InputObject</span></span>
<span data-ttu-id="54d8b-116">Oggetto di input per il cmdlet: specifica un oggetto piano di ripristino ASR, il cui contenuto viene usato per aggiornare il piano di ripristino a cui fa riferimento l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="54d8b-116">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54d8b-117">-Path</span><span class="sxs-lookup"><span data-stu-id="54d8b-117">-Path</span></span>
<span data-ttu-id="54d8b-118">Specifica il percorso del file json di definizione del piano di ripristino usato per aggiornare il piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="54d8b-118">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54d8b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54d8b-119">-Confirm</span></span>
<span data-ttu-id="54d8b-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54d8b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54d8b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54d8b-121">-WhatIf</span></span>
<span data-ttu-id="54d8b-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54d8b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54d8b-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54d8b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54d8b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54d8b-124">CommonParameters</span></span>
<span data-ttu-id="54d8b-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54d8b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54d8b-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="54d8b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54d8b-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="54d8b-127">INPUTS</span></span>

### <span data-ttu-id="54d8b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="54d8b-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="54d8b-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="54d8b-129">OUTPUTS</span></span>

### <span data-ttu-id="54d8b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="54d8b-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="54d8b-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="54d8b-131">NOTES</span></span>

## <span data-ttu-id="54d8b-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="54d8b-132">RELATED LINKS</span></span>

[<span data-ttu-id="54d8b-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="54d8b-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="54d8b-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="54d8b-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="54d8b-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="54d8b-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

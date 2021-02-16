---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 6ff0031c5bb8571c69287968f984565daf58b530
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189271"
---
# <span data-ttu-id="60998-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="60998-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="60998-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60998-102">SYNOPSIS</span></span>
<span data-ttu-id="60998-103">Elimina i criteri di replica ASR specificati dal vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="60998-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="60998-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60998-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60998-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="60998-105">DESCRIPTION</span></span>
<span data-ttu-id="60998-106">Il cmdlet **Remove-AzRecoveryServicesAsrPolicy** ha eliminato il criterio di replica specificato dal vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="60998-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="60998-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60998-107">EXAMPLES</span></span>

### <span data-ttu-id="60998-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="60998-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="60998-109">Avvia l'eliminazione dei criteri di replica specificati e restituisce il processo A MATRICE usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="60998-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="60998-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60998-110">PARAMETERS</span></span>

### <span data-ttu-id="60998-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60998-111">-DefaultProfile</span></span>
<span data-ttu-id="60998-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60998-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="60998-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60998-113">-InputObject</span></span>
<span data-ttu-id="60998-114">Oggetto di input per il cmdlet: oggetto criterio di replica ASR corrispondente ai criteri di replica da eliminare.</span><span class="sxs-lookup"><span data-stu-id="60998-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60998-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60998-115">-Confirm</span></span>
<span data-ttu-id="60998-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60998-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60998-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60998-117">-WhatIf</span></span>
<span data-ttu-id="60998-118">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60998-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60998-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60998-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60998-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60998-120">CommonParameters</span></span>
<span data-ttu-id="60998-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60998-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60998-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="60998-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60998-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="60998-123">INPUTS</span></span>

### <span data-ttu-id="60998-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="60998-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="60998-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60998-125">OUTPUTS</span></span>

### <span data-ttu-id="60998-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="60998-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="60998-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="60998-127">NOTES</span></span>

## <span data-ttu-id="60998-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60998-128">RELATED LINKS</span></span>

[<span data-ttu-id="60998-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="60998-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="60998-130">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="60998-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 138fd84684fda149d66be85a0fabfbe4a2df0e52
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355648"
---
# <span data-ttu-id="54993-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="54993-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="54993-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="54993-102">SYNOPSIS</span></span>
<span data-ttu-id="54993-103">Elimina il piano di ripristino ASR specificato da Recovery Services Vault.</span><span class="sxs-lookup"><span data-stu-id="54993-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

## <span data-ttu-id="54993-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="54993-104">SYNTAX</span></span>

### <span data-ttu-id="54993-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="54993-105">ByObject (Default)</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54993-106">ByName</span><span class="sxs-lookup"><span data-stu-id="54993-106">ByName</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54993-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54993-107">DESCRIPTION</span></span>
<span data-ttu-id="54993-108">Il cmdlet **Remove-AzRecoveryServicesAsrRecoveryPlan** Elimina il piano di ripristino specificato dall'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="54993-108">The **Remove-AzRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="54993-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="54993-109">EXAMPLES</span></span>

### <span data-ttu-id="54993-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="54993-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="54993-111">Avvia l'eliminazione del piano di ripristino specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="54993-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="54993-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="54993-112">PARAMETERS</span></span>

### <span data-ttu-id="54993-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54993-113">-DefaultProfile</span></span>
<span data-ttu-id="54993-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="54993-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="54993-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54993-115">-InputObject</span></span>
<span data-ttu-id="54993-116">Oggetto di input per il cmdlet: l'oggetto piano di ripristino ASR corrispondente al piano di ripristino da eliminare.</span><span class="sxs-lookup"><span data-stu-id="54993-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="54993-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="54993-117">-Name</span></span>
<span data-ttu-id="54993-118">Specifica il nome del piano di ripristino da eliminare.</span><span class="sxs-lookup"><span data-stu-id="54993-118">Specifies the name of the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="54993-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="54993-119">-Confirm</span></span>
<span data-ttu-id="54993-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54993-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54993-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54993-121">-WhatIf</span></span>
<span data-ttu-id="54993-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54993-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54993-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54993-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54993-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54993-124">CommonParameters</span></span>
<span data-ttu-id="54993-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54993-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54993-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54993-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54993-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="54993-127">INPUTS</span></span>

### <span data-ttu-id="54993-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="54993-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="54993-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="54993-129">OUTPUTS</span></span>

### <span data-ttu-id="54993-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="54993-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="54993-131">Note</span><span class="sxs-lookup"><span data-stu-id="54993-131">NOTES</span></span>

## <span data-ttu-id="54993-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="54993-132">RELATED LINKS</span></span>

[<span data-ttu-id="54993-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="54993-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="54993-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="54993-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="54993-135">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="54993-135">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)



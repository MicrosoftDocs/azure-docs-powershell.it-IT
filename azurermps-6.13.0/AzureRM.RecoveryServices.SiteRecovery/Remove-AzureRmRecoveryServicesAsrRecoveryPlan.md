---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: b3bedc5c521736ff702f5e7378b4c401a42bce5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685566"
---
# <span data-ttu-id="0dce4-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0dce4-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="0dce4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0dce4-102">SYNOPSIS</span></span>
<span data-ttu-id="0dce4-103">Elimina il piano di ripristino ASR specificato da Recovery Services Vault.</span><span class="sxs-lookup"><span data-stu-id="0dce4-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0dce4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0dce4-104">SYNTAX</span></span>

### <span data-ttu-id="0dce4-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0dce4-105">ByObject (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dce4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0dce4-106">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dce4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0dce4-107">DESCRIPTION</span></span>
<span data-ttu-id="0dce4-108">Il cmdlet **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** Elimina il piano di ripristino specificato dall'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0dce4-108">The **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="0dce4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0dce4-109">EXAMPLES</span></span>

### <span data-ttu-id="0dce4-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0dce4-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="0dce4-111">Avvia l'eliminazione del piano di ripristino specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0dce4-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="0dce4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0dce4-112">PARAMETERS</span></span>

### <span data-ttu-id="0dce4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dce4-113">-DefaultProfile</span></span>
<span data-ttu-id="0dce4-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0dce4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dce4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0dce4-115">-InputObject</span></span>
<span data-ttu-id="0dce4-116">Oggetto di input per il cmdlet: l'oggetto piano di ripristino ASR corrispondente al piano di ripristino da eliminare.</span><span class="sxs-lookup"><span data-stu-id="0dce4-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="0dce4-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="0dce4-117">-Name</span></span>
<span data-ttu-id="0dce4-118">Specifica il nome del piano di ripristino da eliminare.</span><span class="sxs-lookup"><span data-stu-id="0dce4-118">Specifies the name of the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="0dce4-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0dce4-119">-Confirm</span></span>
<span data-ttu-id="0dce4-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0dce4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dce4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dce4-121">-WhatIf</span></span>
<span data-ttu-id="0dce4-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0dce4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0dce4-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0dce4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dce4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dce4-124">CommonParameters</span></span>
<span data-ttu-id="0dce4-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dce4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dce4-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dce4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dce4-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0dce4-127">INPUTS</span></span>

### <span data-ttu-id="0dce4-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0dce4-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="0dce4-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0dce4-129">OUTPUTS</span></span>

### <span data-ttu-id="0dce4-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="0dce4-130">System.Object</span></span>

## <span data-ttu-id="0dce4-131">Note</span><span class="sxs-lookup"><span data-stu-id="0dce4-131">NOTES</span></span>

## <span data-ttu-id="0dce4-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0dce4-132">RELATED LINKS</span></span>

[<span data-ttu-id="0dce4-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0dce4-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="0dce4-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0dce4-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="0dce4-135">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0dce4-135">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)



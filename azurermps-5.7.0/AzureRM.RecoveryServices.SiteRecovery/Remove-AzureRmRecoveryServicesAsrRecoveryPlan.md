---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 5f4298c2a4bfdc081447e6a8b15bac565b20b2db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514228"
---
# <span data-ttu-id="88ff4-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="88ff4-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="88ff4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88ff4-102">SYNOPSIS</span></span>
<span data-ttu-id="88ff4-103">Elimina il piano di ripristino ASR specificato da Recovery Services Vault.</span><span class="sxs-lookup"><span data-stu-id="88ff4-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88ff4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88ff4-104">SYNTAX</span></span>

### <span data-ttu-id="88ff4-105">ByObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="88ff4-105">ByObject (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88ff4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="88ff4-106">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88ff4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88ff4-107">DESCRIPTION</span></span>
<span data-ttu-id="88ff4-108">Il cmdlet **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** Elimina il piano di ripristino specificato dall'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="88ff4-108">The **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="88ff4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88ff4-109">EXAMPLES</span></span>

### <span data-ttu-id="88ff4-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="88ff4-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="88ff4-111">Avvia l'eliminazione del piano di ripristino specificato e restituisce il processo ASR usato per tenere traccia dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="88ff4-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="88ff4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88ff4-112">PARAMETERS</span></span>

### <span data-ttu-id="88ff4-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="88ff4-113">-Confirm</span></span>
<span data-ttu-id="88ff4-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88ff4-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ff4-115">-DefaultProfile</span></span>
<span data-ttu-id="88ff4-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="88ff4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88ff4-117">-InputObject</span></span>
<span data-ttu-id="88ff4-118">Oggetto di input per il cmdlet: l'oggetto piano di ripristino ASR corrispondente al piano di ripristino da eliminare.</span><span class="sxs-lookup"><span data-stu-id="88ff4-118">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88ff4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="88ff4-119">-Name</span></span>
<span data-ttu-id="88ff4-120">Specifica il nome del piano di ripristino da eliminare.</span><span class="sxs-lookup"><span data-stu-id="88ff4-120">Specifies the name of the recovery plan to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88ff4-121">-WhatIf</span></span>
<span data-ttu-id="88ff4-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88ff4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88ff4-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88ff4-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ff4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ff4-124">CommonParameters</span></span>
<span data-ttu-id="88ff4-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88ff4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ff4-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88ff4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ff4-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88ff4-127">INPUTS</span></span>

### <span data-ttu-id="88ff4-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="88ff4-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="88ff4-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88ff4-129">OUTPUTS</span></span>

### <span data-ttu-id="88ff4-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="88ff4-130">System.Object</span></span>

## <span data-ttu-id="88ff4-131">Note</span><span class="sxs-lookup"><span data-stu-id="88ff4-131">NOTES</span></span>

## <span data-ttu-id="88ff4-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88ff4-132">RELATED LINKS</span></span>

[<span data-ttu-id="88ff4-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="88ff4-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="88ff4-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="88ff4-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="88ff4-135">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="88ff4-135">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)



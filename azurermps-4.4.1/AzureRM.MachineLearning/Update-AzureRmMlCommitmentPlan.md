---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Update-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: e7c296c74aad7e733659930aea9487cf2a73aef7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686570"
---
# <span data-ttu-id="d3e7c-101">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="d3e7c-101">Update-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="d3e7c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="d3e7c-103">Aggiorna le proprietà di una risorsa del piano di impegni esistente.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-103">Updates properties of an existing commitment plan resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3e7c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3e7c-104">SYNTAX</span></span>

```
Update-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tags <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3e7c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3e7c-105">DESCRIPTION</span></span>
<span data-ttu-id="d3e7c-106">Aggiorna una risorsa del piano di impegni esistente.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="d3e7c-107">Tieni presente che la maggior parte delle proprietà del piano di impegni non è modificabile e non può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="d3e7c-108">Le proprietà che possono essere modificate includono SKU (che consente di eseguire la migrazione del piano di impegno da una SKU a un'altra) e i contrassegni.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="d3e7c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3e7c-109">EXAMPLES</span></span>

### <span data-ttu-id="d3e7c-110">--------------------------Esempio 1: aggiornare un piano di impegni--------------------------</span><span class="sxs-lookup"><span data-stu-id="d3e7c-110">--------------------------  Example 1: Update a commitment plan  --------------------------</span></span>
<span data-ttu-id="d3e7c-111">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="d3e7c-111">@{paragraph=PS C:\\\>}</span></span>





```
Update-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="d3e7c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3e7c-112">PARAMETERS</span></span>

### <span data-ttu-id="d3e7c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d3e7c-113">-Force</span></span>
<span data-ttu-id="d3e7c-114">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-114">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e7c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3e7c-115">-Name</span></span>
<span data-ttu-id="d3e7c-116">Il nome del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-116">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e7c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3e7c-117">-ResourceGroupName</span></span>
<span data-ttu-id="d3e7c-118">Nome del gruppo di risorse per il piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-118">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e7c-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="d3e7c-119">-SkuCapacity</span></span>
<span data-ttu-id="d3e7c-120">Capacità dell'USK da usare quando si aggiorna il piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-120">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e7c-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d3e7c-121">-SkuName</span></span>
<span data-ttu-id="d3e7c-122">Nome dell'USK da usare per l'aggiornamento del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-122">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e7c-123">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d3e7c-123">-SkuTier</span></span>
<span data-ttu-id="d3e7c-124">Livello dell'USK da usare per l'aggiornamento del piano di impegni di Azure ML.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-124">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e7c-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="d3e7c-125">-Tags</span></span>
<span data-ttu-id="d3e7c-126">Tag per la risorsa piano di impegno.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-126">Tags for the commitment plan resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3e7c-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d3e7c-127">-Confirm</span></span>
<span data-ttu-id="d3e7c-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3e7c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3e7c-129">-WhatIf</span></span>
<span data-ttu-id="d3e7c-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3e7c-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3e7c-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3e7c-132">-DefaultProfile</span></span>
<span data-ttu-id="d3e7c-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3e7c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3e7c-134">CommonParameters</span></span>
<span data-ttu-id="d3e7c-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3e7c-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3e7c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3e7c-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3e7c-137">INPUTS</span></span>

## <span data-ttu-id="d3e7c-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3e7c-138">OUTPUTS</span></span>

### <span data-ttu-id="d3e7c-139">Microsoft. Azure. Management. MachineLearning. CommitmentPlans. Models. CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="d3e7c-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="d3e7c-140">Note</span><span class="sxs-lookup"><span data-stu-id="d3e7c-140">NOTES</span></span>
<span data-ttu-id="d3e7c-141">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="d3e7c-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="d3e7c-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3e7c-142">RELATED LINKS</span></span>


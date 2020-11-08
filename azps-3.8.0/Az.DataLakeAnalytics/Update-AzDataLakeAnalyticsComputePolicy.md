---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/update-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 5dd36c9dbd263dc2e5c72cc6d57f95e29c456c41
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018490"
---
# <span data-ttu-id="5c97b-101">Update-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="5c97b-101">Update-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="5c97b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5c97b-102">SYNOPSIS</span></span>
<span data-ttu-id="5c97b-103">Aggiorna una regola di criteri per il calcolo dei dati di Lake Analytics per una specifica entità AAD.</span><span class="sxs-lookup"><span data-stu-id="5c97b-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="5c97b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c97b-104">SYNTAX</span></span>

```
Update-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c97b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c97b-105">DESCRIPTION</span></span>
<span data-ttu-id="5c97b-106">**Update-AzDataLakeAnalyticsComputePolicy** aggiorna la regola di criteri di calcolo specificata per una specifica entità AAD in un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="5c97b-106">The **Update-AzDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="5c97b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c97b-107">EXAMPLES</span></span>

### <span data-ttu-id="5c97b-108">Esempio 1: aggiornare una regola in un criterio di calcolo</span><span class="sxs-lookup"><span data-stu-id="5c97b-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="5c97b-109">Questo comando aggiorna un criterio denominato "criterio" nell'account "contosoadla" per garantire che l'utente non possa inviare alcun processo con più di 5 unità di analisi.</span><span class="sxs-lookup"><span data-stu-id="5c97b-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="5c97b-110">Esempio 2: creare un criterio di calcolo con entrambi gli aggiornamenti delle regole</span><span class="sxs-lookup"><span data-stu-id="5c97b-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="5c97b-111">Questo comando crea un criterio denominato "criterio" nell'account "contosoadla" per garantire che l'utente non possa inviare alcun processo con più di 5 unità di analisi o con una priorità inferiore a 100</span><span class="sxs-lookup"><span data-stu-id="5c97b-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="5c97b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5c97b-112">PARAMETERS</span></span>

### <span data-ttu-id="5c97b-113">-Account</span><span class="sxs-lookup"><span data-stu-id="5c97b-113">-Account</span></span>
<span data-ttu-id="5c97b-114">Nome dell'account in cui aggiornare i criteri di calcolo.</span><span class="sxs-lookup"><span data-stu-id="5c97b-114">Name of the account to update the compute policy in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c97b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c97b-115">-DefaultProfile</span></span>
<span data-ttu-id="5c97b-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5c97b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c97b-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="5c97b-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="5c97b-118">Le unità di analisi supportate massimo per ogni processo per questo criterio.</span><span class="sxs-lookup"><span data-stu-id="5c97b-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="5c97b-119">In questo caso, MinPriorityPerJob o entrambi i parametri devono essere specificati.</span><span class="sxs-lookup"><span data-stu-id="5c97b-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelismPerJob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c97b-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="5c97b-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="5c97b-121">Priorità minima supportata per ogni processo per questo criterio.</span><span class="sxs-lookup"><span data-stu-id="5c97b-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="5c97b-122">In questo caso, MaxAnalyticsUnitsPerJob o entrambi i parametri devono essere specificati.</span><span class="sxs-lookup"><span data-stu-id="5c97b-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c97b-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c97b-123">-Name</span></span>
<span data-ttu-id="5c97b-124">Nome del criterio di calcolo da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="5c97b-124">Name of the compute policy to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c97b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c97b-125">-ResourceGroupName</span></span>
<span data-ttu-id="5c97b-126">Nome del gruppo di risorse in cui è presente l'account.</span><span class="sxs-lookup"><span data-stu-id="5c97b-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="5c97b-127">Facoltativo e tenterà di scoprire se non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="5c97b-127">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c97b-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5c97b-128">-Confirm</span></span>
<span data-ttu-id="5c97b-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c97b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c97b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c97b-130">-WhatIf</span></span>
<span data-ttu-id="5c97b-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c97b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c97b-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c97b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c97b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c97b-133">CommonParameters</span></span>
<span data-ttu-id="5c97b-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c97b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c97b-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c97b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c97b-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5c97b-136">INPUTS</span></span>

### <span data-ttu-id="5c97b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5c97b-137">System.String</span></span>

### <span data-ttu-id="5c97b-138">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5c97b-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5c97b-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c97b-139">OUTPUTS</span></span>

### <span data-ttu-id="5c97b-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="5c97b-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="5c97b-141">Note</span><span class="sxs-lookup"><span data-stu-id="5c97b-141">NOTES</span></span>

## <span data-ttu-id="5c97b-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c97b-142">RELATED LINKS</span></span>

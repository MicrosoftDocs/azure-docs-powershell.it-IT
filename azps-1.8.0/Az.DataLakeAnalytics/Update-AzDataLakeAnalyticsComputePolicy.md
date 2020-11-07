---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/update-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 39c13bd7dd85f15edf1521ef372196b6c7472512
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836344"
---
# <span data-ttu-id="4d57f-101">Update-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="4d57f-101">Update-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="4d57f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d57f-102">SYNOPSIS</span></span>
<span data-ttu-id="4d57f-103">Aggiorna una regola di criteri per il calcolo dei dati di Lake Analytics per una specifica entità AAD.</span><span class="sxs-lookup"><span data-stu-id="4d57f-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="4d57f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d57f-104">SYNTAX</span></span>

```
Update-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d57f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d57f-105">DESCRIPTION</span></span>
<span data-ttu-id="4d57f-106">**Update-AzDataLakeAnalyticsComputePolicy** aggiorna la regola di criteri di calcolo specificata per una specifica entità AAD in un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="4d57f-106">The **Update-AzDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="4d57f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d57f-107">EXAMPLES</span></span>

### <span data-ttu-id="4d57f-108">Esempio 1: aggiornare una regola in un criterio di calcolo</span><span class="sxs-lookup"><span data-stu-id="4d57f-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="4d57f-109">Questo comando aggiorna un criterio denominato "criterio" nell'account "contosoadla" per garantire che l'utente non possa inviare alcun processo con più di 5 unità di analisi.</span><span class="sxs-lookup"><span data-stu-id="4d57f-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="4d57f-110">Esempio 2: creare un criterio di calcolo con entrambi gli aggiornamenti delle regole</span><span class="sxs-lookup"><span data-stu-id="4d57f-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="4d57f-111">Questo comando crea un criterio denominato "criterio" nell'account "contosoadla" per garantire che l'utente non possa inviare alcun processo con più di 5 unità di analisi o con una priorità inferiore a 100</span><span class="sxs-lookup"><span data-stu-id="4d57f-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="4d57f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d57f-112">PARAMETERS</span></span>

### <span data-ttu-id="4d57f-113">-Account</span><span class="sxs-lookup"><span data-stu-id="4d57f-113">-Account</span></span>
<span data-ttu-id="4d57f-114">Nome dell'account in cui aggiornare i criteri di calcolo.</span><span class="sxs-lookup"><span data-stu-id="4d57f-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="4d57f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d57f-115">-DefaultProfile</span></span>
<span data-ttu-id="4d57f-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4d57f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d57f-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="4d57f-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="4d57f-118">Le unità di analisi supportate massimo per ogni processo per questo criterio.</span><span class="sxs-lookup"><span data-stu-id="4d57f-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="4d57f-119">In questo caso, MinPriorityPerJob o entrambi i parametri devono essere specificati.</span><span class="sxs-lookup"><span data-stu-id="4d57f-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="4d57f-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="4d57f-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="4d57f-121">Priorità minima supportata per ogni processo per questo criterio.</span><span class="sxs-lookup"><span data-stu-id="4d57f-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="4d57f-122">In questo caso, MaxAnalyticsUnitsPerJob o entrambi i parametri devono essere specificati.</span><span class="sxs-lookup"><span data-stu-id="4d57f-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="4d57f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d57f-123">-Name</span></span>
<span data-ttu-id="4d57f-124">Nome del criterio di calcolo da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="4d57f-124">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="4d57f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d57f-125">-ResourceGroupName</span></span>
<span data-ttu-id="4d57f-126">Nome del gruppo di risorse in cui è presente l'account.</span><span class="sxs-lookup"><span data-stu-id="4d57f-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="4d57f-127">Facoltativo e tenterà di scoprire se non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="4d57f-127">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="4d57f-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4d57f-128">-Confirm</span></span>
<span data-ttu-id="4d57f-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d57f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d57f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d57f-130">-WhatIf</span></span>
<span data-ttu-id="4d57f-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d57f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d57f-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d57f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d57f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d57f-133">CommonParameters</span></span>
<span data-ttu-id="4d57f-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d57f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d57f-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d57f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d57f-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d57f-136">INPUTS</span></span>

### <span data-ttu-id="4d57f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4d57f-137">System.String</span></span>

### <span data-ttu-id="4d57f-138">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4d57f-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4d57f-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d57f-139">OUTPUTS</span></span>

### <span data-ttu-id="4d57f-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="4d57f-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="4d57f-141">Note</span><span class="sxs-lookup"><span data-stu-id="4d57f-141">NOTES</span></span>

## <span data-ttu-id="4d57f-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d57f-142">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/update-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 860b58ce3be37eb2ef2277b627971adb301a02af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518748"
---
# <span data-ttu-id="fe80c-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="fe80c-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="fe80c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe80c-102">SYNOPSIS</span></span>
<span data-ttu-id="fe80c-103">Aggiorna una regola di criteri per il calcolo dei dati di Lake Analytics per una specifica entità AAD.</span><span class="sxs-lookup"><span data-stu-id="fe80c-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe80c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe80c-104">SYNTAX</span></span>

```
Update-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe80c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe80c-105">DESCRIPTION</span></span>
<span data-ttu-id="fe80c-106">**Update-AzureRmDataLakeAnalyticsComputePolicy** aggiorna la regola di criteri di calcolo specificata per una specifica entità AAD in un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="fe80c-106">The **Update-AzureRmDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="fe80c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe80c-107">EXAMPLES</span></span>

### <span data-ttu-id="fe80c-108">Esempio 1: aggiornare una regola in un criterio di calcolo</span><span class="sxs-lookup"><span data-stu-id="fe80c-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="fe80c-109">Questo comando aggiorna un criterio denominato "criterio" nell'account "contosoadla" per garantire che l'utente non possa inviare alcun processo con più di 5 unità di analisi.</span><span class="sxs-lookup"><span data-stu-id="fe80c-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="fe80c-110">Esempio 2: creare un criterio di calcolo con entrambi gli aggiornamenti delle regole</span><span class="sxs-lookup"><span data-stu-id="fe80c-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="fe80c-111">Questo comando crea un criterio denominato "criterio" nell'account "contosoadla" per garantire che l'utente non possa inviare alcun processo con più di 5 unità di analisi o con una priorità inferiore a 100</span><span class="sxs-lookup"><span data-stu-id="fe80c-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="fe80c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe80c-112">PARAMETERS</span></span>

### <span data-ttu-id="fe80c-113">-Account</span><span class="sxs-lookup"><span data-stu-id="fe80c-113">-Account</span></span>
<span data-ttu-id="fe80c-114">Nome dell'account in cui aggiornare i criteri di calcolo.</span><span class="sxs-lookup"><span data-stu-id="fe80c-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="fe80c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe80c-115">-DefaultProfile</span></span>
<span data-ttu-id="fe80c-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fe80c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe80c-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="fe80c-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="fe80c-118">Le unità di analisi supportate massimo per ogni processo per questo criterio.</span><span class="sxs-lookup"><span data-stu-id="fe80c-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="fe80c-119">In questo caso, MinPriorityPerJob o entrambi i parametri devono essere specificati.</span><span class="sxs-lookup"><span data-stu-id="fe80c-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="fe80c-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="fe80c-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="fe80c-121">Priorità minima supportata per ogni processo per questo criterio.</span><span class="sxs-lookup"><span data-stu-id="fe80c-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="fe80c-122">In questo caso, MaxAnalyticsUnitsPerJob o entrambi i parametri devono essere specificati.</span><span class="sxs-lookup"><span data-stu-id="fe80c-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="fe80c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe80c-123">-Name</span></span>
<span data-ttu-id="fe80c-124">Nome del criterio di calcolo da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="fe80c-124">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="fe80c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe80c-125">-ResourceGroupName</span></span>
<span data-ttu-id="fe80c-126">Nome del gruppo di risorse in cui è presente l'account.</span><span class="sxs-lookup"><span data-stu-id="fe80c-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="fe80c-127">Facoltativo e tenterà di scoprire se non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="fe80c-127">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="fe80c-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fe80c-128">-Confirm</span></span>
<span data-ttu-id="fe80c-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe80c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe80c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe80c-130">-WhatIf</span></span>
<span data-ttu-id="fe80c-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe80c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe80c-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe80c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe80c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe80c-133">CommonParameters</span></span>
<span data-ttu-id="fe80c-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe80c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe80c-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe80c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe80c-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe80c-136">INPUTS</span></span>

### <span data-ttu-id="fe80c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fe80c-137">System.String</span></span>

### <span data-ttu-id="fe80c-138">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="fe80c-138">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="fe80c-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe80c-139">OUTPUTS</span></span>

### <span data-ttu-id="fe80c-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="fe80c-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="fe80c-141">Note</span><span class="sxs-lookup"><span data-stu-id="fe80c-141">NOTES</span></span>

## <span data-ttu-id="fe80c-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe80c-142">RELATED LINKS</span></span>

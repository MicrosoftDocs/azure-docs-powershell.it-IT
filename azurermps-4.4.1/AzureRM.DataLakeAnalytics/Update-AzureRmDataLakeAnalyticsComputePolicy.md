---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 67cffe7f0cdaebc655eb98321166bb7805844a5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520536"
---
# <span data-ttu-id="1cc14-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="1cc14-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="1cc14-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1cc14-102">SYNOPSIS</span></span>
<span data-ttu-id="1cc14-103">Aggiorna una regola di criteri per il calcolo dei dati di Lake Analytics per una specifica entità AAD.</span><span class="sxs-lookup"><span data-stu-id="1cc14-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cc14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1cc14-104">SYNTAX</span></span>

```
Update-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxDegreeOfParallelismPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cc14-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1cc14-105">DESCRIPTION</span></span>
<span data-ttu-id="1cc14-106">**Update-AzureRmDataLakeAnalyticsComputePolicy** aggiorna la regola di criteri di calcolo specificata per una specifica entità AAD in un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="1cc14-106">The **Update-AzureRmDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="1cc14-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1cc14-107">EXAMPLES</span></span>

### <span data-ttu-id="1cc14-108">Esempio 1: aggiornare una regola in un criterio di calcolo</span><span class="sxs-lookup"><span data-stu-id="1cc14-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxDegreeOfParallelismPerJob 5
```

<span data-ttu-id="1cc14-109">Questo comando aggiorna un criterio denominato "criteri" nell'account "contosoadla" per garantire che l'utente non possa inviare alcun processo con più di 5 parallelismi.</span><span class="sxs-lookup"><span data-stu-id="1cc14-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 parallelism.</span></span>

### <span data-ttu-id="1cc14-110">Esempio 2: creare un criterio di calcolo con entrambi gli aggiornamenti delle regole</span><span class="sxs-lookup"><span data-stu-id="1cc14-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxDegreeOfParallelismPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="1cc14-111">Questo comando crea un criterio denominato "criterio" nell'account "contosoadla" per garantire che l'utente non possa inviare alcun lavoro con più di 5 parallelismi o con una priorità inferiore a 100</span><span class="sxs-lookup"><span data-stu-id="1cc14-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 parallelism or with a priority lower than 100</span></span>

## <span data-ttu-id="1cc14-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1cc14-112">PARAMETERS</span></span>

### <span data-ttu-id="1cc14-113">-Account</span><span class="sxs-lookup"><span data-stu-id="1cc14-113">-Account</span></span>
<span data-ttu-id="1cc14-114">Nome dell'account in cui aggiornare i criteri di calcolo.</span><span class="sxs-lookup"><span data-stu-id="1cc14-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="1cc14-115">-MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="1cc14-115">-MaxDegreeOfParallelismPerJob</span></span>
<span data-ttu-id="1cc14-116">Il grado di parallelismo massimo supportato per i processi per questo criterio.</span><span class="sxs-lookup"><span data-stu-id="1cc14-116">The maximum supported degree of parallelism per job for this policy.</span></span> <span data-ttu-id="1cc14-117">In questo caso, MinPriorityPerJob o entrambi i parametri devono essere specificati.</span><span class="sxs-lookup"><span data-stu-id="1cc14-117">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="1cc14-118">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="1cc14-118">-MinPriorityPerJob</span></span>
<span data-ttu-id="1cc14-119">Priorità minima supportata per ogni processo per questo criterio.</span><span class="sxs-lookup"><span data-stu-id="1cc14-119">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="1cc14-120">In questo caso, MaxDegreeOfParallelismPerJob o entrambi i parametri devono essere specificati.</span><span class="sxs-lookup"><span data-stu-id="1cc14-120">Either this, MaxDegreeOfParallelismPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="1cc14-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1cc14-121">-Name</span></span>
<span data-ttu-id="1cc14-122">Nome del criterio di calcolo da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="1cc14-122">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="1cc14-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cc14-123">-ResourceGroupName</span></span>
<span data-ttu-id="1cc14-124">Nome del gruppo di risorse in cui è presente l'account.</span><span class="sxs-lookup"><span data-stu-id="1cc14-124">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="1cc14-125">Facoltativo e tenterà di scoprire se non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="1cc14-125">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="1cc14-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1cc14-126">-Confirm</span></span>
<span data-ttu-id="1cc14-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cc14-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cc14-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cc14-128">-WhatIf</span></span>
<span data-ttu-id="1cc14-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1cc14-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1cc14-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1cc14-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cc14-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cc14-131">-DefaultProfile</span></span>
<span data-ttu-id="1cc14-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1cc14-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cc14-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cc14-133">CommonParameters</span></span>
<span data-ttu-id="1cc14-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cc14-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cc14-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cc14-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cc14-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1cc14-136">INPUTS</span></span>

### <span data-ttu-id="1cc14-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1cc14-137">System.String</span></span>
<span data-ttu-id="1cc14-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1cc14-138">System.Int32</span></span>

## <span data-ttu-id="1cc14-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1cc14-139">OUTPUTS</span></span>

### <span data-ttu-id="1cc14-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="1cc14-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="1cc14-141">Note</span><span class="sxs-lookup"><span data-stu-id="1cc14-141">NOTES</span></span>

## <span data-ttu-id="1cc14-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1cc14-142">RELATED LINKS</span></span>


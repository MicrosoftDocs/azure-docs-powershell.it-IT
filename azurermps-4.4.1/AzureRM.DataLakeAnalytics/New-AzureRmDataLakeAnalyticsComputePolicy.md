---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 1dfd9c4d55c9898ce9f4b656f53d7606ced11359
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510671"
---
# <span data-ttu-id="d5fcd-101">New-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="d5fcd-101">New-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="d5fcd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d5fcd-102">SYNOPSIS</span></span>
<span data-ttu-id="d5fcd-103">Crea una regola di criteri di calcolo dei dati per i Lake Analytics per una specifica entità AAD.</span><span class="sxs-lookup"><span data-stu-id="d5fcd-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5fcd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5fcd-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxDegreeOfParallelismPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5fcd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5fcd-105">DESCRIPTION</span></span>
<span data-ttu-id="d5fcd-106">La **nuova AzureRmDataLakeAnalyticsComputePolicy** crea la regola di criteri di calcolo specificata per una specifica entità AAD in un account di analisi di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="d5fcd-106">The **New-AzureRmDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="d5fcd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5fcd-107">EXAMPLES</span></span>

### <span data-ttu-id="d5fcd-108">Esempio 1: creare un criterio di calcolo con una sola regola</span><span class="sxs-lookup"><span data-stu-id="d5fcd-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxDegreeOfParallelismPerJob 5
```

<span data-ttu-id="d5fcd-109">Questo comando crea un criterio denominato "criterio" in account "contosoadla" per l'utente con ID "83cb7ad2-3523-4b82-B909-d478b0d8aea3" che garantisce che non possa inviare alcun processo con più di 5 parallelismi.</span><span class="sxs-lookup"><span data-stu-id="d5fcd-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 parallelism.</span></span>

### <span data-ttu-id="d5fcd-110">Esempio 2: creare un criterio di calcolo con entrambe le regole impostate</span><span class="sxs-lookup"><span data-stu-id="d5fcd-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxDegreeOfParallelismPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="d5fcd-111">Questo comando crea un criterio denominato "criterio" in account "contosoadla" per l'utente con ID "83cb7ad2-3523-4b82-B909-d478b0d8aea3" che garantisce che non può inviare alcun processo con più di 5 parallelismi o con una priorità inferiore a 100</span><span class="sxs-lookup"><span data-stu-id="d5fcd-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 parallelism or with a priority lower than 100</span></span>

## <span data-ttu-id="d5fcd-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d5fcd-112">PARAMETERS</span></span>

### <span data-ttu-id="d5fcd-113">-Account</span><span class="sxs-lookup"><span data-stu-id="d5fcd-113">-Account</span></span>
<span data-ttu-id="d5fcd-114">Nome dell'account a cui aggiungere i criteri di calcolo.</span><span class="sxs-lookup"><span data-stu-id="d5fcd-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="d5fcd-115">-MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="d5fcd-115">-MaxDegreeOfParallelismPerJob</span></span>
<span data-ttu-id="d5fcd-116">Il grado di parallelismo massimo supportato per i processi per questo criterio.</span><span class="sxs-lookup"><span data-stu-id="d5fcd-116">The maximum supported degree of parallelism per job for this policy.</span></span>
<span data-ttu-id="d5fcd-117">In questo caso, MinPriorityPerJob o entrambi i parametri devono essere specificati.</span><span class="sxs-lookup"><span data-stu-id="d5fcd-117">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="d5fcd-118">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="d5fcd-118">-MinPriorityPerJob</span></span>
<span data-ttu-id="d5fcd-119">Priorità minima supportata per ogni processo per questo criterio.</span><span class="sxs-lookup"><span data-stu-id="d5fcd-119">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="d5fcd-120">In questo caso, MaxDegreeOfParallelismPerJob o entrambi i parametri devono essere specificati.</span><span class="sxs-lookup"><span data-stu-id="d5fcd-120">Either this, MaxDegreeOfParallelismPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="d5fcd-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5fcd-121">-Name</span></span>
<span data-ttu-id="d5fcd-122">Nome del criterio di calcolo da creare.</span><span class="sxs-lookup"><span data-stu-id="d5fcd-122">Name of the compute policy to create.</span></span>

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

### <span data-ttu-id="d5fcd-123">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d5fcd-123">-ObjectId</span></span>
<span data-ttu-id="d5fcd-124">ID oggetto di Azure Active Directory per l'utente o il gruppo a cui applicare il criterio.</span><span class="sxs-lookup"><span data-stu-id="d5fcd-124">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5fcd-125">-ObjectType</span><span class="sxs-lookup"><span data-stu-id="d5fcd-125">-ObjectType</span></span>
<span data-ttu-id="d5fcd-126">Tipo di oggetto Azure Active Directory per l'ID oggetto passato.</span><span class="sxs-lookup"><span data-stu-id="d5fcd-126">The Azure Active Directory object type for the object ID passed in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: User, Group, ServicePrincipal

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5fcd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5fcd-127">-ResourceGroupName</span></span>
<span data-ttu-id="d5fcd-128">Nome del gruppo di risorse in cui è presente l'account.</span><span class="sxs-lookup"><span data-stu-id="d5fcd-128">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="d5fcd-129">Facoltativo e tenterà di scoprire se non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="d5fcd-129">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="d5fcd-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d5fcd-130">-Confirm</span></span>
<span data-ttu-id="d5fcd-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5fcd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5fcd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5fcd-132">-WhatIf</span></span>
<span data-ttu-id="d5fcd-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5fcd-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5fcd-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5fcd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5fcd-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5fcd-135">-DefaultProfile</span></span>
<span data-ttu-id="d5fcd-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d5fcd-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5fcd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5fcd-137">CommonParameters</span></span>
<span data-ttu-id="d5fcd-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5fcd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5fcd-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5fcd-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5fcd-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d5fcd-140">INPUTS</span></span>

### <span data-ttu-id="d5fcd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d5fcd-141">System.String</span></span>
<span data-ttu-id="d5fcd-142">System. Guid System. Int32</span><span class="sxs-lookup"><span data-stu-id="d5fcd-142">System.Guid System.Int32</span></span>

## <span data-ttu-id="d5fcd-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5fcd-143">OUTPUTS</span></span>

### <span data-ttu-id="d5fcd-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="d5fcd-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="d5fcd-145">Note</span><span class="sxs-lookup"><span data-stu-id="d5fcd-145">NOTES</span></span>

## <span data-ttu-id="d5fcd-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5fcd-146">RELATED LINKS</span></span>


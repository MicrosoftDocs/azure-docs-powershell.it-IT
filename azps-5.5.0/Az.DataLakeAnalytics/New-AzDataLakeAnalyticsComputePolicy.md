---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 76df1cb780220a09ccc0d571fd88223e746eefe6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204386"
---
# <span data-ttu-id="4d869-101">New-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="4d869-101">New-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="4d869-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d869-102">SYNOPSIS</span></span>
<span data-ttu-id="4d869-103">Crea una regola dei criteri di calcolo Data Lake Analytics per una specifica entità AAD.</span><span class="sxs-lookup"><span data-stu-id="4d869-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="4d869-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d869-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d869-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4d869-105">DESCRIPTION</span></span>
<span data-ttu-id="4d869-106">Il **nuovo valore di AzDataLakeAnalyticsComputePolicy** crea la regola dei criteri di calcolo specificata per una specifica entità AAD in un account Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4d869-106">The **New-AzDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="4d869-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d869-107">EXAMPLES</span></span>

### <span data-ttu-id="4d869-108">Esempio 1: Creare un criterio di calcolo con una sola regola</span><span class="sxs-lookup"><span data-stu-id="4d869-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="4d869-109">Questo comando crea un criterio denominato "myPolicy" nell'account "contosoadla" per l'utente con id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" che assicura che non possa inviare alcun processo con più di 5 unità di analisi.</span><span class="sxs-lookup"><span data-stu-id="4d869-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="4d869-110">Esempio 2: Creare un criterio di calcolo con entrambe le regole impostate</span><span class="sxs-lookup"><span data-stu-id="4d869-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="4d869-111">Questo comando crea un criterio denominato "myPolicy" nell'account "contosoadla" per l'utente con id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" che assicura che non possa inviare alcun processo con più di 5 unità di analisi o con una priorità inferiore a 100</span><span class="sxs-lookup"><span data-stu-id="4d869-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="4d869-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d869-112">PARAMETERS</span></span>

### <span data-ttu-id="4d869-113">-Account</span><span class="sxs-lookup"><span data-stu-id="4d869-113">-Account</span></span>
<span data-ttu-id="4d869-114">Nome dell'account a cui aggiungere il criterio di calcolo.</span><span class="sxs-lookup"><span data-stu-id="4d869-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="4d869-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d869-115">-DefaultProfile</span></span>
<span data-ttu-id="4d869-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="4d869-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d869-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="4d869-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="4d869-118">Il numero massimo di unità di analisi supportate per ogni processo per questo criterio.</span><span class="sxs-lookup"><span data-stu-id="4d869-118">The maximum supported analytics units per job for this policy.</span></span>
<span data-ttu-id="4d869-119">È necessario specificare questo parametro, MinPriorityPerJob o entrambi i parametri.</span><span class="sxs-lookup"><span data-stu-id="4d869-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="4d869-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="4d869-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="4d869-121">Priorità minima supportata per ogni processo per questo criterio.</span><span class="sxs-lookup"><span data-stu-id="4d869-121">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="4d869-122">In entrambi i casi, è necessario specificare MaxAnalyticsUnitsPerJob o entrambi i parametri.</span><span class="sxs-lookup"><span data-stu-id="4d869-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="4d869-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4d869-123">-Name</span></span>
<span data-ttu-id="4d869-124">Nome del criterio di calcolo da creare.</span><span class="sxs-lookup"><span data-stu-id="4d869-124">Name of the compute policy to create.</span></span>

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

### <span data-ttu-id="4d869-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4d869-125">-ObjectId</span></span>
<span data-ttu-id="4d869-126">ID oggetto di Azure Active Directory a cui l'utente o il gruppo applica il criterio.</span><span class="sxs-lookup"><span data-stu-id="4d869-126">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

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

### <span data-ttu-id="4d869-127">-ObjectType</span><span class="sxs-lookup"><span data-stu-id="4d869-127">-ObjectType</span></span>
<span data-ttu-id="4d869-128">Tipo di oggetto Azure Active Directory per l'ID oggetto passato.</span><span class="sxs-lookup"><span data-stu-id="4d869-128">The Azure Active Directory object type for the object ID passed in.</span></span>

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

### <span data-ttu-id="4d869-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d869-129">-ResourceGroupName</span></span>
<span data-ttu-id="4d869-130">Nome del gruppo di risorse in cui esiste l'account.</span><span class="sxs-lookup"><span data-stu-id="4d869-130">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="4d869-131">Facoltativo e tenterà di individuarne l'errore, se non specificato.</span><span class="sxs-lookup"><span data-stu-id="4d869-131">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="4d869-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d869-132">-Confirm</span></span>
<span data-ttu-id="4d869-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d869-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d869-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d869-134">-WhatIf</span></span>
<span data-ttu-id="4d869-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d869-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d869-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d869-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d869-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d869-137">CommonParameters</span></span>
<span data-ttu-id="4d869-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d869-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d869-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d869-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d869-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="4d869-140">INPUTS</span></span>

### <span data-ttu-id="4d869-141">System.String</span><span class="sxs-lookup"><span data-stu-id="4d869-141">System.String</span></span>

### <span data-ttu-id="4d869-142">System.Guid</span><span class="sxs-lookup"><span data-stu-id="4d869-142">System.Guid</span></span>

### <span data-ttu-id="4d869-143">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4d869-143">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4d869-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d869-144">OUTPUTS</span></span>

### <span data-ttu-id="4d869-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="4d869-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="4d869-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="4d869-146">NOTES</span></span>

## <span data-ttu-id="4d869-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d869-147">RELATED LINKS</span></span>

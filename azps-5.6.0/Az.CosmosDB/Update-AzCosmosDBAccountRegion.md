---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbaccountregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
ms.openlocfilehash: 643cdbf8aa0aed98dba7497fa0107d8d81583bba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958830"
---
# <span data-ttu-id="e9178-101">Update-AzCosmosDBAccountRegion</span><span class="sxs-lookup"><span data-stu-id="e9178-101">Update-AzCosmosDBAccountRegion</span></span>

## <span data-ttu-id="e9178-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9178-102">SYNOPSIS</span></span>
<span data-ttu-id="e9178-103">Aggiornare le aree geografiche di un account diDbDb.</span><span class="sxs-lookup"><span data-stu-id="e9178-103">Update Regions of a CosmosDB Account.</span></span>

## <span data-ttu-id="e9178-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9178-104">SYNTAX</span></span>

### <span data-ttu-id="e9178-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e9178-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountRegion -ResourceGroupName <String> -Name <String> [-Location <String[]>]
 [-LocationObject <PSLocation[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9178-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9178-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9178-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9178-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>]
 -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9178-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e9178-108">DESCRIPTION</span></span>
<span data-ttu-id="e9178-109">Aggiornare le aree geografiche di un account diDbDb.</span><span class="sxs-lookup"><span data-stu-id="e9178-109">Update Regions of a CosmosDB Account.</span></span> <span data-ttu-id="e9178-110">La posizione può essere fornita come oggetto di tipo PSLocation o come stringa di Nome posizione ordinata in base alla priorità di failover.</span><span class="sxs-lookup"><span data-stu-id="e9178-110">Location can be provided either as an object of type PSLocation or as strings of Location Name ordered by failover priority.</span></span>
<span data-ttu-id="e9178-111">Il parametro LocationObject prevede l'aggiunta dell'elenco delle posizioni correnti (priorità di failover incluse) aggiunto dai nuovi LocationObjects corrispondenti alle nuove posizioni.</span><span class="sxs-lookup"><span data-stu-id="e9178-111">LocationObject parameter expects the list of current locations (failover prioritiies included) appended by the new LocationObjects corresponding to new locations to be added.</span></span>
<span data-ttu-id="e9178-112">Il parametro Location prevede l'elenco della posizione corrente (ordinata in base alla priorità di failover) e delle nuove posizioni.</span><span class="sxs-lookup"><span data-stu-id="e9178-112">Location parameter expects the list of current location(ordered by failover priority) and the new locations.</span></span> <span data-ttu-id="e9178-113">Tieni presente che supportiamo solo l'aggiunta di aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="e9178-113">Please note, we only support Addition of Regions.</span></span> <span data-ttu-id="e9178-114">Specifica Location o LocationObject.</span><span class="sxs-lookup"><span data-stu-id="e9178-114">Please provide either Location or LocationObject.</span></span>

## <span data-ttu-id="e9178-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9178-115">EXAMPLES</span></span>

### <span data-ttu-id="e9178-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e9178-116">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountRegion -ResourceGroupName rg1 -Name dbname -Location "location1, location2"

Kind                          : GlobalDocumentDB
ProvisioningState             : Succeeded
DocumentEndpoint              : https://dbname.documents.azure.com:443/
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : False
EnableAutomaticFailover       : False
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Fluent.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {dbname-location1}
ReadLocations                 : {dbname-location2}
FailoverPolicies              : {dbname-location1, dbname-location2}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
Location                      : location1
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/rg1/providers/Microsoft.DocumentDB/databaseAccounts/dbname
Name                          : dbname
Type                          : Microsoft.DocumentDB/databaseAccounts
```

## <span data-ttu-id="e9178-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9178-117">PARAMETERS</span></span>

### <span data-ttu-id="e9178-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9178-118">-AsJob</span></span>
<span data-ttu-id="e9178-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e9178-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9178-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9178-120">-Confirm</span></span>
<span data-ttu-id="e9178-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9178-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9178-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9178-122">-DefaultProfile</span></span>
<span data-ttu-id="e9178-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e9178-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9178-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9178-124">-InputObject</span></span>
<span data-ttu-id="e9178-125">ResourceId della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e9178-125">ResourceId of the resource.</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9178-126">-Location</span><span class="sxs-lookup"><span data-stu-id="e9178-126">-Location</span></span>
<span data-ttu-id="e9178-127">Nome della posizione da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="e9178-127">Name of the location to be added.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9178-128">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="e9178-128">-LocationObject</span></span>
<span data-ttu-id="e9178-129">Aggiungere una posizione all'account di database DB di Coeli.</span><span class="sxs-lookup"><span data-stu-id="e9178-129">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="e9178-130">Matrice di oggetti PSLocation.</span><span class="sxs-lookup"><span data-stu-id="e9178-130">Array of PSLocation objects.</span></span>

```yaml
Type: PSLocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9178-131">-Name</span><span class="sxs-lookup"><span data-stu-id="e9178-131">-Name</span></span>
<span data-ttu-id="e9178-132">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="e9178-132">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9178-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9178-133">-ResourceGroupName</span></span>
<span data-ttu-id="e9178-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e9178-134">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9178-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9178-135">-ResourceId</span></span>
<span data-ttu-id="e9178-136">ResourceId della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e9178-136">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9178-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9178-137">-WhatIf</span></span>
<span data-ttu-id="e9178-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e9178-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9178-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e9178-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9178-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9178-140">CommonParameters</span></span>
<span data-ttu-id="e9178-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9178-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9178-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e9178-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9178-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="e9178-143">INPUTS</span></span>

### <span data-ttu-id="e9178-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e9178-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e9178-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9178-145">OUTPUTS</span></span>

### <span data-ttu-id="e9178-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e9178-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e9178-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="e9178-147">NOTES</span></span>

## <span data-ttu-id="e9178-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9178-148">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
ms.openlocfilehash: bfbbc0b4d5fbaac1dc6ad5f18af2cb201e5124c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190332"
---
# <span data-ttu-id="c2456-101">Update-AzCosmosDBAccountRegion</span><span class="sxs-lookup"><span data-stu-id="c2456-101">Update-AzCosmosDBAccountRegion</span></span>

## <span data-ttu-id="c2456-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2456-102">SYNOPSIS</span></span>
<span data-ttu-id="c2456-103">Aggiornare le aree geografiche di un account di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c2456-103">Update Regions of a CosmosDB Account.</span></span>

## <span data-ttu-id="c2456-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2456-104">SYNTAX</span></span>

### <span data-ttu-id="c2456-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c2456-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountRegion -ResourceGroupName <String> -Name <String> [-Location <String[]>]
 [-LocationObject <PSLocation[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2456-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2456-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2456-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2456-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>]
 -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2456-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2456-108">DESCRIPTION</span></span>
<span data-ttu-id="c2456-109">Aggiornare le aree geografiche di un account di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="c2456-109">Update Regions of a CosmosDB Account.</span></span> <span data-ttu-id="c2456-110">La posizione può essere fornita come oggetto di tipo PSLocation o come stringhe di nome di posizione ordinate per priorità di failover.</span><span class="sxs-lookup"><span data-stu-id="c2456-110">Location can be provided either as an object of type PSLocation or as strings of Location Name ordered by failover priority.</span></span>
<span data-ttu-id="c2456-111">Il parametro LocationObject prevede l'elenco delle posizioni correnti (il failover prioritiies incluso) accodato dal nuovo LocationObjects che corrisponde a nuove posizioni da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="c2456-111">LocationObject parameter expects the list of current locations (failover prioritiies included) appended by the new LocationObjects corresponding to new locations to be added.</span></span>
<span data-ttu-id="c2456-112">Il parametro location prevede l'elenco della posizione corrente (ordinata per priorità di failover) e delle nuove posizioni.</span><span class="sxs-lookup"><span data-stu-id="c2456-112">Location parameter expects the list of current location(ordered by failover priority) and the new locations.</span></span> <span data-ttu-id="c2456-113">Tieni presente che supportiamo solo l'aggiunta di aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="c2456-113">Please note, we only support Addition of Regions.</span></span> <span data-ttu-id="c2456-114">Fornisci una posizione o LocationObject.</span><span class="sxs-lookup"><span data-stu-id="c2456-114">Please provide either Location or LocationObject.</span></span>

## <span data-ttu-id="c2456-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2456-115">EXAMPLES</span></span>

### <span data-ttu-id="c2456-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c2456-116">Example 1</span></span>
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

## <span data-ttu-id="c2456-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2456-117">PARAMETERS</span></span>

### <span data-ttu-id="c2456-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2456-118">-AsJob</span></span>
<span data-ttu-id="c2456-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c2456-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2456-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c2456-120">-Confirm</span></span>
<span data-ttu-id="c2456-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2456-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2456-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2456-122">-DefaultProfile</span></span>
<span data-ttu-id="c2456-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c2456-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2456-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2456-124">-InputObject</span></span>
<span data-ttu-id="c2456-125">ResourceId della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c2456-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="c2456-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c2456-126">-Location</span></span>
<span data-ttu-id="c2456-127">Nome della posizione da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="c2456-127">Name of the location to be added.</span></span>

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

### <span data-ttu-id="c2456-128">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="c2456-128">-LocationObject</span></span>
<span data-ttu-id="c2456-129">Aggiungere una posizione all'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="c2456-129">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="c2456-130">Matrice di oggetti PSLocation.</span><span class="sxs-lookup"><span data-stu-id="c2456-130">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="c2456-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2456-131">-Name</span></span>
<span data-ttu-id="c2456-132">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="c2456-132">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c2456-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2456-133">-ResourceGroupName</span></span>
<span data-ttu-id="c2456-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c2456-134">Name of resource group.</span></span>

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

### <span data-ttu-id="c2456-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2456-135">-ResourceId</span></span>
<span data-ttu-id="c2456-136">ResourceId della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c2456-136">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="c2456-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2456-137">-WhatIf</span></span>
<span data-ttu-id="c2456-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2456-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2456-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2456-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2456-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2456-140">CommonParameters</span></span>
<span data-ttu-id="c2456-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2456-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2456-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2456-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2456-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2456-143">INPUTS</span></span>

### <span data-ttu-id="c2456-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="c2456-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="c2456-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2456-145">OUTPUTS</span></span>

### <span data-ttu-id="c2456-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="c2456-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="c2456-147">Note</span><span class="sxs-lookup"><span data-stu-id="c2456-147">NOTES</span></span>

## <span data-ttu-id="c2456-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2456-148">RELATED LINKS</span></span>
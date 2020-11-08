---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 76df37703882e799eb42542cd08d105f62787419
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020523"
---
# <span data-ttu-id="7c233-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="7c233-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="7c233-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c233-102">SYNOPSIS</span></span>
<span data-ttu-id="7c233-103">Creare un nuovo account di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="7c233-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="7c233-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c233-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork] [-IpRangeFilter <String[]>]
 [-Location <String[]>] [-LocationObject <PSLocation[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-ApiKind <String>] [-PublicNetworkAccess <String>]
 [-DisableKeyBasedMetadataWriteAccess] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7c233-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c233-105">DESCRIPTION</span></span>
<span data-ttu-id="7c233-106">Creare un nuovo account di CosmosDB nella ResourceGroup specificata.</span><span class="sxs-lookup"><span data-stu-id="7c233-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="7c233-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c233-107">EXAMPLES</span></span>

### <span data-ttu-id="7c233-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c233-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name databaseAccountName  -Location "East US"

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : False
EnableAutomaticFailover       : False
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {databaseAccountName-eastus}
ReadLocations                 : {databaseAccountName-eastus}
FailoverPolicies              : {databaseAccountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/databaseAccountName
Name                          : databaseAccountName
Type                          : Microsoft.DocumentDB/databaseAccounts
```

<span data-ttu-id="7c233-109">In ResourceGroup resourceGroupName viene creato un nuovo account di CosmosDB con nome databaseAccountName.</span><span class="sxs-lookup"><span data-stu-id="7c233-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="7c233-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c233-110">PARAMETERS</span></span>

### <span data-ttu-id="7c233-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="7c233-111">-ApiKind</span></span>
<span data-ttu-id="7c233-112">Il tipo di account di database DB Cosmos da creare.</span><span class="sxs-lookup"><span data-stu-id="7c233-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="7c233-113">Valori accettati: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="7c233-113">Accepted values: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="7c233-114">Valore predefinito: GlobalDocumentDB</span><span class="sxs-lookup"><span data-stu-id="7c233-114">Default value: GlobalDocumentDB</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c233-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c233-115">-AsJob</span></span>
<span data-ttu-id="7c233-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7c233-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c233-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7c233-117">-Confirm</span></span>
<span data-ttu-id="7c233-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c233-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c233-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="7c233-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="7c233-120">Livello di coerenza predefinito dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="7c233-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="7c233-121">Valori accettati: BoundedStaleness, ConsistentPrefix, eventuale, sessione, Strong</span><span class="sxs-lookup"><span data-stu-id="7c233-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c233-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c233-122">-DefaultProfile</span></span>
<span data-ttu-id="7c233-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c233-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c233-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="7c233-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="7c233-125">Disabilitare le operazioni di scrittura sulle risorse dei metadati (database, contenitori, throughput) tramite i tasti account</span><span class="sxs-lookup"><span data-stu-id="7c233-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="7c233-126">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="7c233-126">-EnableAutomaticFailover</span></span>
<span data-ttu-id="7c233-127">Consente il failover automatico dell'area di scrittura nell'evento raro che l'area non è disponibile a causa di un'interruzione.</span><span class="sxs-lookup"><span data-stu-id="7c233-127">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="7c233-128">Il failover automatico comporterà una nuova area di scrittura per l'account e verrà scelto in base alle priorità di failover configurate per l'account.</span><span class="sxs-lookup"><span data-stu-id="7c233-128">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="7c233-129">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="7c233-129">Accepted values: false, true</span></span>

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

### <span data-ttu-id="7c233-130">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="7c233-130">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="7c233-131">Abilitare più posizioni di scrittura.</span><span class="sxs-lookup"><span data-stu-id="7c233-131">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="7c233-132">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="7c233-132">Accepted values: false, true</span></span>

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

### <span data-ttu-id="7c233-133">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7c233-133">-EnableVirtualNetwork</span></span>
<span data-ttu-id="7c233-134">Abilita la rete virtuale nell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="7c233-134">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="7c233-135">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="7c233-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="7c233-136">-IpRangeFilter</span><span class="sxs-lookup"><span data-stu-id="7c233-136">-IpRangeFilter</span></span>
<span data-ttu-id="7c233-137">Supporto firewall.</span><span class="sxs-lookup"><span data-stu-id="7c233-137">Firewall support.</span></span>
<span data-ttu-id="7c233-138">Specifica il set di indirizzi IP o intervalli di indirizzi IP in formato CIDR da includere come elenco consentito di IPs client per un dato account di database</span><span class="sxs-lookup"><span data-stu-id="7c233-138">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account</span></span>

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

### <span data-ttu-id="7c233-139">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7c233-139">-Location</span></span>
<span data-ttu-id="7c233-140">Aggiungere una posizione all'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="7c233-140">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="7c233-141">Matrice di stringhe, ordinate per priorità di failover.</span><span class="sxs-lookup"><span data-stu-id="7c233-141">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="7c233-142">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="7c233-142">-LocationObject</span></span>
<span data-ttu-id="7c233-143">Aggiungere una posizione all'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="7c233-143">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="7c233-144">Matrice di oggetti PSLocation.</span><span class="sxs-lookup"><span data-stu-id="7c233-144">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="7c233-145">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="7c233-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="7c233-146">Se usato con coerenza di obsolescenza limitata, questo valore rappresenta la quantità di tempo di obsolescenza (in TimeSpan) tollerata.</span><span class="sxs-lookup"><span data-stu-id="7c233-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="7c233-147">L'intervallo accettato per questo valore è 5-86400.</span><span class="sxs-lookup"><span data-stu-id="7c233-147">Accepted range for this value is 5-86400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c233-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="7c233-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="7c233-149">Se usato con coerenza di obsolescenza limitata, questo valore rappresenta il numero di richieste non aggiornate tollerate.</span><span class="sxs-lookup"><span data-stu-id="7c233-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="7c233-150">L'intervallo accettato per questo valore è 1-2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="7c233-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c233-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c233-151">-Name</span></span>
<span data-ttu-id="7c233-152">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="7c233-152">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c233-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="7c233-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="7c233-154">Indipendentemente dal fatto che sia consentito o meno l'accesso endpoint pubblico per il server.</span><span class="sxs-lookup"><span data-stu-id="7c233-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="7c233-155">I valori possibili includono:' Enabled ',' disabled '</span><span class="sxs-lookup"><span data-stu-id="7c233-155">Possible values include: 'Enabled', 'Disabled'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c233-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c233-156">-ResourceGroupName</span></span>
<span data-ttu-id="7c233-157">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7c233-157">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c233-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="7c233-158">-Tag</span></span>
<span data-ttu-id="7c233-159">Hashtable di tag come coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="7c233-159">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="7c233-160">Usa una stringa vuota per cancellare il tag esistente.</span><span class="sxs-lookup"><span data-stu-id="7c233-160">Use empty string to clear existing tag.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c233-161">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7c233-161">-VirtualNetworkRule</span></span>
<span data-ttu-id="7c233-162">Matrice di valori stringa di ACL per la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="7c233-162">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="7c233-163">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="7c233-163">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="7c233-164">Matrice di PSVirtualNetworkRuleObjects for Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="7c233-164">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c233-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c233-165">-WhatIf</span></span>
<span data-ttu-id="7c233-166">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c233-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c233-167">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c233-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c233-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c233-168">CommonParameters</span></span>
<span data-ttu-id="7c233-169">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c233-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c233-170">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c233-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c233-171">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c233-171">INPUTS</span></span>

### <span data-ttu-id="7c233-172">Microsoft. Azure. Commands. CosmosDB. Models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="7c233-172">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="7c233-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c233-173">OUTPUTS</span></span>

### <span data-ttu-id="7c233-174">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="7c233-174">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="7c233-175">Note</span><span class="sxs-lookup"><span data-stu-id="7c233-175">NOTES</span></span>

## <span data-ttu-id="7c233-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c233-176">RELATED LINKS</span></span>

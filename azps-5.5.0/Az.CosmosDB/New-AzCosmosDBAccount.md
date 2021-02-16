---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 810888885c53381c274f85dc79ea2dd7bd4492c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198990"
---
# <span data-ttu-id="ad233-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="ad233-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="ad233-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad233-102">SYNOPSIS</span></span>
<span data-ttu-id="ad233-103">Creare un nuovo account diDbDb.</span><span class="sxs-lookup"><span data-stu-id="ad233-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="ad233-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad233-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork]
 [-ApiKind <String>] [-DisableKeyBasedMetadataWriteAccess] [-EnableFreeTier <Boolean>]
 [-ServerVersion <String>] [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad233-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ad233-105">DESCRIPTION</span></span>
<span data-ttu-id="ad233-106">Creare un nuovo account diDbDb nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="ad233-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="ad233-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad233-107">EXAMPLES</span></span>

### <span data-ttu-id="ad233-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ad233-108">Example 1</span></span>
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

<span data-ttu-id="ad233-109">In ResourceGroup resourceGroupName viene creato un nuovo accountDbDb con nome databaseAccountName.</span><span class="sxs-lookup"><span data-stu-id="ad233-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="ad233-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad233-110">PARAMETERS</span></span>

### <span data-ttu-id="ad233-111">-Api Riepi</span><span class="sxs-lookup"><span data-stu-id="ad233-111">-ApiKind</span></span>
<span data-ttu-id="ad233-112">Tipo di account di database DB di Ofovas da creare.</span><span class="sxs-lookup"><span data-stu-id="ad233-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="ad233-113">Valori accettati: Sql, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="ad233-113">Accepted values: Sql, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="ad233-114">Valore predefinito: Sql</span><span class="sxs-lookup"><span data-stu-id="ad233-114">Default value: Sql</span></span>

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

### <span data-ttu-id="ad233-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad233-115">-AsJob</span></span>
<span data-ttu-id="ad233-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ad233-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ad233-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad233-117">-Confirm</span></span>
<span data-ttu-id="ad233-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad233-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad233-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="ad233-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="ad233-120">Livello di coerenza predefinito dell'account di database DB di Coeli.</span><span class="sxs-lookup"><span data-stu-id="ad233-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="ad233-121">Valori accettati: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="ad233-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="ad233-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad233-122">-DefaultProfile</span></span>
<span data-ttu-id="ad233-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad233-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad233-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="ad233-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="ad233-125">Disabilitare le operazioni di scrittura su risorse di metadati (database, contenitori e velocità effettiva) tramite chiavi account</span><span class="sxs-lookup"><span data-stu-id="ad233-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="ad233-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="ad233-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="ad233-127">Bool per indicare se AnalyticalStorage è abilitato per l'account.</span><span class="sxs-lookup"><span data-stu-id="ad233-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad233-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="ad233-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="ad233-129">Abilita il failover automatico dell'area di scrittura nei rari casi in cui l'area non sia disponibile a causa di un'interruzione.</span><span class="sxs-lookup"><span data-stu-id="ad233-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="ad233-130">Il failover automatico causa una nuova area di scrittura per l'account e viene scelto in base alle priorità di failover configurate per l'account.</span><span class="sxs-lookup"><span data-stu-id="ad233-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="ad233-131">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="ad233-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="ad233-132">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="ad233-132">-EnableFreeTier</span></span>
<span data-ttu-id="ad233-133">Bool per indicare se FreeTier è abilitato per l'account.</span><span class="sxs-lookup"><span data-stu-id="ad233-133">Bool to indicate if FreeTier is enabled on the account.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad233-134">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="ad233-134">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="ad233-135">Abilitare più posizioni di scrittura.</span><span class="sxs-lookup"><span data-stu-id="ad233-135">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="ad233-136">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="ad233-136">Accepted values: false, true</span></span>

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

### <span data-ttu-id="ad233-137">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ad233-137">-EnableVirtualNetwork</span></span>
<span data-ttu-id="ad233-138">Abilita la rete virtuale nell'account di database DB di Coelige.</span><span class="sxs-lookup"><span data-stu-id="ad233-138">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="ad233-139">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="ad233-139">Accepted values: false, true</span></span>

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

### <span data-ttu-id="ad233-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="ad233-140">-IpRule</span></span>
<span data-ttu-id="ad233-141">Supporto del firewall.</span><span class="sxs-lookup"><span data-stu-id="ad233-141">Firewall support.</span></span> <span data-ttu-id="ad233-142">Specifica il set di indirizzi IP o intervalli di indirizzi IP in formato CIDR da includere nell'elenco di INDIRIZZI IP client consentiti per un determinato account di database.</span><span class="sxs-lookup"><span data-stu-id="ad233-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="ad233-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="ad233-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="ad233-144">URI della proprietà KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad233-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="ad233-145">-Location</span><span class="sxs-lookup"><span data-stu-id="ad233-145">-Location</span></span>
<span data-ttu-id="ad233-146">Aggiungere una posizione all'account di database DB di Coeli.</span><span class="sxs-lookup"><span data-stu-id="ad233-146">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="ad233-147">Matrice di stringhe ordinata in base alla priorità di failover.</span><span class="sxs-lookup"><span data-stu-id="ad233-147">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="ad233-148">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="ad233-148">-LocationObject</span></span>
<span data-ttu-id="ad233-149">Aggiungere una posizione all'account di database DB di Coeli.</span><span class="sxs-lookup"><span data-stu-id="ad233-149">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="ad233-150">Matrice di oggetti PSLocation.</span><span class="sxs-lookup"><span data-stu-id="ad233-150">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="ad233-151">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="ad233-151">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="ad233-152">Quando viene usato con la coerenza della coerenza dei dati associati, questo valore rappresenta la quantità di tempo non utile (nell'intervallo di tempo).</span><span class="sxs-lookup"><span data-stu-id="ad233-152">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="ad233-153">L'intervallo accettato per questo valore è 5-86400.</span><span class="sxs-lookup"><span data-stu-id="ad233-153">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="ad233-154">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="ad233-154">-MaxStalenessPrefix</span></span>
<span data-ttu-id="ad233-155">Quando viene usato con la coerenza della coerenza dei dati associati, questo valore rappresenta il numero di richieste non più corrette.</span><span class="sxs-lookup"><span data-stu-id="ad233-155">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="ad233-156">L'intervallo accettato per questo valore è 1 - 2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="ad233-156">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="ad233-157">-Name</span><span class="sxs-lookup"><span data-stu-id="ad233-157">-Name</span></span>
<span data-ttu-id="ad233-158">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="ad233-158">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ad233-159">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="ad233-159">-PublicNetworkAccess</span></span>
<span data-ttu-id="ad233-160">Se l'accesso all'endpoint pubblico è consentito o meno per questo server.</span><span class="sxs-lookup"><span data-stu-id="ad233-160">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="ad233-161">I valori possibili includono: 'Abilitato', 'Disabilitato'</span><span class="sxs-lookup"><span data-stu-id="ad233-161">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="ad233-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad233-162">-ResourceGroupName</span></span>
<span data-ttu-id="ad233-163">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ad233-163">Name of resource group.</span></span>

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

### <span data-ttu-id="ad233-164">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="ad233-164">-ServerVersion</span></span>
<span data-ttu-id="ad233-165">ServerVersion, valido solo nel caso di account MongoDB.</span><span class="sxs-lookup"><span data-stu-id="ad233-165">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="ad233-166">-Tag</span><span class="sxs-lookup"><span data-stu-id="ad233-166">-Tag</span></span>
<span data-ttu-id="ad233-167">Tabella hash di tag come coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="ad233-167">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="ad233-168">Usare una stringa vuota per cancellare il tag esistente.</span><span class="sxs-lookup"><span data-stu-id="ad233-168">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="ad233-169">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ad233-169">-VirtualNetworkRule</span></span>
<span data-ttu-id="ad233-170">Matrice dei valori stringa degli ACL per la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ad233-170">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="ad233-171">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="ad233-171">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="ad233-172">Matrice di PSVirtualNetworkRuleObjects per la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ad233-172">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="ad233-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad233-173">-WhatIf</span></span>
<span data-ttu-id="ad233-174">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad233-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad233-175">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad233-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad233-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad233-176">CommonParameters</span></span>
<span data-ttu-id="ad233-177">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad233-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad233-178">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ad233-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad233-179">INPUT</span><span class="sxs-lookup"><span data-stu-id="ad233-179">INPUTS</span></span>

### <span data-ttu-id="ad233-180">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="ad233-180">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="ad233-181">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad233-181">OUTPUTS</span></span>

### <span data-ttu-id="ad233-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="ad233-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="ad233-183">NOTE</span><span class="sxs-lookup"><span data-stu-id="ad233-183">NOTES</span></span>

## <span data-ttu-id="ad233-184">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad233-184">RELATED LINKS</span></span>

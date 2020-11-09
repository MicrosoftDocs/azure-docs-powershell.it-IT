---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: f082f9390dd5a00fa5984aa2e0df26e8c3b63636
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299389"
---
# <span data-ttu-id="3b380-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="3b380-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="3b380-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b380-102">SYNOPSIS</span></span>
<span data-ttu-id="3b380-103">Creare un nuovo account di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="3b380-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="3b380-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b380-104">SYNTAX</span></span>

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

## <span data-ttu-id="3b380-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b380-105">DESCRIPTION</span></span>
<span data-ttu-id="3b380-106">Creare un nuovo account di CosmosDB nella ResourceGroup specificata.</span><span class="sxs-lookup"><span data-stu-id="3b380-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="3b380-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b380-107">EXAMPLES</span></span>

### <span data-ttu-id="3b380-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3b380-108">Example 1</span></span>
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

<span data-ttu-id="3b380-109">In ResourceGroup resourceGroupName viene creato un nuovo account di CosmosDB con nome databaseAccountName.</span><span class="sxs-lookup"><span data-stu-id="3b380-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="3b380-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b380-110">PARAMETERS</span></span>

### <span data-ttu-id="3b380-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="3b380-111">-ApiKind</span></span>
<span data-ttu-id="3b380-112">Il tipo di account di database DB Cosmos da creare.</span><span class="sxs-lookup"><span data-stu-id="3b380-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="3b380-113">Valori accettati: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="3b380-113">Accepted values: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="3b380-114">Valore predefinito: GlobalDocumentDB</span><span class="sxs-lookup"><span data-stu-id="3b380-114">Default value: GlobalDocumentDB</span></span>

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

### <span data-ttu-id="3b380-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b380-115">-AsJob</span></span>
<span data-ttu-id="3b380-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3b380-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3b380-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3b380-117">-Confirm</span></span>
<span data-ttu-id="3b380-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b380-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b380-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="3b380-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="3b380-120">Livello di coerenza predefinito dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="3b380-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="3b380-121">Valori accettati: BoundedStaleness, ConsistentPrefix, eventuale, sessione, Strong</span><span class="sxs-lookup"><span data-stu-id="3b380-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="3b380-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b380-122">-DefaultProfile</span></span>
<span data-ttu-id="3b380-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b380-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b380-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="3b380-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="3b380-125">Disabilitare le operazioni di scrittura sulle risorse dei metadati (database, contenitori, throughput) tramite i tasti account</span><span class="sxs-lookup"><span data-stu-id="3b380-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="3b380-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="3b380-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="3b380-127">Bool per indicare se AnalyticalStorage è abilitato per l'account.</span><span class="sxs-lookup"><span data-stu-id="3b380-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="3b380-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="3b380-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="3b380-129">Consente il failover automatico dell'area di scrittura nell'evento raro che l'area non è disponibile a causa di un'interruzione.</span><span class="sxs-lookup"><span data-stu-id="3b380-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="3b380-130">Il failover automatico comporterà una nuova area di scrittura per l'account e verrà scelto in base alle priorità di failover configurate per l'account.</span><span class="sxs-lookup"><span data-stu-id="3b380-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="3b380-131">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="3b380-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="3b380-132">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="3b380-132">-EnableFreeTier</span></span>
<span data-ttu-id="3b380-133">Bool per indicare se FreeTier è abilitato per l'account.</span><span class="sxs-lookup"><span data-stu-id="3b380-133">Bool to indicate if FreeTier is enabled on the account.</span></span>

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

### <span data-ttu-id="3b380-134">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="3b380-134">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="3b380-135">Abilitare più posizioni di scrittura.</span><span class="sxs-lookup"><span data-stu-id="3b380-135">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="3b380-136">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="3b380-136">Accepted values: false, true</span></span>

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

### <span data-ttu-id="3b380-137">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3b380-137">-EnableVirtualNetwork</span></span>
<span data-ttu-id="3b380-138">Abilita la rete virtuale nell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="3b380-138">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="3b380-139">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="3b380-139">Accepted values: false, true</span></span>

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

### <span data-ttu-id="3b380-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="3b380-140">-IpRule</span></span>
<span data-ttu-id="3b380-141">Supporto firewall.</span><span class="sxs-lookup"><span data-stu-id="3b380-141">Firewall support.</span></span> <span data-ttu-id="3b380-142">Specifica il set di indirizzi IP o intervalli di indirizzi IP in formato CIDR da includere come elenco consentito di IPs client per un dato account di database.</span><span class="sxs-lookup"><span data-stu-id="3b380-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="3b380-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="3b380-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="3b380-144">URI del Vault</span><span class="sxs-lookup"><span data-stu-id="3b380-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="3b380-145">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3b380-145">-Location</span></span>
<span data-ttu-id="3b380-146">Aggiungere una posizione all'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="3b380-146">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="3b380-147">Matrice di stringhe, ordinate per priorità di failover.</span><span class="sxs-lookup"><span data-stu-id="3b380-147">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="3b380-148">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="3b380-148">-LocationObject</span></span>
<span data-ttu-id="3b380-149">Aggiungere una posizione all'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="3b380-149">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="3b380-150">Matrice di oggetti PSLocation.</span><span class="sxs-lookup"><span data-stu-id="3b380-150">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="3b380-151">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="3b380-151">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="3b380-152">Se usato con coerenza di obsolescenza limitata, questo valore rappresenta la quantità di tempo di obsolescenza (in TimeSpan) tollerata.</span><span class="sxs-lookup"><span data-stu-id="3b380-152">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="3b380-153">L'intervallo accettato per questo valore è 5-86400.</span><span class="sxs-lookup"><span data-stu-id="3b380-153">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="3b380-154">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="3b380-154">-MaxStalenessPrefix</span></span>
<span data-ttu-id="3b380-155">Se usato con coerenza di obsolescenza limitata, questo valore rappresenta il numero di richieste non aggiornate tollerate.</span><span class="sxs-lookup"><span data-stu-id="3b380-155">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="3b380-156">L'intervallo accettato per questo valore è 1-2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="3b380-156">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="3b380-157">-Nome</span><span class="sxs-lookup"><span data-stu-id="3b380-157">-Name</span></span>
<span data-ttu-id="3b380-158">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="3b380-158">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3b380-159">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="3b380-159">-PublicNetworkAccess</span></span>
<span data-ttu-id="3b380-160">Indipendentemente dal fatto che sia consentito o meno l'accesso endpoint pubblico per il server.</span><span class="sxs-lookup"><span data-stu-id="3b380-160">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="3b380-161">I valori possibili includono:' Enabled ',' disabled '</span><span class="sxs-lookup"><span data-stu-id="3b380-161">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="3b380-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b380-162">-ResourceGroupName</span></span>
<span data-ttu-id="3b380-163">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3b380-163">Name of resource group.</span></span>

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

### <span data-ttu-id="3b380-164">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="3b380-164">-ServerVersion</span></span>
<span data-ttu-id="3b380-165">ServerVersion, valido solo in caso di account MongoDB.</span><span class="sxs-lookup"><span data-stu-id="3b380-165">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="3b380-166">-Tag</span><span class="sxs-lookup"><span data-stu-id="3b380-166">-Tag</span></span>
<span data-ttu-id="3b380-167">Hashtable di tag come coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="3b380-167">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="3b380-168">Usa una stringa vuota per cancellare il tag esistente.</span><span class="sxs-lookup"><span data-stu-id="3b380-168">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="3b380-169">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3b380-169">-VirtualNetworkRule</span></span>
<span data-ttu-id="3b380-170">Matrice di valori stringa di ACL per la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="3b380-170">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="3b380-171">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="3b380-171">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="3b380-172">Matrice di PSVirtualNetworkRuleObjects for Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="3b380-172">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="3b380-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b380-173">-WhatIf</span></span>
<span data-ttu-id="3b380-174">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b380-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b380-175">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3b380-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b380-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b380-176">CommonParameters</span></span>
<span data-ttu-id="3b380-177">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b380-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b380-178">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b380-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b380-179">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b380-179">INPUTS</span></span>

### <span data-ttu-id="3b380-180">Microsoft. Azure. Commands. CosmosDB. Models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="3b380-180">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="3b380-181">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b380-181">OUTPUTS</span></span>

### <span data-ttu-id="3b380-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="3b380-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="3b380-183">Note</span><span class="sxs-lookup"><span data-stu-id="3b380-183">NOTES</span></span>

## <span data-ttu-id="3b380-184">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b380-184">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 75085bed9c1f9b0cd0c0328b9a166c6dc08a60b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992822"
---
# <span data-ttu-id="9e174-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="9e174-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="9e174-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e174-102">SYNOPSIS</span></span>
<span data-ttu-id="9e174-103">Creare un nuovo account diDbDb.</span><span class="sxs-lookup"><span data-stu-id="9e174-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="9e174-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e174-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork]
 [-ApiKind <String>] [-DisableKeyBasedMetadataWriteAccess] [-EnableFreeTier <Boolean>] [-Location <String[]>]
 [-LocationObject <PSLocation[]>] -ResourceGroupName <String> -Name <String>
 [-DefaultConsistencyLevel <String>] [-IpRule <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-PublicNetworkAccess <String>]
 [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob] [-NetworkAclBypass <String>]
 [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>] [-BackupIntervalInMinutes <Int32>]
 [-BackupRetentionIntervalInHours <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9e174-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9e174-105">DESCRIPTION</span></span>
<span data-ttu-id="9e174-106">Creare un nuovo account diDbDb per il gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="9e174-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="9e174-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e174-107">EXAMPLES</span></span>

### <span data-ttu-id="9e174-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9e174-108">Example 1</span></span>
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
NetworkAclBypass              : None
NetworkAclBypassResourceIds   : {}
```

<span data-ttu-id="9e174-109">In ResourceGroup resourceGroupName viene creato un nuovo accountDbDb con nome databaseAccountName.</span><span class="sxs-lookup"><span data-stu-id="9e174-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="9e174-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e174-110">PARAMETERS</span></span>

### <span data-ttu-id="9e174-111">-Api Riepi</span><span class="sxs-lookup"><span data-stu-id="9e174-111">-ApiKind</span></span>
<span data-ttu-id="9e174-112">Tipo di account di database DB di Ofovas da creare.</span><span class="sxs-lookup"><span data-stu-id="9e174-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="9e174-113">Valori accettati: Sql, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="9e174-113">Accepted values: Sql, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="9e174-114">Valore predefinito: Sql</span><span class="sxs-lookup"><span data-stu-id="9e174-114">Default value: Sql</span></span>

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

### <span data-ttu-id="9e174-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e174-115">-AsJob</span></span>
<span data-ttu-id="9e174-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9e174-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e174-117">-BackupIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="9e174-117">-BackupIntervalInMinutes</span></span>
<span data-ttu-id="9e174-118">Intervallo (in minuti) con cui viene eseguito il backup (solo per gli account con backup in modalità periodica)</span><span class="sxs-lookup"><span data-stu-id="9e174-118">The interval(in minutes) with which backup are taken (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="9e174-119">-BackupRetentionIntervalInHours</span><span class="sxs-lookup"><span data-stu-id="9e174-119">-BackupRetentionIntervalInHours</span></span>
<span data-ttu-id="9e174-120">Il tempo (in ore) per cui viene conservato ogni backup (solo per gli account con backup in modalità periodica)</span><span class="sxs-lookup"><span data-stu-id="9e174-120">The time(in hours) for which each backup is retained (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="9e174-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e174-121">-Confirm</span></span>
<span data-ttu-id="9e174-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e174-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e174-123">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="9e174-123">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="9e174-124">Livello di coerenza predefinito dell'account di database DB di Corso.</span><span class="sxs-lookup"><span data-stu-id="9e174-124">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="9e174-125">Valori accettati: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="9e174-125">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="9e174-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e174-126">-DefaultProfile</span></span>
<span data-ttu-id="9e174-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e174-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e174-128">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="9e174-128">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="9e174-129">Disabilitare le operazioni di scrittura su risorse di metadati (database, contenitori e velocità effettiva) tramite chiavi account</span><span class="sxs-lookup"><span data-stu-id="9e174-129">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="9e174-130">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="9e174-130">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="9e174-131">Bool per indicare se AnalyticalStorage è abilitato per l'account.</span><span class="sxs-lookup"><span data-stu-id="9e174-131">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="9e174-132">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="9e174-132">-EnableAutomaticFailover</span></span>
<span data-ttu-id="9e174-133">Abilita il failover automatico dell'area di scrittura nei rari casi in cui l'area non sia disponibile a causa di un'interruzione.</span><span class="sxs-lookup"><span data-stu-id="9e174-133">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="9e174-134">Il failover automatico causa una nuova area di scrittura per l'account e viene scelto in base alle priorità di failover configurate per l'account.</span><span class="sxs-lookup"><span data-stu-id="9e174-134">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="9e174-135">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="9e174-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="9e174-136">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="9e174-136">-EnableFreeTier</span></span>
<span data-ttu-id="9e174-137">Bool per indicare se FreeTier è abilitato per l'account.</span><span class="sxs-lookup"><span data-stu-id="9e174-137">Bool to indicate if FreeTier is enabled on the account.</span></span>

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

### <span data-ttu-id="9e174-138">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="9e174-138">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="9e174-139">Abilitare più posizioni di scrittura.</span><span class="sxs-lookup"><span data-stu-id="9e174-139">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="9e174-140">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="9e174-140">Accepted values: false, true</span></span>

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

### <span data-ttu-id="9e174-141">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9e174-141">-EnableVirtualNetwork</span></span>
<span data-ttu-id="9e174-142">Abilita la rete virtuale nell'account di database DB di Coelige.</span><span class="sxs-lookup"><span data-stu-id="9e174-142">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="9e174-143">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="9e174-143">Accepted values: false, true</span></span>

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

### <span data-ttu-id="9e174-144">-IpRule</span><span class="sxs-lookup"><span data-stu-id="9e174-144">-IpRule</span></span>
<span data-ttu-id="9e174-145">Supporto del firewall.</span><span class="sxs-lookup"><span data-stu-id="9e174-145">Firewall support.</span></span> <span data-ttu-id="9e174-146">Specifica il set di indirizzi IP o intervalli di indirizzi IP in formato CIDR da includere nell'elenco di INDIRIZZI IP client consentiti per un determinato account di database.</span><span class="sxs-lookup"><span data-stu-id="9e174-146">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="9e174-147">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="9e174-147">-KeyVaultKeyUri</span></span>
<span data-ttu-id="9e174-148">URI della proprietà KeyVault</span><span class="sxs-lookup"><span data-stu-id="9e174-148">URI of the KeyVault</span></span>

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

### <span data-ttu-id="9e174-149">-Location</span><span class="sxs-lookup"><span data-stu-id="9e174-149">-Location</span></span>
<span data-ttu-id="9e174-150">Aggiungere una posizione all'account di database DB di Coeli.</span><span class="sxs-lookup"><span data-stu-id="9e174-150">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="9e174-151">Matrice di stringhe ordinata in base alla priorità di failover.</span><span class="sxs-lookup"><span data-stu-id="9e174-151">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="9e174-152">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="9e174-152">-LocationObject</span></span>
<span data-ttu-id="9e174-153">Aggiungere una posizione all'account di database DB di Coeli.</span><span class="sxs-lookup"><span data-stu-id="9e174-153">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="9e174-154">Matrice di oggetti PSLocation.</span><span class="sxs-lookup"><span data-stu-id="9e174-154">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="9e174-155">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="9e174-155">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="9e174-156">Quando viene usato con la coerenza della coerenza dei dati associati, questo valore rappresenta la quantità di tempo non utile (nell'intervallo di tempo).</span><span class="sxs-lookup"><span data-stu-id="9e174-156">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="9e174-157">L'intervallo accettato per questo valore è 5-86400.</span><span class="sxs-lookup"><span data-stu-id="9e174-157">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="9e174-158">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="9e174-158">-MaxStalenessPrefix</span></span>
<span data-ttu-id="9e174-159">Quando viene usato con la coerenza dei dati obsoleti associati, questo valore rappresenta il numero di richieste non più richieste.</span><span class="sxs-lookup"><span data-stu-id="9e174-159">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="9e174-160">L'intervallo accettato per questo valore è 1 - 2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="9e174-160">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="9e174-161">-Name</span><span class="sxs-lookup"><span data-stu-id="9e174-161">-Name</span></span>
<span data-ttu-id="9e174-162">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="9e174-162">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9e174-163">-NetworkAclBypass</span><span class="sxs-lookup"><span data-stu-id="9e174-163">-NetworkAclBypass</span></span>
<span data-ttu-id="9e174-164">Se è abilitato o meno il bypass di accesso di rete per questo account per Synapse Link.</span><span class="sxs-lookup"><span data-stu-id="9e174-164">Whether or not Network Acl Bypass is enabled for this account for Synapse Link.</span></span> <span data-ttu-id="9e174-165">I valori possibili includono: 'Nessuno', 'AzureServices'.</span><span class="sxs-lookup"><span data-stu-id="9e174-165">Possible values include: 'None', 'AzureServices'.</span></span>

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

### <span data-ttu-id="9e174-166">-NetworkAclBypassResourceId</span><span class="sxs-lookup"><span data-stu-id="9e174-166">-NetworkAclBypassResourceId</span></span>
<span data-ttu-id="9e174-167">Elenco degli ID di risorsa per consentire il bypass di Acl di rete per Synapse Link.</span><span class="sxs-lookup"><span data-stu-id="9e174-167">List of Resource Ids to allow Network Acl Bypass for Synapse Link.</span></span>

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

### <span data-ttu-id="9e174-168">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="9e174-168">-PublicNetworkAccess</span></span>
<span data-ttu-id="9e174-169">Se l'accesso all'endpoint pubblico è consentito o meno per questo server.</span><span class="sxs-lookup"><span data-stu-id="9e174-169">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="9e174-170">I valori possibili includono: 'Abilitato', 'Disabilitato'</span><span class="sxs-lookup"><span data-stu-id="9e174-170">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="9e174-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e174-171">-ResourceGroupName</span></span>
<span data-ttu-id="9e174-172">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9e174-172">Name of resource group.</span></span>

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

### <span data-ttu-id="9e174-173">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="9e174-173">-ServerVersion</span></span>
<span data-ttu-id="9e174-174">ServerVersion, valido solo nel caso di account MongoDB.</span><span class="sxs-lookup"><span data-stu-id="9e174-174">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="9e174-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="9e174-175">-Tag</span></span>
<span data-ttu-id="9e174-176">Tabella hash di tag come coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="9e174-176">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="9e174-177">Usare una stringa vuota per cancellare il tag esistente.</span><span class="sxs-lookup"><span data-stu-id="9e174-177">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="9e174-178">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9e174-178">-VirtualNetworkRule</span></span>
<span data-ttu-id="9e174-179">Matrice dei valori stringa degli ACL per la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9e174-179">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="9e174-180">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="9e174-180">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="9e174-181">Matrice di PSVirtualNetworkRuleObjects per la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9e174-181">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="9e174-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e174-182">-WhatIf</span></span>
<span data-ttu-id="9e174-183">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e174-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e174-184">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e174-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e174-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e174-185">CommonParameters</span></span>
<span data-ttu-id="9e174-186">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e174-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e174-187">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9e174-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e174-188">INPUT</span><span class="sxs-lookup"><span data-stu-id="9e174-188">INPUTS</span></span>

### <span data-ttu-id="9e174-189">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="9e174-189">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="9e174-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e174-190">OUTPUTS</span></span>

### <span data-ttu-id="9e174-191">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="9e174-191">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="9e174-192">NOTE</span><span class="sxs-lookup"><span data-stu-id="9e174-192">NOTES</span></span>

## <span data-ttu-id="9e174-193">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e174-193">RELATED LINKS</span></span>

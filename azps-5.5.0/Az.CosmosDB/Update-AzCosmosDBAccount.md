---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: e88deadc0a46aa5d89bd513a4aba1b93e22fbb5a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177231"
---
# <span data-ttu-id="41118-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="41118-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="41118-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41118-102">SYNOPSIS</span></span>
<span data-ttu-id="41118-103">Aggiornare gli attributi di un accountDbDb.</span><span class="sxs-lookup"><span data-stu-id="41118-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="41118-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41118-104">SYNTAX</span></span>

### <span data-ttu-id="41118-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="41118-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-DisableKeyBasedMetadataWriteAccess <Boolean>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41118-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41118-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41118-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41118-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41118-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="41118-108">DESCRIPTION</span></span>
<span data-ttu-id="41118-109">Aggiornare le proprietà di un account Dibdb.</span><span class="sxs-lookup"><span data-stu-id="41118-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="41118-110">Non è possibile aggiornare le aree account in modo simulato con altre proprietà.</span><span class="sxs-lookup"><span data-stu-id="41118-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="41118-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41118-111">EXAMPLES</span></span>

### <span data-ttu-id="41118-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="41118-112">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name accountName -DefaultConsistencyLevel "Strong" -EnableAutomaticFailover 1 -EnableMultipleWriteLocations 1 -EnableVirtualNetwork 1

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : True
EnableAutomaticFailover       : True
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Fluent.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {accountName-eastus}
ReadLocations                 : {accountName-eastus}
FailoverPolicies              : {accountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : True
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/accountName
Name                          : accountName
Type                          : Microsoft.DocumentDB/databaseAccounts
```

<span data-ttu-id="41118-113">Aggiornato DefaultConsistencyLevel a "Strong", abilitato AutomaticFailover, Enabled MultipleWriteLocations e Enabled VirtualNetwork per l'account CpsDB con nome accountName.</span><span class="sxs-lookup"><span data-stu-id="41118-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="41118-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41118-114">PARAMETERS</span></span>

### <span data-ttu-id="41118-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41118-115">-AsJob</span></span>
<span data-ttu-id="41118-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="41118-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41118-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41118-117">-Confirm</span></span>
<span data-ttu-id="41118-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41118-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41118-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="41118-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="41118-120">Livello di coerenza predefinito dell'account di database DB di Coeli.</span><span class="sxs-lookup"><span data-stu-id="41118-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="41118-121">Valori accettati: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="41118-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="41118-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41118-122">-DefaultProfile</span></span>
<span data-ttu-id="41118-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41118-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41118-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="41118-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="41118-125">Disabilitare le operazioni di scrittura su risorse di metadati (database, contenitori e velocità effettiva) tramite chiavi account</span><span class="sxs-lookup"><span data-stu-id="41118-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="41118-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="41118-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="41118-127">Bool per indicare se AnalyticalStorage è abilitato per l'account.</span><span class="sxs-lookup"><span data-stu-id="41118-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="41118-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="41118-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="41118-129">Abilita il failover automatico dell'area di scrittura nei rari casi in cui l'area non sia disponibile a causa di un'interruzione.</span><span class="sxs-lookup"><span data-stu-id="41118-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="41118-130">Il failover automatico causa una nuova area di scrittura per l'account e viene scelto in base alle priorità di failover configurate per l'account.</span><span class="sxs-lookup"><span data-stu-id="41118-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="41118-131">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="41118-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="41118-132">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="41118-132">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="41118-133">Abilitare più posizioni di scrittura.</span><span class="sxs-lookup"><span data-stu-id="41118-133">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="41118-134">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="41118-134">Accepted values: false, true</span></span>

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

### <span data-ttu-id="41118-135">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="41118-135">-EnableVirtualNetwork</span></span>
<span data-ttu-id="41118-136">Abilita la rete virtuale nell'account di database DB di Coelige.</span><span class="sxs-lookup"><span data-stu-id="41118-136">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="41118-137">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="41118-137">Accepted values: false, true</span></span>

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

### <span data-ttu-id="41118-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41118-138">-InputObject</span></span>
<span data-ttu-id="41118-139">Oggetto AccountDb Disa</span><span class="sxs-lookup"><span data-stu-id="41118-139">CosmosDB Account object</span></span>

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

### <span data-ttu-id="41118-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="41118-140">-IpRule</span></span>
<span data-ttu-id="41118-141">Supporto del firewall.</span><span class="sxs-lookup"><span data-stu-id="41118-141">Firewall support.</span></span> <span data-ttu-id="41118-142">Specifica il set di indirizzi IP o intervalli di indirizzi IP in formato CIDR da includere nell'elenco di INDIRIZZI IP client consentiti per un determinato account di database.</span><span class="sxs-lookup"><span data-stu-id="41118-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="41118-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="41118-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="41118-144">URI della proprietà KeyVault</span><span class="sxs-lookup"><span data-stu-id="41118-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="41118-145">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="41118-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="41118-146">Quando viene usato con la coerenza della coerenza dei dati associati, questo valore rappresenta la quantità di tempo non utile (nell'intervallo di tempo).</span><span class="sxs-lookup"><span data-stu-id="41118-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="41118-147">L'intervallo accettato per questo valore è 5-86400.</span><span class="sxs-lookup"><span data-stu-id="41118-147">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="41118-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="41118-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="41118-149">Quando viene usato con la coerenza della coerenza dei dati associati, questo valore rappresenta il numero di richieste non più corrette.</span><span class="sxs-lookup"><span data-stu-id="41118-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="41118-150">L'intervallo accettato per questo valore è 1 - 2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="41118-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="41118-151">-Name</span><span class="sxs-lookup"><span data-stu-id="41118-151">-Name</span></span>
<span data-ttu-id="41118-152">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="41118-152">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="41118-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="41118-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="41118-154">Se l'accesso all'endpoint pubblico è consentito o meno per questo server.</span><span class="sxs-lookup"><span data-stu-id="41118-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="41118-155">I valori possibili includono: 'Abilitato', 'Disabilitato'</span><span class="sxs-lookup"><span data-stu-id="41118-155">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="41118-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41118-156">-ResourceGroupName</span></span>
<span data-ttu-id="41118-157">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="41118-157">Name of resource group.</span></span>

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

### <span data-ttu-id="41118-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41118-158">-ResourceId</span></span>
<span data-ttu-id="41118-159">ResourceId della risorsa.</span><span class="sxs-lookup"><span data-stu-id="41118-159">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="41118-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="41118-160">-Tag</span></span>
<span data-ttu-id="41118-161">Tabella hash di tag come coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="41118-161">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="41118-162">Usare una stringa vuota per cancellare il tag esistente.</span><span class="sxs-lookup"><span data-stu-id="41118-162">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="41118-163">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="41118-163">-VirtualNetworkRule</span></span>
<span data-ttu-id="41118-164">Matrice dei valori stringa degli ACL per la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="41118-164">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="41118-165">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="41118-165">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="41118-166">Matrice di PSVirtualNetworkRuleObjects per la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="41118-166">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="41118-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41118-167">-WhatIf</span></span>
<span data-ttu-id="41118-168">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41118-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41118-169">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41118-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41118-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41118-170">CommonParameters</span></span>
<span data-ttu-id="41118-171">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41118-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41118-172">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="41118-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41118-173">INPUT</span><span class="sxs-lookup"><span data-stu-id="41118-173">INPUTS</span></span>

### <span data-ttu-id="41118-174">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="41118-174">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="41118-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41118-175">OUTPUTS</span></span>

### <span data-ttu-id="41118-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="41118-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="41118-177">NOTE</span><span class="sxs-lookup"><span data-stu-id="41118-177">NOTES</span></span>

## <span data-ttu-id="41118-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41118-178">RELATED LINKS</span></span>

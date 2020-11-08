---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: e88deadc0a46aa5d89bd513a4aba1b93e22fbb5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190333"
---
# <span data-ttu-id="a0d40-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="a0d40-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="a0d40-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0d40-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d40-103">Aggiornare gli attributi di un account di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="a0d40-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="a0d40-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0d40-104">SYNTAX</span></span>

### <span data-ttu-id="a0d40-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a0d40-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-DisableKeyBasedMetadataWriteAccess <Boolean>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0d40-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0d40-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0d40-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0d40-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0d40-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0d40-108">DESCRIPTION</span></span>
<span data-ttu-id="a0d40-109">Aggiornare le proprietà di un account di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="a0d40-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="a0d40-110">Non è possibile aggiornare le aree dell'account simulataneously con altre proprietà.</span><span class="sxs-lookup"><span data-stu-id="a0d40-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="a0d40-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0d40-111">EXAMPLES</span></span>

### <span data-ttu-id="a0d40-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a0d40-112">Example 1</span></span>
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

<span data-ttu-id="a0d40-113">Aggiornamento di DefaultConsistencyLevel a "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations e Enabled VirtualNetwork per CosmosDB account con Name AccountName.</span><span class="sxs-lookup"><span data-stu-id="a0d40-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="a0d40-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0d40-114">PARAMETERS</span></span>

### <span data-ttu-id="a0d40-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0d40-115">-AsJob</span></span>
<span data-ttu-id="a0d40-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a0d40-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0d40-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a0d40-117">-Confirm</span></span>
<span data-ttu-id="a0d40-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0d40-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0d40-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="a0d40-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="a0d40-120">Livello di coerenza predefinito dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="a0d40-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="a0d40-121">Valori accettati: BoundedStaleness, ConsistentPrefix, eventuale, sessione, Strong</span><span class="sxs-lookup"><span data-stu-id="a0d40-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="a0d40-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0d40-122">-DefaultProfile</span></span>
<span data-ttu-id="a0d40-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0d40-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0d40-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="a0d40-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="a0d40-125">Disabilitare le operazioni di scrittura sulle risorse dei metadati (database, contenitori, throughput) tramite i tasti account</span><span class="sxs-lookup"><span data-stu-id="a0d40-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="a0d40-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="a0d40-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="a0d40-127">Bool per indicare se AnalyticalStorage è abilitato per l'account.</span><span class="sxs-lookup"><span data-stu-id="a0d40-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="a0d40-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="a0d40-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="a0d40-129">Consente il failover automatico dell'area di scrittura nell'evento raro che l'area non è disponibile a causa di un'interruzione.</span><span class="sxs-lookup"><span data-stu-id="a0d40-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="a0d40-130">Il failover automatico comporterà una nuova area di scrittura per l'account e verrà scelto in base alle priorità di failover configurate per l'account.</span><span class="sxs-lookup"><span data-stu-id="a0d40-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="a0d40-131">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="a0d40-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="a0d40-132">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="a0d40-132">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="a0d40-133">Abilitare più posizioni di scrittura.</span><span class="sxs-lookup"><span data-stu-id="a0d40-133">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="a0d40-134">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="a0d40-134">Accepted values: false, true</span></span>

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

### <span data-ttu-id="a0d40-135">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a0d40-135">-EnableVirtualNetwork</span></span>
<span data-ttu-id="a0d40-136">Abilita la rete virtuale nell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="a0d40-136">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="a0d40-137">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="a0d40-137">Accepted values: false, true</span></span>

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

### <span data-ttu-id="a0d40-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0d40-138">-InputObject</span></span>
<span data-ttu-id="a0d40-139">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="a0d40-139">CosmosDB Account object</span></span>

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

### <span data-ttu-id="a0d40-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="a0d40-140">-IpRule</span></span>
<span data-ttu-id="a0d40-141">Supporto firewall.</span><span class="sxs-lookup"><span data-stu-id="a0d40-141">Firewall support.</span></span> <span data-ttu-id="a0d40-142">Specifica il set di indirizzi IP o intervalli di indirizzi IP in formato CIDR da includere come elenco consentito di IPs client per un dato account di database.</span><span class="sxs-lookup"><span data-stu-id="a0d40-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="a0d40-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="a0d40-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="a0d40-144">URI del Vault</span><span class="sxs-lookup"><span data-stu-id="a0d40-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="a0d40-145">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a0d40-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="a0d40-146">Se usato con coerenza di obsolescenza limitata, questo valore rappresenta la quantità di tempo di obsolescenza (in TimeSpan) tollerata.</span><span class="sxs-lookup"><span data-stu-id="a0d40-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="a0d40-147">L'intervallo accettato per questo valore è 5-86400.</span><span class="sxs-lookup"><span data-stu-id="a0d40-147">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="a0d40-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="a0d40-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="a0d40-149">Se usato con coerenza di obsolescenza limitata, questo valore rappresenta il numero di richieste non aggiornate tollerate.</span><span class="sxs-lookup"><span data-stu-id="a0d40-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="a0d40-150">L'intervallo accettato per questo valore è 1-2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="a0d40-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="a0d40-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0d40-151">-Name</span></span>
<span data-ttu-id="a0d40-152">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="a0d40-152">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a0d40-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="a0d40-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="a0d40-154">Indipendentemente dal fatto che sia consentito o meno l'accesso endpoint pubblico per il server.</span><span class="sxs-lookup"><span data-stu-id="a0d40-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="a0d40-155">I valori possibili includono:' Enabled ',' disabled '</span><span class="sxs-lookup"><span data-stu-id="a0d40-155">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="a0d40-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0d40-156">-ResourceGroupName</span></span>
<span data-ttu-id="a0d40-157">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a0d40-157">Name of resource group.</span></span>

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

### <span data-ttu-id="a0d40-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0d40-158">-ResourceId</span></span>
<span data-ttu-id="a0d40-159">ResourceId della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a0d40-159">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="a0d40-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0d40-160">-Tag</span></span>
<span data-ttu-id="a0d40-161">Hashtable di tag come coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="a0d40-161">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="a0d40-162">Usa una stringa vuota per cancellare il tag esistente.</span><span class="sxs-lookup"><span data-stu-id="a0d40-162">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="a0d40-163">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a0d40-163">-VirtualNetworkRule</span></span>
<span data-ttu-id="a0d40-164">Matrice di valori stringa di ACL per la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a0d40-164">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="a0d40-165">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="a0d40-165">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="a0d40-166">Matrice di PSVirtualNetworkRuleObjects for Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="a0d40-166">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="a0d40-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0d40-167">-WhatIf</span></span>
<span data-ttu-id="a0d40-168">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0d40-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0d40-169">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0d40-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0d40-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d40-170">CommonParameters</span></span>
<span data-ttu-id="a0d40-171">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0d40-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d40-172">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0d40-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d40-173">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0d40-173">INPUTS</span></span>

### <span data-ttu-id="a0d40-174">Microsoft. Azure. Commands. CosmosDB. Models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="a0d40-174">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="a0d40-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0d40-175">OUTPUTS</span></span>

### <span data-ttu-id="a0d40-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="a0d40-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="a0d40-177">Note</span><span class="sxs-lookup"><span data-stu-id="a0d40-177">NOTES</span></span>

## <span data-ttu-id="a0d40-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0d40-178">RELATED LINKS</span></span>

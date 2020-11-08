---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: a31df71a1242f4f4e9eb01a37d31eb54ec874a99
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018510"
---
# <span data-ttu-id="0b9d8-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="0b9d8-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="0b9d8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0b9d8-102">SYNOPSIS</span></span>
<span data-ttu-id="0b9d8-103">Aggiornare gli attributi di un account di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="0b9d8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b9d8-104">SYNTAX</span></span>

### <span data-ttu-id="0b9d8-105">ByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0b9d8-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b9d8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b9d8-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b9d8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b9d8-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccount> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b9d8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b9d8-108">DESCRIPTION</span></span>
<span data-ttu-id="0b9d8-109">Aggiornare le proprietà di un account di CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="0b9d8-110">Non è possibile aggiornare le aree dell'account simulataneously con altre proprietà.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="0b9d8-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b9d8-111">EXAMPLES</span></span>

### <span data-ttu-id="0b9d8-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0b9d8-112">Example 1</span></span>
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

<span data-ttu-id="0b9d8-113">Aggiornamento di DefaultConsistencyLevel a "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations e Enabled VirtualNetwork per CosmosDB account con Name AccountName.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="0b9d8-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0b9d8-114">PARAMETERS</span></span>

### <span data-ttu-id="0b9d8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b9d8-115">-AsJob</span></span>
<span data-ttu-id="0b9d8-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0b9d8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b9d8-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0b9d8-117">-Confirm</span></span>
<span data-ttu-id="0b9d8-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b9d8-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="0b9d8-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="0b9d8-120">Livello di coerenza predefinito dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="0b9d8-121">Valori accettati: BoundedStaleness, ConsistentPrefix, eventuale, sessione, Strong</span><span class="sxs-lookup"><span data-stu-id="0b9d8-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="0b9d8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b9d8-122">-DefaultProfile</span></span>
<span data-ttu-id="0b9d8-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b9d8-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="0b9d8-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="0b9d8-125">Disabilitare le operazioni di scrittura sulle risorse dei metadati (database, contenitori, throughput) tramite i tasti account</span><span class="sxs-lookup"><span data-stu-id="0b9d8-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="0b9d8-126">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="0b9d8-126">-EnableAutomaticFailover</span></span>
<span data-ttu-id="0b9d8-127">Consente il failover automatico dell'area di scrittura nell'evento raro che l'area non è disponibile a causa di un'interruzione.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-127">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="0b9d8-128">Il failover automatico comporterà una nuova area di scrittura per l'account e verrà scelto in base alle priorità di failover configurate per l'account.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-128">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="0b9d8-129">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="0b9d8-129">Accepted values: false, true</span></span>

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

### <span data-ttu-id="0b9d8-130">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="0b9d8-130">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="0b9d8-131">Abilitare più posizioni di scrittura.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-131">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="0b9d8-132">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="0b9d8-132">Accepted values: false, true</span></span>

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

### <span data-ttu-id="0b9d8-133">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0b9d8-133">-EnableVirtualNetwork</span></span>
<span data-ttu-id="0b9d8-134">Abilita la rete virtuale nell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-134">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="0b9d8-135">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="0b9d8-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="0b9d8-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b9d8-136">-InputObject</span></span>
<span data-ttu-id="0b9d8-137">Oggetto account CosmosDB</span><span class="sxs-lookup"><span data-stu-id="0b9d8-137">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b9d8-138">-IpRangeFilter</span><span class="sxs-lookup"><span data-stu-id="0b9d8-138">-IpRangeFilter</span></span>
<span data-ttu-id="0b9d8-139">Supporto firewall.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-139">Firewall support.</span></span>
<span data-ttu-id="0b9d8-140">Specifica il set di indirizzi IP o intervalli di indirizzi IP in formato CIDR da includere come elenco consentito di IPs client per un dato account di database</span><span class="sxs-lookup"><span data-stu-id="0b9d8-140">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account</span></span>

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

### <span data-ttu-id="0b9d8-141">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="0b9d8-141">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="0b9d8-142">Se usato con coerenza di obsolescenza limitata, questo valore rappresenta la quantità di tempo di obsolescenza (in TimeSpan) tollerata.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-142">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="0b9d8-143">L'intervallo accettato per questo valore è 5-86400.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-143">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="0b9d8-144">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="0b9d8-144">-MaxStalenessPrefix</span></span>
<span data-ttu-id="0b9d8-145">Se usato con coerenza di obsolescenza limitata, questo valore rappresenta il numero di richieste non aggiornate tollerate.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-145">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="0b9d8-146">L'intervallo accettato per questo valore è 1-2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-146">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="0b9d8-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b9d8-147">-Name</span></span>
<span data-ttu-id="0b9d8-148">Nome dell'account di database Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-148">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0b9d8-149">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="0b9d8-149">-PublicNetworkAccess</span></span>
<span data-ttu-id="0b9d8-150">Indipendentemente dal fatto che sia consentito o meno l'accesso endpoint pubblico per il server.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-150">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="0b9d8-151">I valori possibili includono:' Enabled ',' disabled '</span><span class="sxs-lookup"><span data-stu-id="0b9d8-151">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="0b9d8-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b9d8-152">-ResourceGroupName</span></span>
<span data-ttu-id="0b9d8-153">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-153">Name of resource group.</span></span>

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

### <span data-ttu-id="0b9d8-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b9d8-154">-ResourceId</span></span>
<span data-ttu-id="0b9d8-155">ResourceId della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-155">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="0b9d8-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="0b9d8-156">-Tag</span></span>
<span data-ttu-id="0b9d8-157">Hashtable di tag come coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-157">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="0b9d8-158">Usa una stringa vuota per cancellare il tag esistente.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-158">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="0b9d8-159">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0b9d8-159">-VirtualNetworkRule</span></span>
<span data-ttu-id="0b9d8-160">Matrice di valori stringa di ACL per la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-160">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="0b9d8-161">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="0b9d8-161">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="0b9d8-162">Matrice di PSVirtualNetworkRuleObjects for Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-162">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b9d8-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b9d8-163">-WhatIf</span></span>
<span data-ttu-id="0b9d8-164">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b9d8-165">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b9d8-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b9d8-166">CommonParameters</span></span>
<span data-ttu-id="0b9d8-167">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b9d8-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b9d8-168">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b9d8-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b9d8-169">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0b9d8-169">INPUTS</span></span>

### <span data-ttu-id="0b9d8-170">Microsoft. Azure. Commands. CosmosDB. Models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="0b9d8-170">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="0b9d8-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b9d8-171">OUTPUTS</span></span>

### <span data-ttu-id="0b9d8-172">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="0b9d8-172">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="0b9d8-173">Note</span><span class="sxs-lookup"><span data-stu-id="0b9d8-173">NOTES</span></span>

## <span data-ttu-id="0b9d8-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b9d8-174">RELATED LINKS</span></span>

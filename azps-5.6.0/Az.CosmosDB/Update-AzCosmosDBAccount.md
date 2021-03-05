---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: cbee0ef9ce750dbb72af5be484106ccabec79321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010734"
---
# <span data-ttu-id="5c0a5-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="5c0a5-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="5c0a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c0a5-102">SYNOPSIS</span></span>
<span data-ttu-id="5c0a5-103">Aggiornare gli attributi di un accountDbDb.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="5c0a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c0a5-104">SYNTAX</span></span>

### <span data-ttu-id="5c0a5-105">ByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5c0a5-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-DisableKeyBasedMetadataWriteAccess <Boolean>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-NetworkAclBypass <String>] [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>]
 [-BackupIntervalInMinutes <Int32>] [-BackupRetentionIntervalInHours <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c0a5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c0a5-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-NetworkAclBypass <String>] [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>]
 [-BackupIntervalInMinutes <Int32>] [-BackupRetentionIntervalInHours <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c0a5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c0a5-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-NetworkAclBypass <String>] [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>]
 [-BackupIntervalInMinutes <Int32>] [-BackupRetentionIntervalInHours <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c0a5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5c0a5-108">DESCRIPTION</span></span>
<span data-ttu-id="5c0a5-109">Aggiornare le proprietà di un account Dibdb.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="5c0a5-110">Non è possibile aggiornare le aree account in modo simulato con altre proprietà.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="5c0a5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c0a5-111">EXAMPLES</span></span>

### <span data-ttu-id="5c0a5-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5c0a5-112">Example 1</span></span>
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
NetworkAclBypass              : None
NetworkAclBypassResourceIds   : {}
```

<span data-ttu-id="5c0a5-113">Aggiornato DefaultConsistencyLevel a "Strong", abilitato AutomaticFailover, Enabled MultipleWriteLocations e Enabled VirtualNetwork per l'account CpsDB con nome accountName.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="5c0a5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c0a5-114">PARAMETERS</span></span>

### <span data-ttu-id="5c0a5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c0a5-115">-AsJob</span></span>
<span data-ttu-id="5c0a5-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5c0a5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c0a5-117">-BackupIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="5c0a5-117">-BackupIntervalInMinutes</span></span>
<span data-ttu-id="5c0a5-118">Intervallo (in minuti) con cui viene eseguito il backup (solo per gli account con backup in modalità periodica)</span><span class="sxs-lookup"><span data-stu-id="5c0a5-118">The interval(in minutes) with which backup are taken (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="5c0a5-119">-BackupRetentionIntervalInHours</span><span class="sxs-lookup"><span data-stu-id="5c0a5-119">-BackupRetentionIntervalInHours</span></span>
<span data-ttu-id="5c0a5-120">Il tempo (in ore) per cui viene conservato ogni backup (solo per gli account con backup in modalità periodica)</span><span class="sxs-lookup"><span data-stu-id="5c0a5-120">The time(in hours) for which each backup is retained (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="5c0a5-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c0a5-121">-Confirm</span></span>
<span data-ttu-id="5c0a5-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c0a5-123">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="5c0a5-123">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="5c0a5-124">Livello di coerenza predefinito dell'account di database DB di Corso.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-124">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="5c0a5-125">Valori accettati: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="5c0a5-125">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="5c0a5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c0a5-126">-DefaultProfile</span></span>
<span data-ttu-id="5c0a5-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c0a5-128">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="5c0a5-128">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="5c0a5-129">Disabilitare le operazioni di scrittura su risorse di metadati (database, contenitori e velocità effettiva) tramite chiavi account</span><span class="sxs-lookup"><span data-stu-id="5c0a5-129">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="5c0a5-130">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="5c0a5-130">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="5c0a5-131">Bool per indicare se AnalyticalStorage è abilitato per l'account.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-131">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="5c0a5-132">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="5c0a5-132">-EnableAutomaticFailover</span></span>
<span data-ttu-id="5c0a5-133">Abilita il failover automatico dell'area di scrittura nei rari casi in cui l'area non sia disponibile a causa di un'interruzione.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-133">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="5c0a5-134">Il failover automatico causa una nuova area di scrittura per l'account e viene scelto in base alle priorità di failover configurate per l'account.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-134">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="5c0a5-135">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="5c0a5-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="5c0a5-136">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="5c0a5-136">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="5c0a5-137">Abilitare più posizioni di scrittura.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-137">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="5c0a5-138">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="5c0a5-138">Accepted values: false, true</span></span>

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

### <span data-ttu-id="5c0a5-139">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5c0a5-139">-EnableVirtualNetwork</span></span>
<span data-ttu-id="5c0a5-140">Abilita la rete virtuale nell'account di database DB di Coelige.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-140">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="5c0a5-141">Valori accettati: falso, vero</span><span class="sxs-lookup"><span data-stu-id="5c0a5-141">Accepted values: false, true</span></span>

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

### <span data-ttu-id="5c0a5-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c0a5-142">-InputObject</span></span>
<span data-ttu-id="5c0a5-143">Oggetto Account Aziendale</span><span class="sxs-lookup"><span data-stu-id="5c0a5-143">CosmosDB Account object</span></span>

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

### <span data-ttu-id="5c0a5-144">-IpRule</span><span class="sxs-lookup"><span data-stu-id="5c0a5-144">-IpRule</span></span>
<span data-ttu-id="5c0a5-145">Supporto del firewall.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-145">Firewall support.</span></span> <span data-ttu-id="5c0a5-146">Specifica il set di indirizzi IP o intervalli di indirizzi IP in formato CIDR da includere nell'elenco di INDIRIZZI IP client consentiti per un determinato account di database.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-146">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="5c0a5-147">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="5c0a5-147">-KeyVaultKeyUri</span></span>
<span data-ttu-id="5c0a5-148">URI della proprietà KeyVault</span><span class="sxs-lookup"><span data-stu-id="5c0a5-148">URI of the KeyVault</span></span>

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

### <span data-ttu-id="5c0a5-149">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="5c0a5-149">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="5c0a5-150">Quando viene usato con la coerenza della coerenza dei dati associati, questo valore rappresenta la quantità di tempo non utile (nell'intervallo di tempo).</span><span class="sxs-lookup"><span data-stu-id="5c0a5-150">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="5c0a5-151">L'intervallo accettato per questo valore è 5-86400.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-151">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="5c0a5-152">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="5c0a5-152">-MaxStalenessPrefix</span></span>
<span data-ttu-id="5c0a5-153">Quando viene usato con la coerenza dei dati obsoleti associati, questo valore rappresenta il numero di richieste non più richieste.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-153">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="5c0a5-154">L'intervallo accettato per questo valore è 1 - 2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-154">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="5c0a5-155">-Name</span><span class="sxs-lookup"><span data-stu-id="5c0a5-155">-Name</span></span>
<span data-ttu-id="5c0a5-156">Nome dell'account di database DB di Dellis.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-156">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5c0a5-157">-NetworkAclBypass</span><span class="sxs-lookup"><span data-stu-id="5c0a5-157">-NetworkAclBypass</span></span>
<span data-ttu-id="5c0a5-158">Se è abilitato o meno il bypass di accesso di rete per questo account per Synapse Link.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-158">Whether or not Network Acl Bypass is enabled for this account for Synapse Link.</span></span> <span data-ttu-id="5c0a5-159">I valori possibili includono: 'Nessuno', 'AzureServices'.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-159">Possible values include: 'None', 'AzureServices'.</span></span>

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

### <span data-ttu-id="5c0a5-160">-NetworkAclBypassResourceId</span><span class="sxs-lookup"><span data-stu-id="5c0a5-160">-NetworkAclBypassResourceId</span></span>
<span data-ttu-id="5c0a5-161">Elenco degli ID di risorsa per consentire il bypass di Acl di rete per Synapse Link.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-161">List of Resource Ids to allow Network Acl Bypass for Synapse Link.</span></span>

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

### <span data-ttu-id="5c0a5-162">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="5c0a5-162">-PublicNetworkAccess</span></span>
<span data-ttu-id="5c0a5-163">Se l'accesso all'endpoint pubblico è consentito o meno per questo server.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-163">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="5c0a5-164">I valori possibili includono: 'Abilitato', 'Disabilitato'</span><span class="sxs-lookup"><span data-stu-id="5c0a5-164">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="5c0a5-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c0a5-165">-ResourceGroupName</span></span>
<span data-ttu-id="5c0a5-166">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-166">Name of resource group.</span></span>

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

### <span data-ttu-id="5c0a5-167">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c0a5-167">-ResourceId</span></span>
<span data-ttu-id="5c0a5-168">ResourceId della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-168">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="5c0a5-169">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="5c0a5-169">-ServerVersion</span></span>
<span data-ttu-id="5c0a5-170">ServerVersion, valido solo nel caso di account MongoDB.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-170">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="5c0a5-171">-Tag</span><span class="sxs-lookup"><span data-stu-id="5c0a5-171">-Tag</span></span>
<span data-ttu-id="5c0a5-172">Tabella hash di tag come coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-172">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="5c0a5-173">Usare una stringa vuota per cancellare il tag esistente.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-173">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="5c0a5-174">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5c0a5-174">-VirtualNetworkRule</span></span>
<span data-ttu-id="5c0a5-175">Matrice dei valori stringa degli ACL per la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-175">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="5c0a5-176">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="5c0a5-176">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="5c0a5-177">Matrice di PSVirtualNetworkRuleObjects per la rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-177">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="5c0a5-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c0a5-178">-WhatIf</span></span>
<span data-ttu-id="5c0a5-179">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c0a5-180">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c0a5-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c0a5-181">CommonParameters</span></span>
<span data-ttu-id="5c0a5-182">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c0a5-183">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5c0a5-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c0a5-184">INPUT</span><span class="sxs-lookup"><span data-stu-id="5c0a5-184">INPUTS</span></span>

### <span data-ttu-id="5c0a5-185">Microsoft.Azure.Commands.EnterpriseDb.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="5c0a5-185">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="5c0a5-186">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c0a5-186">OUTPUTS</span></span>

### <span data-ttu-id="5c0a5-187">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="5c0a5-187">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="5c0a5-188">NOTE</span><span class="sxs-lookup"><span data-stu-id="5c0a5-188">NOTES</span></span>

## <span data-ttu-id="5c0a5-189">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c0a5-189">RELATED LINKS</span></span>

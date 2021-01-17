---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b8b6c11da622b7fa0ee67dc418f2055dd72c1d13
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359043"
---
# <span data-ttu-id="603c9-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="603c9-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="603c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="603c9-102">SYNOPSIS</span></span>
<span data-ttu-id="603c9-103">Creare o aggiornare un cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="603c9-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="603c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="603c9-104">SYNTAX</span></span>

```
New-AzKustoCluster -Name <String> -ResourceGroupName <String> -Location <String> -SkuName <AzureSkuName>
 -SkuTier <AzureSkuTier> [-SubscriptionId <String>] [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="603c9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="603c9-105">DESCRIPTION</span></span>
<span data-ttu-id="603c9-106">Creare o aggiornare un cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="603c9-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="603c9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="603c9-107">EXAMPLES</span></span>

### <span data-ttu-id="603c9-108">Esempio 1: creare un nuovo cluster di Kusto</span><span class="sxs-lookup"><span data-stu-id="603c9-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="603c9-109">Il comando precedente crea un nuovo cluster di Kusto denominato "testnewkustocluster" nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="603c9-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="603c9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="603c9-110">PARAMETERS</span></span>

### <span data-ttu-id="603c9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="603c9-111">-AsJob</span></span>
<span data-ttu-id="603c9-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="603c9-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="603c9-113">-DefaultProfile</span></span>
<span data-ttu-id="603c9-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="603c9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="603c9-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="603c9-116">Valore booleano che indica se i dischi del cluster sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="603c9-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="603c9-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="603c9-118">Valore booleano che indica se è abilitata la crittografia doppia.</span><span class="sxs-lookup"><span data-stu-id="603c9-118">A boolean value that indicates if double encryption is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="603c9-119">-EnablePurge</span></span>
<span data-ttu-id="603c9-120">Valore booleano che indica se le operazioni di ripulitura sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="603c9-120">A boolean value that indicates if the purge operations are enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="603c9-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="603c9-122">Valore booleano che indica se l'acquisizione del flusso è abilitata.</span><span class="sxs-lookup"><span data-stu-id="603c9-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-123">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="603c9-123">-IdentityType</span></span>
<span data-ttu-id="603c9-124">Tipo di identità.</span><span class="sxs-lookup"><span data-stu-id="603c9-124">The identity type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-125">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="603c9-125">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="603c9-126">Elenco delle identità utente associate al cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="603c9-126">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="603c9-127">I riferimenti chiave del dizionario delle identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="603c9-127">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-128">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="603c9-128">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="603c9-129">Il nome della chiave di volta chiave.</span><span class="sxs-lookup"><span data-stu-id="603c9-129">The name of the key vault key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-130">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="603c9-130">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="603c9-131">URI del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="603c9-131">The Uri of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-132">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="603c9-132">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="603c9-133">La versione della chiave di volta chiave.</span><span class="sxs-lookup"><span data-stu-id="603c9-133">The version of the key vault key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-134">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="603c9-134">-LanguageExtensionValue</span></span>
<span data-ttu-id="603c9-135">Elenco delle estensioni della lingua.</span><span class="sxs-lookup"><span data-stu-id="603c9-135">The list of language extensions.</span></span>
<span data-ttu-id="603c9-136">Per costruire, vedere la sezione Note per le proprietà di LANGUAGEEXTENSIONVALUE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="603c9-136">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-137">-Posizione</span><span class="sxs-lookup"><span data-stu-id="603c9-137">-Location</span></span>
<span data-ttu-id="603c9-138">Posizione geografica in cui vive la risorsa</span><span class="sxs-lookup"><span data-stu-id="603c9-138">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="603c9-139">-Name</span></span>
<span data-ttu-id="603c9-140">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="603c9-140">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-141">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="603c9-141">-NoWait</span></span>
<span data-ttu-id="603c9-142">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="603c9-142">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-143">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="603c9-143">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="603c9-144">Valore booleano che indica se la caratteristica di scalabilità ottimizzata è abilitata o meno.</span><span class="sxs-lookup"><span data-stu-id="603c9-144">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-145">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="603c9-145">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="603c9-146">Numero massimo di istanze consentite.</span><span class="sxs-lookup"><span data-stu-id="603c9-146">Maximum allowed instances count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-147">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="603c9-147">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="603c9-148">Conteggio istanze minime consentite.</span><span class="sxs-lookup"><span data-stu-id="603c9-148">Minimum allowed instances count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-149">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="603c9-149">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="603c9-150">Versione del modello definita, ad esempio 1.</span><span class="sxs-lookup"><span data-stu-id="603c9-150">The version of the template defined, for instance 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="603c9-151">-ResourceGroupName</span></span>
<span data-ttu-id="603c9-152">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="603c9-152">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-153">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="603c9-153">-SkuCapacity</span></span>
<span data-ttu-id="603c9-154">Numero di istanze del cluster.</span><span class="sxs-lookup"><span data-stu-id="603c9-154">The number of instances of the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-155">-SkuName</span><span class="sxs-lookup"><span data-stu-id="603c9-155">-SkuName</span></span>
<span data-ttu-id="603c9-156">Nome Usk.</span><span class="sxs-lookup"><span data-stu-id="603c9-156">SKU name.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-157">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="603c9-157">-SkuTier</span></span>
<span data-ttu-id="603c9-158">Livello SKU.</span><span class="sxs-lookup"><span data-stu-id="603c9-158">SKU tier.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="603c9-159">-SubscriptionId</span></span>
<span data-ttu-id="603c9-160">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="603c9-160">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="603c9-161">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="603c9-161">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="603c9-162">-Tag</span></span>
<span data-ttu-id="603c9-163">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="603c9-163">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-164">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="603c9-164">-TrustedExternalTenant</span></span>
<span data-ttu-id="603c9-165">Tenant esterni del cluster.</span><span class="sxs-lookup"><span data-stu-id="603c9-165">The cluster's external tenants.</span></span>
<span data-ttu-id="603c9-166">Per costruire, vedere la sezione Note per le proprietà di TRUSTEDEXTERNALTENANT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="603c9-166">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ITrustedExternalTenant[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="603c9-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="603c9-168">ID risorsa indirizzo IP pubblico del servizio di gestione dati.</span><span class="sxs-lookup"><span data-stu-id="603c9-168">Data management's service public IP address resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-169">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="603c9-169">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="603c9-170">ID risorsa indirizzo IP pubblico del servizio motore.</span><span class="sxs-lookup"><span data-stu-id="603c9-170">Engine service's public IP address resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-171">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="603c9-171">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="603c9-172">ID risorsa subnet.</span><span class="sxs-lookup"><span data-stu-id="603c9-172">The subnet resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-173">-Zona</span><span class="sxs-lookup"><span data-stu-id="603c9-173">-Zone</span></span>
<span data-ttu-id="603c9-174">Aree di disponibilità del cluster.</span><span class="sxs-lookup"><span data-stu-id="603c9-174">The availability zones of the cluster.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-175">-Confermare</span><span class="sxs-lookup"><span data-stu-id="603c9-175">-Confirm</span></span>
<span data-ttu-id="603c9-176">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="603c9-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="603c9-177">-WhatIf</span></span>
<span data-ttu-id="603c9-178">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="603c9-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="603c9-179">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="603c9-179">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="603c9-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="603c9-180">CommonParameters</span></span>
<span data-ttu-id="603c9-181">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="603c9-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="603c9-182">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="603c9-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="603c9-183">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="603c9-183">INPUTS</span></span>

## <span data-ttu-id="603c9-184">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="603c9-184">OUTPUTS</span></span>

### <span data-ttu-id="603c9-185">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. ICluster</span><span class="sxs-lookup"><span data-stu-id="603c9-185">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="603c9-186">Note</span><span class="sxs-lookup"><span data-stu-id="603c9-186">NOTES</span></span>

<span data-ttu-id="603c9-187">ALIAS</span><span class="sxs-lookup"><span data-stu-id="603c9-187">ALIASES</span></span>

<span data-ttu-id="603c9-188">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="603c9-188">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="603c9-189">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="603c9-189">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="603c9-190">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="603c9-190">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="603c9-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: l'elenco delle estensioni della lingua.</span><span class="sxs-lookup"><span data-stu-id="603c9-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="603c9-192">`[Name <LanguageExtensionName?>]`: Nome dell'estensione della lingua.</span><span class="sxs-lookup"><span data-stu-id="603c9-192">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="603c9-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: i tenant esterni del cluster.</span><span class="sxs-lookup"><span data-stu-id="603c9-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="603c9-194">`[Value <String>]`: GUID che rappresenta un tenant esterno.</span><span class="sxs-lookup"><span data-stu-id="603c9-194">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="603c9-195">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="603c9-195">RELATED LINKS</span></span>


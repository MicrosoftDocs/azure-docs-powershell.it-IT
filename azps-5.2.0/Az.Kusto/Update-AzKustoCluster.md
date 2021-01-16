---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: a3e1561feb470708420015bac1e2f0688f182896
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366897"
---
# <span data-ttu-id="2699e-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="2699e-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="2699e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2699e-102">SYNOPSIS</span></span>
<span data-ttu-id="2699e-103">Aggiornare un cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="2699e-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="2699e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2699e-104">SYNTAX</span></span>

### <span data-ttu-id="2699e-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2699e-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EnableDiskEncryption] [-EnableDoubleEncryption] [-EnablePurge] [-EnableStreamingIngest]
 [-IdentityType <IdentityType>] [-IdentityUserAssignedIdentity <Hashtable>]
 [-KeyVaultPropertyKeyName <String>] [-KeyVaultPropertyKeyVaultUri <String>]
 [-KeyVaultPropertyKeyVersion <String>] [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>]
 [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2699e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2699e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoCluster -InputObject <IKustoIdentity> [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2699e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2699e-107">DESCRIPTION</span></span>
<span data-ttu-id="2699e-108">Aggiornare un cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="2699e-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="2699e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2699e-109">EXAMPLES</span></span>

### <span data-ttu-id="2699e-110">Esempio 1: aggiornare un cluster esistente per nome</span><span class="sxs-lookup"><span data-stu-id="2699e-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="2699e-111">Il comando precedente aggiorna l'USK del cluster kusto "testnewkustocluster" disponibile nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="2699e-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="2699e-112">Esempio 2: aggiornare un cluster esistente per nome</span><span class="sxs-lookup"><span data-stu-id="2699e-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="2699e-113">Il comando precedente aggiorna il cluster "testnewkustocluster" trovato nel gruppo di risorse "testrg" con una chiave gestita dal cliente.</span><span class="sxs-lookup"><span data-stu-id="2699e-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="2699e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2699e-114">PARAMETERS</span></span>

### <span data-ttu-id="2699e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2699e-115">-AsJob</span></span>
<span data-ttu-id="2699e-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="2699e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2699e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2699e-117">-DefaultProfile</span></span>
<span data-ttu-id="2699e-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2699e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2699e-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="2699e-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="2699e-120">Valore booleano che indica se i dischi del cluster sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="2699e-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="2699e-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="2699e-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="2699e-122">Valore booleano che indica se è abilitata la crittografia doppia.</span><span class="sxs-lookup"><span data-stu-id="2699e-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="2699e-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="2699e-123">-EnablePurge</span></span>
<span data-ttu-id="2699e-124">Valore booleano che indica se le operazioni di ripulitura sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="2699e-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="2699e-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="2699e-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="2699e-126">Valore booleano che indica se l'acquisizione del flusso è abilitata.</span><span class="sxs-lookup"><span data-stu-id="2699e-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="2699e-127">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="2699e-127">-IdentityType</span></span>
<span data-ttu-id="2699e-128">Tipo di identità.</span><span class="sxs-lookup"><span data-stu-id="2699e-128">The identity type.</span></span>

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

### <span data-ttu-id="2699e-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2699e-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="2699e-130">Elenco delle identità utente associate al cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="2699e-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="2699e-131">I riferimenti chiave del dizionario delle identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="2699e-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="2699e-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2699e-132">-InputObject</span></span>
<span data-ttu-id="2699e-133">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2699e-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2699e-134">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="2699e-134">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="2699e-135">Il nome della chiave di volta chiave.</span><span class="sxs-lookup"><span data-stu-id="2699e-135">The name of the key vault key.</span></span>

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

### <span data-ttu-id="2699e-136">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="2699e-136">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="2699e-137">URI del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="2699e-137">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="2699e-138">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="2699e-138">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="2699e-139">La versione della chiave di volta chiave.</span><span class="sxs-lookup"><span data-stu-id="2699e-139">The version of the key vault key.</span></span>

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

### <span data-ttu-id="2699e-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="2699e-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="2699e-141">Elenco delle estensioni della lingua.</span><span class="sxs-lookup"><span data-stu-id="2699e-141">The list of language extensions.</span></span>
<span data-ttu-id="2699e-142">Per costruire, vedere la sezione Note per le proprietà di LANGUAGEEXTENSIONVALUE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2699e-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="2699e-143">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2699e-143">-Location</span></span>
<span data-ttu-id="2699e-144">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="2699e-144">Resource location.</span></span>

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

### <span data-ttu-id="2699e-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="2699e-145">-Name</span></span>
<span data-ttu-id="2699e-146">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="2699e-146">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2699e-147">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="2699e-147">-NoWait</span></span>
<span data-ttu-id="2699e-148">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="2699e-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2699e-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="2699e-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="2699e-150">Valore booleano che indica se la caratteristica di scalabilità ottimizzata è abilitata o meno.</span><span class="sxs-lookup"><span data-stu-id="2699e-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="2699e-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="2699e-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="2699e-152">Numero massimo di istanze consentite.</span><span class="sxs-lookup"><span data-stu-id="2699e-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="2699e-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="2699e-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="2699e-154">Conteggio istanze minime consentite.</span><span class="sxs-lookup"><span data-stu-id="2699e-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="2699e-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="2699e-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="2699e-156">Versione del modello definita, ad esempio 1.</span><span class="sxs-lookup"><span data-stu-id="2699e-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="2699e-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2699e-157">-ResourceGroupName</span></span>
<span data-ttu-id="2699e-158">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="2699e-158">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2699e-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="2699e-159">-SkuCapacity</span></span>
<span data-ttu-id="2699e-160">Numero di istanze del cluster.</span><span class="sxs-lookup"><span data-stu-id="2699e-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="2699e-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2699e-161">-SkuName</span></span>
<span data-ttu-id="2699e-162">Nome Usk.</span><span class="sxs-lookup"><span data-stu-id="2699e-162">SKU name.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2699e-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="2699e-163">-SkuTier</span></span>
<span data-ttu-id="2699e-164">Livello SKU.</span><span class="sxs-lookup"><span data-stu-id="2699e-164">SKU tier.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2699e-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2699e-165">-SubscriptionId</span></span>
<span data-ttu-id="2699e-166">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2699e-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2699e-167">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="2699e-167">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2699e-168">-Tag</span><span class="sxs-lookup"><span data-stu-id="2699e-168">-Tag</span></span>
<span data-ttu-id="2699e-169">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="2699e-169">Resource tags.</span></span>

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

### <span data-ttu-id="2699e-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="2699e-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="2699e-171">Tenant esterni del cluster.</span><span class="sxs-lookup"><span data-stu-id="2699e-171">The cluster's external tenants.</span></span>
<span data-ttu-id="2699e-172">Per costruire, vedere la sezione Note per le proprietà di TRUSTEDEXTERNALTENANT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2699e-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2699e-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="2699e-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="2699e-174">ID risorsa indirizzo IP pubblico del servizio di gestione dati.</span><span class="sxs-lookup"><span data-stu-id="2699e-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="2699e-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="2699e-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="2699e-176">ID risorsa indirizzo IP pubblico del servizio motore.</span><span class="sxs-lookup"><span data-stu-id="2699e-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="2699e-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="2699e-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="2699e-178">ID risorsa subnet.</span><span class="sxs-lookup"><span data-stu-id="2699e-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="2699e-179">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2699e-179">-Confirm</span></span>
<span data-ttu-id="2699e-180">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2699e-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2699e-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2699e-181">-WhatIf</span></span>
<span data-ttu-id="2699e-182">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2699e-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2699e-183">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2699e-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2699e-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2699e-184">CommonParameters</span></span>
<span data-ttu-id="2699e-185">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2699e-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2699e-186">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2699e-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2699e-187">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2699e-187">INPUTS</span></span>

### <span data-ttu-id="2699e-188">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="2699e-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="2699e-189">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2699e-189">OUTPUTS</span></span>

### <span data-ttu-id="2699e-190">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. ICluster</span><span class="sxs-lookup"><span data-stu-id="2699e-190">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="2699e-191">Note</span><span class="sxs-lookup"><span data-stu-id="2699e-191">NOTES</span></span>

<span data-ttu-id="2699e-192">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2699e-192">ALIASES</span></span>

<span data-ttu-id="2699e-193">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2699e-193">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2699e-194">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="2699e-194">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2699e-195">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2699e-195">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2699e-196">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="2699e-196">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2699e-197">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="2699e-197">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="2699e-198">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="2699e-198">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="2699e-199">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="2699e-199">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="2699e-200">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="2699e-200">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="2699e-201">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="2699e-201">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2699e-202">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2699e-202">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="2699e-203">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="2699e-203">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="2699e-204">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="2699e-204">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="2699e-205">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2699e-205">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2699e-206">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="2699e-206">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="2699e-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: l'elenco delle estensioni della lingua.</span><span class="sxs-lookup"><span data-stu-id="2699e-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="2699e-208">`[Name <LanguageExtensionName?>]`: Nome dell'estensione della lingua.</span><span class="sxs-lookup"><span data-stu-id="2699e-208">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="2699e-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: i tenant esterni del cluster.</span><span class="sxs-lookup"><span data-stu-id="2699e-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="2699e-210">`[Value <String>]`: GUID che rappresenta un tenant esterno.</span><span class="sxs-lookup"><span data-stu-id="2699e-210">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="2699e-211">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2699e-211">RELATED LINKS</span></span>


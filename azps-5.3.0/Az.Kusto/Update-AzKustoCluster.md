---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 7cc359b230bc3e4480b1cc6a03db768c17ebf60c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386284"
---
# <span data-ttu-id="16708-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="16708-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="16708-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="16708-102">SYNOPSIS</span></span>
<span data-ttu-id="16708-103">Aggiornare un cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="16708-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="16708-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16708-104">SYNTAX</span></span>

### <span data-ttu-id="16708-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="16708-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EnableDiskEncryption] [-EnableDoubleEncryption] [-EnablePurge] [-EnableStreamingIngest]
 [-EngineType <EngineType>] [-IdentityType <IdentityType>] [-IdentityUserAssignedIdentity <Hashtable>]
 [-KeyVaultPropertyKeyName <String>] [-KeyVaultPropertyKeyVaultUri <String>]
 [-KeyVaultPropertyKeyVersion <String>] [-KeyVaultPropertyUserIdentity <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="16708-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="16708-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoCluster -InputObject <IKustoIdentity> [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-EngineType <EngineType>] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-KeyVaultPropertyUserIdentity <String>] [-LanguageExtensionValue <ILanguageExtension[]>]
 [-Location <String>] [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>]
 [-OptimizedAutoscaleMinimum <Int32>] [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>]
 [-SkuName <AzureSkuName>] [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="16708-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16708-107">DESCRIPTION</span></span>
<span data-ttu-id="16708-108">Aggiornare un cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="16708-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="16708-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16708-109">EXAMPLES</span></span>

### <span data-ttu-id="16708-110">Esempio 1: aggiornare un cluster esistente per nome</span><span class="sxs-lookup"><span data-stu-id="16708-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="16708-111">Il comando precedente aggiorna l'USK del cluster kusto "testnewkustocluster" disponibile nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="16708-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="16708-112">Esempio 2: aggiornare un cluster esistente per nome</span><span class="sxs-lookup"><span data-stu-id="16708-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="16708-113">Il comando precedente aggiorna il cluster "testnewkustocluster" trovato nel gruppo di risorse "testrg" con una chiave gestita dal cliente.</span><span class="sxs-lookup"><span data-stu-id="16708-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="16708-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16708-114">PARAMETERS</span></span>

### <span data-ttu-id="16708-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16708-115">-AsJob</span></span>
<span data-ttu-id="16708-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="16708-116">Run the command as a job</span></span>

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

### <span data-ttu-id="16708-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16708-117">-DefaultProfile</span></span>
<span data-ttu-id="16708-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16708-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16708-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="16708-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="16708-120">Valore booleano che indica se i dischi del cluster sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="16708-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="16708-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="16708-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="16708-122">Valore booleano che indica se è abilitata la crittografia doppia.</span><span class="sxs-lookup"><span data-stu-id="16708-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="16708-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="16708-123">-EnablePurge</span></span>
<span data-ttu-id="16708-124">Valore booleano che indica se le operazioni di ripulitura sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="16708-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="16708-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="16708-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="16708-126">Valore booleano che indica se l'acquisizione del flusso è abilitata.</span><span class="sxs-lookup"><span data-stu-id="16708-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="16708-127">-EngineType</span><span class="sxs-lookup"><span data-stu-id="16708-127">-EngineType</span></span>
<span data-ttu-id="16708-128">Tipo di motore</span><span class="sxs-lookup"><span data-stu-id="16708-128">The engine type</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EngineType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16708-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="16708-129">-IdentityType</span></span>
<span data-ttu-id="16708-130">Tipo di identità gestita usata.</span><span class="sxs-lookup"><span data-stu-id="16708-130">The type of managed identity used.</span></span>
<span data-ttu-id="16708-131">Il tipo ' SystemAssigned, UserAssigned ' include sia un'identità creata in modo implicito che un set di identità assegnate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="16708-131">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="16708-132">Il tipo "None" rimuoverà tutte le identità.</span><span class="sxs-lookup"><span data-stu-id="16708-132">The type 'None' will remove all identities.</span></span>

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

### <span data-ttu-id="16708-133">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="16708-133">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="16708-134">Elenco delle identità utente associate al cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="16708-134">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="16708-135">I riferimenti chiave del dizionario delle identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="16708-135">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="16708-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16708-136">-InputObject</span></span>
<span data-ttu-id="16708-137">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="16708-137">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="16708-138">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="16708-138">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="16708-139">Il nome della chiave di volta chiave.</span><span class="sxs-lookup"><span data-stu-id="16708-139">The name of the key vault key.</span></span>

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

### <span data-ttu-id="16708-140">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="16708-140">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="16708-141">URI del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="16708-141">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="16708-142">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="16708-142">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="16708-143">La versione della chiave di volta chiave.</span><span class="sxs-lookup"><span data-stu-id="16708-143">The version of the key vault key.</span></span>

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

### <span data-ttu-id="16708-144">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="16708-144">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="16708-145">Identità assegnata dall'utente (ID risorsa ARM) che ha accesso alla chiave.</span><span class="sxs-lookup"><span data-stu-id="16708-145">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="16708-146">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="16708-146">-LanguageExtensionValue</span></span>
<span data-ttu-id="16708-147">Elenco delle estensioni della lingua.</span><span class="sxs-lookup"><span data-stu-id="16708-147">The list of language extensions.</span></span>
<span data-ttu-id="16708-148">Per costruire, vedere la sezione Note per le proprietà di LANGUAGEEXTENSIONVALUE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="16708-148">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16708-149">-Posizione</span><span class="sxs-lookup"><span data-stu-id="16708-149">-Location</span></span>
<span data-ttu-id="16708-150">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="16708-150">Resource location.</span></span>

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

### <span data-ttu-id="16708-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="16708-151">-Name</span></span>
<span data-ttu-id="16708-152">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="16708-152">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="16708-153">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="16708-153">-NoWait</span></span>
<span data-ttu-id="16708-154">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="16708-154">Run the command asynchronously</span></span>

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

### <span data-ttu-id="16708-155">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="16708-155">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="16708-156">Valore booleano che indica se la caratteristica di scalabilità ottimizzata è abilitata o meno.</span><span class="sxs-lookup"><span data-stu-id="16708-156">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="16708-157">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="16708-157">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="16708-158">Numero massimo di istanze consentite.</span><span class="sxs-lookup"><span data-stu-id="16708-158">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="16708-159">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="16708-159">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="16708-160">Conteggio istanze minime consentite.</span><span class="sxs-lookup"><span data-stu-id="16708-160">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="16708-161">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="16708-161">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="16708-162">Versione del modello definita, ad esempio 1.</span><span class="sxs-lookup"><span data-stu-id="16708-162">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="16708-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16708-163">-ResourceGroupName</span></span>
<span data-ttu-id="16708-164">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="16708-164">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="16708-165">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="16708-165">-SkuCapacity</span></span>
<span data-ttu-id="16708-166">Numero di istanze del cluster.</span><span class="sxs-lookup"><span data-stu-id="16708-166">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="16708-167">-SkuName</span><span class="sxs-lookup"><span data-stu-id="16708-167">-SkuName</span></span>
<span data-ttu-id="16708-168">Nome Usk.</span><span class="sxs-lookup"><span data-stu-id="16708-168">SKU name.</span></span>

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

### <span data-ttu-id="16708-169">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="16708-169">-SkuTier</span></span>
<span data-ttu-id="16708-170">Livello SKU.</span><span class="sxs-lookup"><span data-stu-id="16708-170">SKU tier.</span></span>

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

### <span data-ttu-id="16708-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16708-171">-SubscriptionId</span></span>
<span data-ttu-id="16708-172">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="16708-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="16708-173">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="16708-173">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="16708-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="16708-174">-Tag</span></span>
<span data-ttu-id="16708-175">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="16708-175">Resource tags.</span></span>

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

### <span data-ttu-id="16708-176">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="16708-176">-TrustedExternalTenant</span></span>
<span data-ttu-id="16708-177">Tenant esterni del cluster.</span><span class="sxs-lookup"><span data-stu-id="16708-177">The cluster's external tenants.</span></span>
<span data-ttu-id="16708-178">Per costruire, vedere la sezione Note per le proprietà di TRUSTEDEXTERNALTENANT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="16708-178">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ITrustedExternalTenant[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16708-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="16708-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="16708-180">ID risorsa indirizzo IP pubblico del servizio di gestione dati.</span><span class="sxs-lookup"><span data-stu-id="16708-180">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="16708-181">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="16708-181">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="16708-182">ID risorsa indirizzo IP pubblico del servizio motore.</span><span class="sxs-lookup"><span data-stu-id="16708-182">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="16708-183">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="16708-183">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="16708-184">ID risorsa subnet.</span><span class="sxs-lookup"><span data-stu-id="16708-184">The subnet resource id.</span></span>

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

### <span data-ttu-id="16708-185">-Confermare</span><span class="sxs-lookup"><span data-stu-id="16708-185">-Confirm</span></span>
<span data-ttu-id="16708-186">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16708-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16708-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16708-187">-WhatIf</span></span>
<span data-ttu-id="16708-188">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16708-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16708-189">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16708-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16708-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16708-190">CommonParameters</span></span>
<span data-ttu-id="16708-191">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16708-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16708-192">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16708-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16708-193">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="16708-193">INPUTS</span></span>

### <span data-ttu-id="16708-194">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="16708-194">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="16708-195">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16708-195">OUTPUTS</span></span>

### <span data-ttu-id="16708-196">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200918. ICluster</span><span class="sxs-lookup"><span data-stu-id="16708-196">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="16708-197">Note</span><span class="sxs-lookup"><span data-stu-id="16708-197">NOTES</span></span>

<span data-ttu-id="16708-198">ALIAS</span><span class="sxs-lookup"><span data-stu-id="16708-198">ALIASES</span></span>

<span data-ttu-id="16708-199">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16708-199">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="16708-200">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="16708-200">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="16708-201">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="16708-201">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="16708-202">INPUTOBJECT <IKustoIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="16708-202">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="16708-203">`[AttachedDatabaseConfigurationName <String>]`: Nome della configurazione del database allegato.</span><span class="sxs-lookup"><span data-stu-id="16708-203">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="16708-204">`[ClusterName <String>]`: Nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="16708-204">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="16708-205">`[DataConnectionName <String>]`: Nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="16708-205">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="16708-206">`[DatabaseName <String>]`: Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="16708-206">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="16708-207">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="16708-207">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="16708-208">`[Location <String>]`: Posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="16708-208">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="16708-209">`[PrincipalAssignmentName <String>]`: Il nome della principalAssignment kusto.</span><span class="sxs-lookup"><span data-stu-id="16708-209">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="16708-210">`[ResourceGroupName <String>]`: Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="16708-210">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="16708-211">`[SubscriptionId <String>]`: Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="16708-211">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="16708-212">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="16708-212">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="16708-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: l'elenco delle estensioni della lingua.</span><span class="sxs-lookup"><span data-stu-id="16708-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="16708-214">`[Name <LanguageExtensionName?>]`: Nome dell'estensione della lingua.</span><span class="sxs-lookup"><span data-stu-id="16708-214">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="16708-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: i tenant esterni del cluster.</span><span class="sxs-lookup"><span data-stu-id="16708-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="16708-216">`[Value <String>]`: GUID che rappresenta un tenant esterno.</span><span class="sxs-lookup"><span data-stu-id="16708-216">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="16708-217">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16708-217">RELATED LINKS</span></span>


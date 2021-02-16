---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 7cc359b230bc3e4480b1cc6a03db768c17ebf60c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180422"
---
# <span data-ttu-id="e7822-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="e7822-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="e7822-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7822-102">SYNOPSIS</span></span>
<span data-ttu-id="e7822-103">Aggiornare un cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e7822-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="e7822-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e7822-104">SYNTAX</span></span>

### <span data-ttu-id="e7822-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e7822-105">UpdateExpanded (Default)</span></span>
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

### <span data-ttu-id="e7822-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e7822-106">UpdateViaIdentityExpanded</span></span>
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

## <span data-ttu-id="e7822-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e7822-107">DESCRIPTION</span></span>
<span data-ttu-id="e7822-108">Aggiornare un cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e7822-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="e7822-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e7822-109">EXAMPLES</span></span>

### <span data-ttu-id="e7822-110">Esempio 1: Aggiornare un cluster esistente in base al nome</span><span class="sxs-lookup"><span data-stu-id="e7822-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="e7822-111">Il comando precedente aggiorna la SKU del cluster Kusto "testnewkustocluster" trovato nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="e7822-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="e7822-112">Esempio 2: Aggiornare un cluster esistente in base al nome</span><span class="sxs-lookup"><span data-stu-id="e7822-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="e7822-113">Il comando precedente aggiorna il cluster "testnewkustocluster" trovato nel gruppo di risorse "testrg" con una chiave gestita dal cliente.</span><span class="sxs-lookup"><span data-stu-id="e7822-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="e7822-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7822-114">PARAMETERS</span></span>

### <span data-ttu-id="e7822-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7822-115">-AsJob</span></span>
<span data-ttu-id="e7822-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="e7822-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e7822-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7822-117">-DefaultProfile</span></span>
<span data-ttu-id="e7822-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e7822-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7822-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="e7822-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="e7822-120">Valore booleano che indica se i dischi del cluster sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="e7822-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="e7822-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="e7822-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="e7822-122">Valore booleano che indica se è abilitata la doppia crittografia.</span><span class="sxs-lookup"><span data-stu-id="e7822-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="e7822-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="e7822-123">-EnablePurge</span></span>
<span data-ttu-id="e7822-124">Valore booleano che indica se le operazioni di ripulitura sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="e7822-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="e7822-125">-EnableStreamingingest</span><span class="sxs-lookup"><span data-stu-id="e7822-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="e7822-126">Valore booleano che indica se la funzionalità di inserimento del flusso è abilitata.</span><span class="sxs-lookup"><span data-stu-id="e7822-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="e7822-127">-EngineType</span><span class="sxs-lookup"><span data-stu-id="e7822-127">-EngineType</span></span>
<span data-ttu-id="e7822-128">Tipo di motore</span><span class="sxs-lookup"><span data-stu-id="e7822-128">The engine type</span></span>

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

### <span data-ttu-id="e7822-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="e7822-129">-IdentityType</span></span>
<span data-ttu-id="e7822-130">Tipo di identità gestita usata.</span><span class="sxs-lookup"><span data-stu-id="e7822-130">The type of managed identity used.</span></span>
<span data-ttu-id="e7822-131">Il tipo 'SystemAssigned, UserAssigned' include sia un'identità creata in modo implicito che un set di identità assegnate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="e7822-131">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="e7822-132">Il tipo "Nessuna" rimuove tutte le identità.</span><span class="sxs-lookup"><span data-stu-id="e7822-132">The type 'None' will remove all identities.</span></span>

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

### <span data-ttu-id="e7822-133">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e7822-133">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="e7822-134">Elenco delle identità utente associate al cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e7822-134">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="e7822-135">I riferimenti alle chiavi del dizionario delle identità utente verranno ARM ID risorsa nel formato '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="e7822-135">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="e7822-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7822-136">-InputObject</span></span>
<span data-ttu-id="e7822-137">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e7822-137">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e7822-138">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="e7822-138">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="e7822-139">Nome della chiave del vault.</span><span class="sxs-lookup"><span data-stu-id="e7822-139">The name of the key vault key.</span></span>

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

### <span data-ttu-id="e7822-140">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="e7822-140">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="e7822-141">Uri del vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="e7822-141">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="e7822-142">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="e7822-142">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="e7822-143">Versione della chiave del vault.</span><span class="sxs-lookup"><span data-stu-id="e7822-143">The version of the key vault key.</span></span>

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

### <span data-ttu-id="e7822-144">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="e7822-144">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="e7822-145">Identità assegnata dall'utente (ARM ID risorsa) che ha accesso alla chiave.</span><span class="sxs-lookup"><span data-stu-id="e7822-145">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="e7822-146">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="e7822-146">-LanguageExtensionValue</span></span>
<span data-ttu-id="e7822-147">L'elenco delle estensioni di lingua.</span><span class="sxs-lookup"><span data-stu-id="e7822-147">The list of language extensions.</span></span>
<span data-ttu-id="e7822-148">Per creare, vedere la sezione NOTE per le proprietà LANGUAGEEXTENSIONVALUE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e7822-148">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="e7822-149">-Location</span><span class="sxs-lookup"><span data-stu-id="e7822-149">-Location</span></span>
<span data-ttu-id="e7822-150">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e7822-150">Resource location.</span></span>

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

### <span data-ttu-id="e7822-151">-Name</span><span class="sxs-lookup"><span data-stu-id="e7822-151">-Name</span></span>
<span data-ttu-id="e7822-152">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e7822-152">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e7822-153">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e7822-153">-NoWait</span></span>
<span data-ttu-id="e7822-154">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="e7822-154">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e7822-155">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="e7822-155">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="e7822-156">Valore booleano che indica se la caratteristica di gradazione automatica ottimizzata è abilitata o meno.</span><span class="sxs-lookup"><span data-stu-id="e7822-156">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="e7822-157">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="e7822-157">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="e7822-158">Numero massimo di istanze consentite.</span><span class="sxs-lookup"><span data-stu-id="e7822-158">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="e7822-159">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="e7822-159">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="e7822-160">Numero minimo di istanze consentite.</span><span class="sxs-lookup"><span data-stu-id="e7822-160">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="e7822-161">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="e7822-161">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="e7822-162">Versione del modello definita, ad esempio 1.</span><span class="sxs-lookup"><span data-stu-id="e7822-162">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="e7822-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7822-163">-ResourceGroupName</span></span>
<span data-ttu-id="e7822-164">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e7822-164">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e7822-165">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="e7822-165">-SkuCapacity</span></span>
<span data-ttu-id="e7822-166">Numero di istanze del cluster.</span><span class="sxs-lookup"><span data-stu-id="e7822-166">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="e7822-167">-SKUName</span><span class="sxs-lookup"><span data-stu-id="e7822-167">-SkuName</span></span>
<span data-ttu-id="e7822-168">Nome SKU.</span><span class="sxs-lookup"><span data-stu-id="e7822-168">SKU name.</span></span>

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

### <span data-ttu-id="e7822-169">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="e7822-169">-SkuTier</span></span>
<span data-ttu-id="e7822-170">Livello SKU.</span><span class="sxs-lookup"><span data-stu-id="e7822-170">SKU tier.</span></span>

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

### <span data-ttu-id="e7822-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e7822-171">-SubscriptionId</span></span>
<span data-ttu-id="e7822-172">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e7822-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e7822-173">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="e7822-173">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e7822-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="e7822-174">-Tag</span></span>
<span data-ttu-id="e7822-175">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="e7822-175">Resource tags.</span></span>

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

### <span data-ttu-id="e7822-176">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="e7822-176">-TrustedExternalTenant</span></span>
<span data-ttu-id="e7822-177">Tenant esterni del cluster.</span><span class="sxs-lookup"><span data-stu-id="e7822-177">The cluster's external tenants.</span></span>
<span data-ttu-id="e7822-178">Per creare, vedere la sezione NOTES per le proprietà TRUSTEDEXTERNALTENANT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e7822-178">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e7822-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="e7822-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="e7822-180">ID risorsa indirizzo IP pubblico del servizio di gestione dei dati.</span><span class="sxs-lookup"><span data-stu-id="e7822-180">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="e7822-181">-VirtualNetworkConfigurationToolPublicIPId</span><span class="sxs-lookup"><span data-stu-id="e7822-181">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="e7822-182">ID risorsa indirizzo IP pubblico del servizio motore.</span><span class="sxs-lookup"><span data-stu-id="e7822-182">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="e7822-183">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="e7822-183">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="e7822-184">ID risorsa subnet.</span><span class="sxs-lookup"><span data-stu-id="e7822-184">The subnet resource id.</span></span>

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

### <span data-ttu-id="e7822-185">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7822-185">-Confirm</span></span>
<span data-ttu-id="e7822-186">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7822-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7822-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7822-187">-WhatIf</span></span>
<span data-ttu-id="e7822-188">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e7822-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7822-189">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e7822-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7822-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7822-190">CommonParameters</span></span>
<span data-ttu-id="e7822-191">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7822-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7822-192">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e7822-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7822-193">INPUT</span><span class="sxs-lookup"><span data-stu-id="e7822-193">INPUTS</span></span>

### <span data-ttu-id="e7822-194">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="e7822-194">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="e7822-195">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e7822-195">OUTPUTS</span></span>

### <span data-ttu-id="e7822-196">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="e7822-196">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="e7822-197">NOTE</span><span class="sxs-lookup"><span data-stu-id="e7822-197">NOTES</span></span>

<span data-ttu-id="e7822-198">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e7822-198">ALIASES</span></span>

<span data-ttu-id="e7822-199">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="e7822-199">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e7822-200">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e7822-200">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e7822-201">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e7822-201">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e7822-202">INPUTOBJECT <IKustoIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="e7822-202">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e7822-203">`[AttachedDatabaseConfigurationName <String>]`: nome della configurazione di database collegata.</span><span class="sxs-lookup"><span data-stu-id="e7822-203">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="e7822-204">`[ClusterName <String>]`: nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e7822-204">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="e7822-205">`[DataConnectionName <String>]`: nome della connessione dati.</span><span class="sxs-lookup"><span data-stu-id="e7822-205">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="e7822-206">`[DatabaseName <String>]`: nome del database nel cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e7822-206">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="e7822-207">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="e7822-207">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e7822-208">`[Location <String>]`: posizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e7822-208">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="e7822-209">`[PrincipalAssignmentName <String>]`: nome dell'assegnazione di Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="e7822-209">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="e7822-210">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="e7822-210">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="e7822-211">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e7822-211">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e7822-212">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="e7822-212">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="e7822-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: elenco delle estensioni delle lingue.</span><span class="sxs-lookup"><span data-stu-id="e7822-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="e7822-214">`[Name <LanguageExtensionName?>]`: nome dell'estensione della lingua.</span><span class="sxs-lookup"><span data-stu-id="e7822-214">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="e7822-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: tenant esterni del cluster.</span><span class="sxs-lookup"><span data-stu-id="e7822-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="e7822-216">`[Value <String>]`: GUID che rappresenta un tenant esterno.</span><span class="sxs-lookup"><span data-stu-id="e7822-216">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="e7822-217">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e7822-217">RELATED LINKS</span></span>


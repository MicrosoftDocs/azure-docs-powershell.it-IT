---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: c8378e9be3c92cc799eb92b9ff913be98116b019
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959597"
---
# <span data-ttu-id="ced1a-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="ced1a-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="ced1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ced1a-102">SYNOPSIS</span></span>
<span data-ttu-id="ced1a-103">Creare o aggiornare un cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ced1a-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="ced1a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ced1a-104">SYNTAX</span></span>

```
New-AzKustoCluster -Name <String> -ResourceGroupName <String> -Location <String> -SkuName <AzureSkuName>
 -SkuTier <AzureSkuTier> [-SubscriptionId <String>] [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-EngineType <EngineType>] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-KeyVaultPropertyUserIdentity <String>] [-LanguageExtensionValue <ILanguageExtension[]>]
 [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ced1a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ced1a-105">DESCRIPTION</span></span>
<span data-ttu-id="ced1a-106">Creare o aggiornare un cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ced1a-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="ced1a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ced1a-107">EXAMPLES</span></span>

### <span data-ttu-id="ced1a-108">Esempio 1: Creare un nuovo cluster Kusto</span><span class="sxs-lookup"><span data-stu-id="ced1a-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="ced1a-109">Il comando precedente crea un nuovo cluster Kusto denominato "testnewkustocluster" nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="ced1a-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="ced1a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ced1a-110">PARAMETERS</span></span>

### <span data-ttu-id="ced1a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ced1a-111">-AsJob</span></span>
<span data-ttu-id="ced1a-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="ced1a-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ced1a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ced1a-113">-DefaultProfile</span></span>
<span data-ttu-id="ced1a-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ced1a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ced1a-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="ced1a-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="ced1a-116">Valore booleano che indica se i dischi del cluster sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="ced1a-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="ced1a-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="ced1a-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="ced1a-118">Valore booleano che indica se la crittografia doppia è abilitata.</span><span class="sxs-lookup"><span data-stu-id="ced1a-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="ced1a-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="ced1a-119">-EnablePurge</span></span>
<span data-ttu-id="ced1a-120">Valore booleano che indica se le operazioni di ripulitura sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="ced1a-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="ced1a-121">-EnableStreamingingest</span><span class="sxs-lookup"><span data-stu-id="ced1a-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="ced1a-122">Valore booleano che indica se la funzionalità di inserimento in streaming è abilitata.</span><span class="sxs-lookup"><span data-stu-id="ced1a-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="ced1a-123">-EngineType</span><span class="sxs-lookup"><span data-stu-id="ced1a-123">-EngineType</span></span>
<span data-ttu-id="ced1a-124">Tipo di motore</span><span class="sxs-lookup"><span data-stu-id="ced1a-124">The engine type</span></span>

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

### <span data-ttu-id="ced1a-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ced1a-125">-IdentityType</span></span>
<span data-ttu-id="ced1a-126">Tipo di identità gestita usata.</span><span class="sxs-lookup"><span data-stu-id="ced1a-126">The type of managed identity used.</span></span>
<span data-ttu-id="ced1a-127">Il tipo 'SystemAssigned, UserAssigned' include sia un'identità creata in modo implicito che un set di identità assegnate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="ced1a-127">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="ced1a-128">Il tipo "Nessuna" rimuove tutte le identità.</span><span class="sxs-lookup"><span data-stu-id="ced1a-128">The type 'None' will remove all identities.</span></span>

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

### <span data-ttu-id="ced1a-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ced1a-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="ced1a-130">Elenco delle identità utente associate al cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ced1a-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="ced1a-131">I riferimenti alle chiavi del dizionario delle identità utente verranno ARM ID risorsa nel formato '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="ced1a-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="ced1a-132">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="ced1a-132">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="ced1a-133">Nome della chiave del vault.</span><span class="sxs-lookup"><span data-stu-id="ced1a-133">The name of the key vault key.</span></span>

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

### <span data-ttu-id="ced1a-134">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="ced1a-134">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="ced1a-135">Uri del vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="ced1a-135">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="ced1a-136">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="ced1a-136">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="ced1a-137">Versione della chiave del Vault.</span><span class="sxs-lookup"><span data-stu-id="ced1a-137">The version of the key vault key.</span></span>

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

### <span data-ttu-id="ced1a-138">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="ced1a-138">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="ced1a-139">Identità assegnata dall'utente (ARM ID risorsa) che ha accesso alla chiave.</span><span class="sxs-lookup"><span data-stu-id="ced1a-139">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="ced1a-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="ced1a-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="ced1a-141">L'elenco delle estensioni delle lingue.</span><span class="sxs-lookup"><span data-stu-id="ced1a-141">The list of language extensions.</span></span>
<span data-ttu-id="ced1a-142">Per creare, vedere la sezione NOTE per le proprietà LANGUAGEEXTENSIONVALUE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ced1a-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ced1a-143">-Location</span><span class="sxs-lookup"><span data-stu-id="ced1a-143">-Location</span></span>
<span data-ttu-id="ced1a-144">Posizione geografica in cui si trova la risorsa</span><span class="sxs-lookup"><span data-stu-id="ced1a-144">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="ced1a-145">-Name</span><span class="sxs-lookup"><span data-stu-id="ced1a-145">-Name</span></span>
<span data-ttu-id="ced1a-146">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ced1a-146">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ced1a-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ced1a-147">-NoWait</span></span>
<span data-ttu-id="ced1a-148">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="ced1a-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ced1a-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="ced1a-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="ced1a-150">Valore booleano che indica se la caratteristica di gradazione automatica ottimizzata è abilitata o meno.</span><span class="sxs-lookup"><span data-stu-id="ced1a-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="ced1a-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="ced1a-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="ced1a-152">Numero massimo di istanze consentite.</span><span class="sxs-lookup"><span data-stu-id="ced1a-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="ced1a-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="ced1a-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="ced1a-154">Numero minimo di istanze consentite.</span><span class="sxs-lookup"><span data-stu-id="ced1a-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="ced1a-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="ced1a-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="ced1a-156">Versione del modello definita, ad esempio 1.</span><span class="sxs-lookup"><span data-stu-id="ced1a-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="ced1a-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ced1a-157">-ResourceGroupName</span></span>
<span data-ttu-id="ced1a-158">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="ced1a-158">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ced1a-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ced1a-159">-SkuCapacity</span></span>
<span data-ttu-id="ced1a-160">Numero di istanze del cluster.</span><span class="sxs-lookup"><span data-stu-id="ced1a-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="ced1a-161">-SKUName</span><span class="sxs-lookup"><span data-stu-id="ced1a-161">-SkuName</span></span>
<span data-ttu-id="ced1a-162">Nome SKU.</span><span class="sxs-lookup"><span data-stu-id="ced1a-162">SKU name.</span></span>

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

### <span data-ttu-id="ced1a-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ced1a-163">-SkuTier</span></span>
<span data-ttu-id="ced1a-164">Livello SKU.</span><span class="sxs-lookup"><span data-stu-id="ced1a-164">SKU tier.</span></span>

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

### <span data-ttu-id="ced1a-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ced1a-165">-SubscriptionId</span></span>
<span data-ttu-id="ced1a-166">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ced1a-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ced1a-167">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ced1a-167">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ced1a-168">-Tag</span><span class="sxs-lookup"><span data-stu-id="ced1a-168">-Tag</span></span>
<span data-ttu-id="ced1a-169">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="ced1a-169">Resource tags.</span></span>

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

### <span data-ttu-id="ced1a-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="ced1a-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="ced1a-171">Tenant esterni del cluster.</span><span class="sxs-lookup"><span data-stu-id="ced1a-171">The cluster's external tenants.</span></span>
<span data-ttu-id="ced1a-172">Per creare, vedere la sezione NOTE per le proprietà TRUSTEDEXTERNALTENANT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ced1a-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ced1a-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="ced1a-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="ced1a-174">ID risorsa indirizzo IP pubblico del servizio di gestione dei dati.</span><span class="sxs-lookup"><span data-stu-id="ced1a-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="ced1a-175">-VirtualNetworkConfigurationConfigurationConfigurationPublicIPId</span><span class="sxs-lookup"><span data-stu-id="ced1a-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="ced1a-176">ID risorsa indirizzo IP pubblico del servizio motore.</span><span class="sxs-lookup"><span data-stu-id="ced1a-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="ced1a-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="ced1a-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="ced1a-178">ID risorsa subnet.</span><span class="sxs-lookup"><span data-stu-id="ced1a-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="ced1a-179">-Zone</span><span class="sxs-lookup"><span data-stu-id="ced1a-179">-Zone</span></span>
<span data-ttu-id="ced1a-180">Aree di disponibilità del cluster.</span><span class="sxs-lookup"><span data-stu-id="ced1a-180">The availability zones of the cluster.</span></span>

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

### <span data-ttu-id="ced1a-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ced1a-181">-Confirm</span></span>
<span data-ttu-id="ced1a-182">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ced1a-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ced1a-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ced1a-183">-WhatIf</span></span>
<span data-ttu-id="ced1a-184">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ced1a-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ced1a-185">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ced1a-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ced1a-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ced1a-186">CommonParameters</span></span>
<span data-ttu-id="ced1a-187">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ced1a-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ced1a-188">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ced1a-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ced1a-189">INPUT</span><span class="sxs-lookup"><span data-stu-id="ced1a-189">INPUTS</span></span>

## <span data-ttu-id="ced1a-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ced1a-190">OUTPUTS</span></span>

### <span data-ttu-id="ced1a-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="ced1a-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="ced1a-192">NOTE</span><span class="sxs-lookup"><span data-stu-id="ced1a-192">NOTES</span></span>

<span data-ttu-id="ced1a-193">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ced1a-193">ALIASES</span></span>

<span data-ttu-id="ced1a-194">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="ced1a-194">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ced1a-195">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ced1a-195">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ced1a-196">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ced1a-196">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ced1a-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: elenco delle estensioni delle lingue.</span><span class="sxs-lookup"><span data-stu-id="ced1a-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="ced1a-198">`[Name <LanguageExtensionName?>]`: nome dell'estensione della lingua.</span><span class="sxs-lookup"><span data-stu-id="ced1a-198">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="ced1a-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: tenant esterni del cluster.</span><span class="sxs-lookup"><span data-stu-id="ced1a-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="ced1a-200">`[Value <String>]`: GUID che rappresenta un tenant esterno.</span><span class="sxs-lookup"><span data-stu-id="ced1a-200">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="ced1a-201">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ced1a-201">RELATED LINKS</span></span>


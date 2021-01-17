---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b868633f0217b2048f0a83641f678e9c092d21c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476952"
---
# <span data-ttu-id="aa89b-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="aa89b-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="aa89b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aa89b-102">SYNOPSIS</span></span>
<span data-ttu-id="aa89b-103">Creare o aggiornare un cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="aa89b-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="aa89b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa89b-104">SYNTAX</span></span>

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

## <span data-ttu-id="aa89b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa89b-105">DESCRIPTION</span></span>
<span data-ttu-id="aa89b-106">Creare o aggiornare un cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="aa89b-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="aa89b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa89b-107">EXAMPLES</span></span>

### <span data-ttu-id="aa89b-108">Esempio 1: creare un nuovo cluster di Kusto</span><span class="sxs-lookup"><span data-stu-id="aa89b-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="aa89b-109">Il comando precedente crea un nuovo cluster di Kusto denominato "testnewkustocluster" nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="aa89b-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="aa89b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aa89b-110">PARAMETERS</span></span>

### <span data-ttu-id="aa89b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa89b-111">-AsJob</span></span>
<span data-ttu-id="aa89b-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="aa89b-112">Run the command as a job</span></span>

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

### <span data-ttu-id="aa89b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa89b-113">-DefaultProfile</span></span>
<span data-ttu-id="aa89b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aa89b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa89b-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="aa89b-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="aa89b-116">Valore booleano che indica se i dischi del cluster sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="aa89b-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="aa89b-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="aa89b-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="aa89b-118">Valore booleano che indica se è abilitata la crittografia doppia.</span><span class="sxs-lookup"><span data-stu-id="aa89b-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="aa89b-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="aa89b-119">-EnablePurge</span></span>
<span data-ttu-id="aa89b-120">Valore booleano che indica se le operazioni di ripulitura sono abilitate.</span><span class="sxs-lookup"><span data-stu-id="aa89b-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="aa89b-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="aa89b-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="aa89b-122">Valore booleano che indica se l'acquisizione del flusso è abilitata.</span><span class="sxs-lookup"><span data-stu-id="aa89b-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="aa89b-123">-EngineType</span><span class="sxs-lookup"><span data-stu-id="aa89b-123">-EngineType</span></span>
<span data-ttu-id="aa89b-124">Tipo di motore</span><span class="sxs-lookup"><span data-stu-id="aa89b-124">The engine type</span></span>

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

### <span data-ttu-id="aa89b-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="aa89b-125">-IdentityType</span></span>
<span data-ttu-id="aa89b-126">Tipo di identità gestita usata.</span><span class="sxs-lookup"><span data-stu-id="aa89b-126">The type of managed identity used.</span></span>
<span data-ttu-id="aa89b-127">Il tipo ' SystemAssigned, UserAssigned ' include sia un'identità creata in modo implicito che un set di identità assegnate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="aa89b-127">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="aa89b-128">Il tipo "None" rimuoverà tutte le identità.</span><span class="sxs-lookup"><span data-stu-id="aa89b-128">The type 'None' will remove all identities.</span></span>

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

### <span data-ttu-id="aa89b-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="aa89b-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="aa89b-130">Elenco delle identità utente associate al cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="aa89b-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="aa89b-131">I riferimenti chiave del dizionario delle identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span><span class="sxs-lookup"><span data-stu-id="aa89b-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="aa89b-132">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="aa89b-132">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="aa89b-133">Il nome della chiave di volta chiave.</span><span class="sxs-lookup"><span data-stu-id="aa89b-133">The name of the key vault key.</span></span>

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

### <span data-ttu-id="aa89b-134">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="aa89b-134">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="aa89b-135">URI del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="aa89b-135">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="aa89b-136">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="aa89b-136">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="aa89b-137">La versione della chiave di volta chiave.</span><span class="sxs-lookup"><span data-stu-id="aa89b-137">The version of the key vault key.</span></span>

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

### <span data-ttu-id="aa89b-138">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="aa89b-138">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="aa89b-139">Identità assegnata dall'utente (ID risorsa ARM) che ha accesso alla chiave.</span><span class="sxs-lookup"><span data-stu-id="aa89b-139">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="aa89b-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="aa89b-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="aa89b-141">Elenco delle estensioni della lingua.</span><span class="sxs-lookup"><span data-stu-id="aa89b-141">The list of language extensions.</span></span>
<span data-ttu-id="aa89b-142">Per costruire, vedere la sezione Note per le proprietà di LANGUAGEEXTENSIONVALUE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="aa89b-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="aa89b-143">-Posizione</span><span class="sxs-lookup"><span data-stu-id="aa89b-143">-Location</span></span>
<span data-ttu-id="aa89b-144">Posizione geografica in cui vive la risorsa</span><span class="sxs-lookup"><span data-stu-id="aa89b-144">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="aa89b-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa89b-145">-Name</span></span>
<span data-ttu-id="aa89b-146">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="aa89b-146">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="aa89b-147">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="aa89b-147">-NoWait</span></span>
<span data-ttu-id="aa89b-148">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="aa89b-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="aa89b-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="aa89b-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="aa89b-150">Valore booleano che indica se la caratteristica di scalabilità ottimizzata è abilitata o meno.</span><span class="sxs-lookup"><span data-stu-id="aa89b-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="aa89b-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="aa89b-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="aa89b-152">Numero massimo di istanze consentite.</span><span class="sxs-lookup"><span data-stu-id="aa89b-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="aa89b-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="aa89b-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="aa89b-154">Conteggio istanze minime consentite.</span><span class="sxs-lookup"><span data-stu-id="aa89b-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="aa89b-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="aa89b-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="aa89b-156">Versione del modello definita, ad esempio 1.</span><span class="sxs-lookup"><span data-stu-id="aa89b-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="aa89b-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa89b-157">-ResourceGroupName</span></span>
<span data-ttu-id="aa89b-158">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="aa89b-158">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="aa89b-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="aa89b-159">-SkuCapacity</span></span>
<span data-ttu-id="aa89b-160">Numero di istanze del cluster.</span><span class="sxs-lookup"><span data-stu-id="aa89b-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="aa89b-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="aa89b-161">-SkuName</span></span>
<span data-ttu-id="aa89b-162">Nome Usk.</span><span class="sxs-lookup"><span data-stu-id="aa89b-162">SKU name.</span></span>

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

### <span data-ttu-id="aa89b-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="aa89b-163">-SkuTier</span></span>
<span data-ttu-id="aa89b-164">Livello SKU.</span><span class="sxs-lookup"><span data-stu-id="aa89b-164">SKU tier.</span></span>

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

### <span data-ttu-id="aa89b-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa89b-165">-SubscriptionId</span></span>
<span data-ttu-id="aa89b-166">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="aa89b-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="aa89b-167">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="aa89b-167">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="aa89b-168">-Tag</span><span class="sxs-lookup"><span data-stu-id="aa89b-168">-Tag</span></span>
<span data-ttu-id="aa89b-169">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="aa89b-169">Resource tags.</span></span>

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

### <span data-ttu-id="aa89b-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="aa89b-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="aa89b-171">Tenant esterni del cluster.</span><span class="sxs-lookup"><span data-stu-id="aa89b-171">The cluster's external tenants.</span></span>
<span data-ttu-id="aa89b-172">Per costruire, vedere la sezione Note per le proprietà di TRUSTEDEXTERNALTENANT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="aa89b-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="aa89b-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="aa89b-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="aa89b-174">ID risorsa indirizzo IP pubblico del servizio di gestione dati.</span><span class="sxs-lookup"><span data-stu-id="aa89b-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="aa89b-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="aa89b-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="aa89b-176">ID risorsa indirizzo IP pubblico del servizio motore.</span><span class="sxs-lookup"><span data-stu-id="aa89b-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="aa89b-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="aa89b-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="aa89b-178">ID risorsa subnet.</span><span class="sxs-lookup"><span data-stu-id="aa89b-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="aa89b-179">-Zona</span><span class="sxs-lookup"><span data-stu-id="aa89b-179">-Zone</span></span>
<span data-ttu-id="aa89b-180">Aree di disponibilità del cluster.</span><span class="sxs-lookup"><span data-stu-id="aa89b-180">The availability zones of the cluster.</span></span>

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

### <span data-ttu-id="aa89b-181">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aa89b-181">-Confirm</span></span>
<span data-ttu-id="aa89b-182">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa89b-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa89b-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa89b-183">-WhatIf</span></span>
<span data-ttu-id="aa89b-184">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa89b-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa89b-185">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa89b-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa89b-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa89b-186">CommonParameters</span></span>
<span data-ttu-id="aa89b-187">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa89b-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa89b-188">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa89b-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa89b-189">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aa89b-189">INPUTS</span></span>

## <span data-ttu-id="aa89b-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa89b-190">OUTPUTS</span></span>

### <span data-ttu-id="aa89b-191">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200918. ICluster</span><span class="sxs-lookup"><span data-stu-id="aa89b-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="aa89b-192">Note</span><span class="sxs-lookup"><span data-stu-id="aa89b-192">NOTES</span></span>

<span data-ttu-id="aa89b-193">ALIAS</span><span class="sxs-lookup"><span data-stu-id="aa89b-193">ALIASES</span></span>

<span data-ttu-id="aa89b-194">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aa89b-194">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aa89b-195">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="aa89b-195">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aa89b-196">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aa89b-196">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aa89b-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: l'elenco delle estensioni della lingua.</span><span class="sxs-lookup"><span data-stu-id="aa89b-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="aa89b-198">`[Name <LanguageExtensionName?>]`: Nome dell'estensione della lingua.</span><span class="sxs-lookup"><span data-stu-id="aa89b-198">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="aa89b-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: i tenant esterni del cluster.</span><span class="sxs-lookup"><span data-stu-id="aa89b-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="aa89b-200">`[Value <String>]`: GUID che rappresenta un tenant esterno.</span><span class="sxs-lookup"><span data-stu-id="aa89b-200">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="aa89b-201">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa89b-201">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: f13a92bef4bfbafc67beec6d99cf02d8d1d63c31
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200897"
---
# <span data-ttu-id="ac6e1-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="ac6e1-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="ac6e1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ac6e1-102">SYNOPSIS</span></span>
<span data-ttu-id="ac6e1-103">Aggiorna lo spazio dei nomi degli hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="ac6e1-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="ac6e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac6e1-104">SYNTAX</span></span>

### <span data-ttu-id="ac6e1-105">NamespaceParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ac6e1-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-Identity] [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac6e1-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac6e1-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity]
 [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac6e1-107">IdentityUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac6e1-107">IdentityUpdateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac6e1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac6e1-108">DESCRIPTION</span></span>
<span data-ttu-id="ac6e1-109">Il cmdlet Set-AzEventHubNamespace aggiorna le proprietà dello spazio dei nomi degli hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="ac6e1-109">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="ac6e1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac6e1-110">EXAMPLES</span></span>

### <span data-ttu-id="ac6e1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ac6e1-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -Tag @{Tag1='TagValue1'; Tag2='TagValue2'}

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   : {Tag2, TagValue2, Tag1, TagValue1}
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10

```

<span data-ttu-id="ac6e1-112">Aggiorna i tag per lo spazio dei nomi NamespaceName \` \` in created.</span><span class="sxs-lookup"><span data-stu-id="ac6e1-112">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="ac6e1-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ac6e1-113">Example 2</span></span>
```powershell
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10 

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroup          : Default-EventHub-WestCentralUS
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="ac6e1-114">Aggiorna lo stato dello spazio dei nomi MyNamespace \` \` con AutoInflate = Enabled e MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="ac6e1-114">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

### <span data-ttu-id="ac6e1-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="ac6e1-115">Example 3</span></span>

<span data-ttu-id="ac6e1-116">Aggiorna lo spazio dei nomi degli hub eventi specificati.</span><span class="sxs-lookup"><span data-stu-id="ac6e1-116">Updates the specified Event Hubs namespace.</span></span> <span data-ttu-id="ac6e1-117">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="ac6e1-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzEventHubNamespace -Location 'WestUS' -Name MyNamespaceName -ResourceGroupName MyResourceGroupName -SkuName Basic
```

### <span data-ttu-id="ac6e1-118">Esempio 5: creazione e aggiornamento dello spazio dei nomi con Gestisci identità in un cluster</span><span class="sxs-lookup"><span data-stu-id="ac6e1-118">Example 5: Creating and updating Namespace with Manage Identity in a cluster</span></span> 
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation --EnableAutoInflate -MaximumThroughputUnits 12 -EnableKafka -ZoneRedundant -Identity

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 6/12/2020 4:00:29 AM
UpdatedAt                     : 6/14/2020 11:33:12 PM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 12
ZoneRedundant                 : True
ClusterArmId                  : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/clusters/TestCluster
Identity.PrincipalId          : ##########
Identity.TenantId             : ##########
Identity.Type                 : SystemAssigned
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :

# Get created namespace
PS C:\> $getnamespace = Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName

# Create KeyVault
PS C:\>$Keyvault = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Set Access policy on the KeyVault
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName testingnewCluster -ObjectId $getnamespace.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get -BypassObjectIdValidation

# Add a key to KeyVault
$key = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Update Namespace with KeyVault properties

PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName -Location westus -KeySource Microsoft.KeyVault -KeyProperty @(@($key.Name, $keyvault.VaultUri,""))

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 6/12/2020 4:00:29 AM
UpdatedAt                     : 6/14/2020 11:33:12 PM
ServiceBusEndpoint            : #########
Enabled                       : True
KafkaEnabled                  : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/clusters/TestCluster
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          : #########
Identity.TenantId             : #########
Identity.Type                 : SystemAssigned
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          : MicrosoftKeyVault
Encryption.KeyVaultProperties : {testkey, https://myvaultname.vault.azure.net, }
```

## <span data-ttu-id="ac6e1-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ac6e1-119">PARAMETERS</span></span>

### <span data-ttu-id="ac6e1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac6e1-120">-DefaultProfile</span></span>
<span data-ttu-id="ac6e1-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac6e1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac6e1-122">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="ac6e1-122">-EnableAutoInflate</span></span>
<span data-ttu-id="ac6e1-123">Indica se AutoInflate è abilitato</span><span class="sxs-lookup"><span data-stu-id="ac6e1-123">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet, IdentityUpdateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac6e1-124">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="ac6e1-124">-EnableKafka</span></span>
<span data-ttu-id="ac6e1-125">Abilitazione o disabilitazione di Kafka per lo spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ac6e1-125">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="ac6e1-126">-Identità</span><span class="sxs-lookup"><span data-stu-id="ac6e1-126">-Identity</span></span>
<span data-ttu-id="ac6e1-127">Abilitazione o disabilitazione dell'identità per lo spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ac6e1-127">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="ac6e1-128">-IdentityUserDefined</span><span class="sxs-lookup"><span data-stu-id="ac6e1-128">-IdentityUserDefined</span></span>
<span data-ttu-id="ac6e1-129">Identità definita dall'utente o nessuna</span><span class="sxs-lookup"><span data-stu-id="ac6e1-129">User defined Identity or None</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac6e1-130">-Proprietà Property</span><span class="sxs-lookup"><span data-stu-id="ac6e1-130">-KeyProperty</span></span>
<span data-ttu-id="ac6e1-131">Elenco delle proprietà delle chiavi, @ (@ (nome tasto, KeyVaultUri, versione di chiave), @ (nome tasto, KeyVaultUri, versione di tastiera))</span><span class="sxs-lookup"><span data-stu-id="ac6e1-131">List of Key Properties, @(@(KeyName,KeyVaultUri,Keyversion),@(KeyName,KeyVaultUri,Keyversion))</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String[]]
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac6e1-132">-Sorgente di origine</span><span class="sxs-lookup"><span data-stu-id="ac6e1-132">-KeySource</span></span>
<span data-ttu-id="ac6e1-133">Origine chiave</span><span class="sxs-lookup"><span data-stu-id="ac6e1-133">Key Source</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac6e1-134">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ac6e1-134">-Location</span></span>
<span data-ttu-id="ac6e1-135">Posizione dello spazio dei nomi EventHub.</span><span class="sxs-lookup"><span data-stu-id="ac6e1-135">EventHub Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6e1-136">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="ac6e1-136">-MaximumThroughputUnits</span></span>
<span data-ttu-id="ac6e1-137">Limite superiore delle unità di velocità effettiva quando AutoInflate è abilitato, il valore deve essere compreso tra 0 e 20 unità di velocità effettiva.</span><span class="sxs-lookup"><span data-stu-id="ac6e1-137">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet, IdentityUpdateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6e1-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac6e1-138">-Name</span></span>
<span data-ttu-id="ac6e1-139">Nome dello spazio dei nomi EventHub.</span><span class="sxs-lookup"><span data-stu-id="ac6e1-139">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6e1-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac6e1-140">-ResourceGroupName</span></span>
<span data-ttu-id="ac6e1-141">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ac6e1-141">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6e1-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ac6e1-142">-SkuCapacity</span></span>
<span data-ttu-id="ac6e1-143">Unità throughput eventhub.</span><span class="sxs-lookup"><span data-stu-id="ac6e1-143">The eventhub throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6e1-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ac6e1-144">-SkuName</span></span>
<span data-ttu-id="ac6e1-145">Nome SKU dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ac6e1-145">Namespace Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6e1-146">-Stato</span><span class="sxs-lookup"><span data-stu-id="ac6e1-146">-State</span></span>
<span data-ttu-id="ac6e1-147">Disabilitare/abilitare lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ac6e1-147">Disable/Enable Namespace.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.EventHub.Models.NamespaceState]
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6e1-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="ac6e1-148">-Tag</span></span>
<span data-ttu-id="ac6e1-149">Hashtable che rappresenta il tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="ac6e1-149">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6e1-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ac6e1-150">-Confirm</span></span>
<span data-ttu-id="ac6e1-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac6e1-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac6e1-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac6e1-152">-WhatIf</span></span>
<span data-ttu-id="ac6e1-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac6e1-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac6e1-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac6e1-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac6e1-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac6e1-155">CommonParameters</span></span>
<span data-ttu-id="ac6e1-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac6e1-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac6e1-157">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac6e1-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac6e1-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ac6e1-158">INPUTS</span></span>

### <span data-ttu-id="ac6e1-159">System. String</span><span class="sxs-lookup"><span data-stu-id="ac6e1-159">System.String</span></span>

### <span data-ttu-id="ac6e1-160">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ac6e1-160">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ac6e1-161">System. Nullable ' 1 [[Microsoft. Azure. Commands. EventHub. Models. NamespaceState, Microsoft. Azure. PowerShell. Cmdlets. EventHub, Version = 1.4.3.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ac6e1-161">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.4.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ac6e1-162">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ac6e1-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ac6e1-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac6e1-163">OUTPUTS</span></span>

### <span data-ttu-id="ac6e1-164">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ac6e1-164">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="ac6e1-165">Note</span><span class="sxs-lookup"><span data-stu-id="ac6e1-165">NOTES</span></span>

## <span data-ttu-id="ac6e1-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac6e1-166">RELATED LINKS</span></span>

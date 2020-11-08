---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: a51fffe36102b05121e52054103357bd26f56d51
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193422"
---
# <span data-ttu-id="7bb95-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="7bb95-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="7bb95-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7bb95-102">SYNOPSIS</span></span>
<span data-ttu-id="7bb95-103">Crea uno spazio dei nomi Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="7bb95-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="7bb95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7bb95-104">SYNTAX</span></span>

### <span data-ttu-id="7bb95-105">NamespaceParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7bb95-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka] [-ZoneRedundant]
 [[-ClusterARMId] <String>] [-Identity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7bb95-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bb95-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-ZoneRedundant] [[-ClusterARMId] <String>] [-Identity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bb95-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7bb95-107">DESCRIPTION</span></span>
<span data-ttu-id="7bb95-108">Il cmdlet New-AzEventHubNamespace crea un nuovo spazio dei nomi di tipo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="7bb95-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="7bb95-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7bb95-109">EXAMPLES</span></span>
### <span data-ttu-id="7bb95-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7bb95-110">Example 1</span></span>                                           
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 6/14/2020 9:02:16 PM
UpdatedAt                     : 6/14/2020 9:03:04 PM
ServiceBusEndpoint            : https://testingnew2018.servicebus.windows.net:443/
Enabled                       : True
KafkaEnabled                  : True
IsAutoInflateEnabled          : False
MaximumThroughputUnits        : 0
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="7bb95-111">Crea uno spazio dei nomi Hub di eventi MyNamespace \` \` nella posizione geografica specificata \` in location \` , nel gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="7bb95-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="7bb95-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7bb95-112">Example 2</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="7bb95-113">Crea uno spazio dei nomi Hub di eventi MyNamespace \` \` nella posizione geografica specificata \` in location \` , nel gruppo di risorse \` MyResourceGroupName \` e AutoInflate è abilitato con MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="7bb95-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="7bb95-114">Esempio 3: spazio dei nomi abilitato per Kafka</span><span class="sxs-lookup"><span data-stu-id="7bb95-114">Example 3: Kafka enabled namespace</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="7bb95-115">Crea uno spazio dei nomi Hub di eventi MyNamespace \` \` nella posizione geografica specificata \` in location \` , nel gruppo di risorse \` MyResourceGroupName \` con Kafka e AutoInflate abilitato.</span><span class="sxs-lookup"><span data-stu-id="7bb95-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="7bb95-116">Esempio 4: spazio dei nomi abilitato per ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="7bb95-116">Example 4: ZoneRedundant enabled namespace</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -ZoneRedundant

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : True
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="7bb95-117">Crea uno spazio dei nomi Hub di eventi MyNamespace \` \` nella posizione geografica specificata \` in location \` , nel gruppo di risorse \` MyResourceGroupName \` con Kafka e AutoInflate abilitato.</span><span class="sxs-lookup"><span data-stu-id="7bb95-117">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="7bb95-118">Esempio 5: creazione dello spazio dei nomi con Gestisci identità in un cluster</span><span class="sxs-lookup"><span data-stu-id="7bb95-118">Example 5: Creating Namespace with Manage Identity in a cluster</span></span> 
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
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
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
PS C:\>$getnamespace = Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName

# Create KeyVault
PS C:\>$Keyvault = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Set Access policy on the KeyVault
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName testingnewCluster -ObjectId $getnamespace.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get -BypassObjectIdValidation

# Add a key to KeyVault
PS C:\> $key = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Update Namespace with KeyVault properties

PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName -Location westus -KeySource Microsoft.KeyVault -KeyProperties @(@($key.Name, $keyvault.VaultUri,""))

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

## <span data-ttu-id="7bb95-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7bb95-119">PARAMETERS</span></span>

### <span data-ttu-id="7bb95-120">-ClusterARMId</span><span class="sxs-lookup"><span data-stu-id="7bb95-120">-ClusterARMId</span></span>
<span data-ttu-id="7bb95-121">ID ARM del cluster in cui deve essere creato lo spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7bb95-121">ARM ID of Cluster where namespace is to be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bb95-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bb95-122">-DefaultProfile</span></span>
<span data-ttu-id="7bb95-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7bb95-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bb95-124">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="7bb95-124">-EnableAutoInflate</span></span>
<span data-ttu-id="7bb95-125">Indica se AutoInflate è abilitato</span><span class="sxs-lookup"><span data-stu-id="7bb95-125">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb95-126">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="7bb95-126">-EnableKafka</span></span>
<span data-ttu-id="7bb95-127">Abilitazione o disabilitazione di Kafka per lo spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7bb95-127">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="7bb95-128">-Identità</span><span class="sxs-lookup"><span data-stu-id="7bb95-128">-Identity</span></span>
<span data-ttu-id="7bb95-129">Abilitazione o disabilitazione dell'identità per lo spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7bb95-129">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="7bb95-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7bb95-130">-Location</span></span>
<span data-ttu-id="7bb95-131">Posizione dello spazio dei nomi EventHub.</span><span class="sxs-lookup"><span data-stu-id="7bb95-131">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="7bb95-132">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="7bb95-132">-MaximumThroughputUnits</span></span>
<span data-ttu-id="7bb95-133">Limite superiore delle unità di velocità effettiva quando AutoInflate è abilitato, il valore deve essere compreso tra 0 e 20 unità di velocità effettiva.</span><span class="sxs-lookup"><span data-stu-id="7bb95-133">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bb95-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="7bb95-134">-Name</span></span>
<span data-ttu-id="7bb95-135">Nome dello spazio dei nomi EventHub.</span><span class="sxs-lookup"><span data-stu-id="7bb95-135">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="7bb95-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bb95-136">-ResourceGroupName</span></span>
<span data-ttu-id="7bb95-137">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="7bb95-137">Resource Group Name</span></span>

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

### <span data-ttu-id="7bb95-138">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="7bb95-138">-SkuCapacity</span></span>
<span data-ttu-id="7bb95-139">Unità throughput eventhub.</span><span class="sxs-lookup"><span data-stu-id="7bb95-139">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="7bb95-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7bb95-140">-SkuName</span></span>
<span data-ttu-id="7bb95-141">Nome SKU dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="7bb95-141">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="7bb95-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="7bb95-142">-Tag</span></span>
<span data-ttu-id="7bb95-143">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="7bb95-143">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bb95-144">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="7bb95-144">-ZoneRedundant</span></span>
<span data-ttu-id="7bb95-145">Abilitazione o disabilitazione dell'area ridondante per lo spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7bb95-145">enabling or disabling Zone Redundant for namespace</span></span>

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

### <span data-ttu-id="7bb95-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7bb95-146">-Confirm</span></span>
<span data-ttu-id="7bb95-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bb95-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bb95-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bb95-148">-WhatIf</span></span>
<span data-ttu-id="7bb95-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7bb95-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bb95-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7bb95-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bb95-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bb95-151">CommonParameters</span></span>
<span data-ttu-id="7bb95-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bb95-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bb95-153">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7bb95-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bb95-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7bb95-154">INPUTS</span></span>

### <span data-ttu-id="7bb95-155">System. String</span><span class="sxs-lookup"><span data-stu-id="7bb95-155">System.String</span></span>

### <span data-ttu-id="7bb95-156">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7bb95-156">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7bb95-157">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7bb95-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7bb95-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7bb95-158">OUTPUTS</span></span>

### <span data-ttu-id="7bb95-159">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="7bb95-159">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="7bb95-160">Note</span><span class="sxs-lookup"><span data-stu-id="7bb95-160">NOTES</span></span>

## <span data-ttu-id="7bb95-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7bb95-161">RELATED LINKS</span></span>
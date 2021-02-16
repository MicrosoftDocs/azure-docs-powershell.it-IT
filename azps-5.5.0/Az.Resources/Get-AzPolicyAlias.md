---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAlias.md
ms.openlocfilehash: b2881c735caae8f644676b1ee19cb0d80725c13a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186503"
---
# <span data-ttu-id="75784-101">Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="75784-101">Get-AzPolicyAlias</span></span>

## <span data-ttu-id="75784-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75784-102">SYNOPSIS</span></span>
<span data-ttu-id="75784-103">Get-AzPolicyAlias recupera e restituisce i tipi di risorse del provider di Azure che hanno alias definiti e corrispondenti ai valori dei parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="75784-103">Get-AzPolicyAlias retrieves and outputs Azure provider resource types that have aliases defined and match the given parameter values.</span></span> <span data-ttu-id="75784-104">Se non vengono forniti parametri, verranno restituiti tutti i tipi di risorse provider che contengono un alias.</span><span class="sxs-lookup"><span data-stu-id="75784-104">If no parameters are provided, all provider resource types that contain an alias will be output.</span></span>
<span data-ttu-id="75784-105">L'opzione -ListAvailable modifica questo comportamento elencando tutti i tipi di risorse corrispondenti, inclusi quelli senza alias.</span><span class="sxs-lookup"><span data-stu-id="75784-105">The -ListAvailable switch modifies this behavior by listing all matching resource types including those without aliases.</span></span>

## <span data-ttu-id="75784-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75784-106">SYNTAX</span></span>

```
Get-AzPolicyAlias [-NamespaceMatch <String>] [-ResourceTypeMatch <String>] [-AliasMatch <String>]
 [-PathMatch <String>] [-ApiVersionMatch <String>] [-LocationMatch <String>] [-ListAvailable]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75784-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="75784-107">DESCRIPTION</span></span>
<span data-ttu-id="75784-108">Il **cmdlet Get-AzPolicyAlias** ottiene un elenco di alias dei criteri.</span><span class="sxs-lookup"><span data-stu-id="75784-108">The **Get-AzPolicyAlias** cmdlet gets a listing of policy aliases.</span></span>
<span data-ttu-id="75784-109">Gli alias dei criteri vengono usati dai criteri di Azure per fare riferimento alle proprietà del tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="75784-109">Policy aliases are used by Azure Policy to refer to resource type properties.</span></span>
<span data-ttu-id="75784-110">Vengono forniti parametri che limitano gli elementi nell'elenco abbinando varie proprietà del tipo di risorsa o i relativi alias.</span><span class="sxs-lookup"><span data-stu-id="75784-110">Parameters are provided that limit items in the listing by matching various properties of the resource type or its aliases.</span></span>
<span data-ttu-id="75784-111">Un determinato valore di corrispondenza corrisponde se la stringa di destinazione lo contiene usando un confronto senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="75784-111">A given match value matches if the target string contains it using case insensitive comparison.</span></span>

## <span data-ttu-id="75784-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75784-112">EXAMPLES</span></span>

### <span data-ttu-id="75784-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="75784-113">Example 1</span></span>
```powershell
PS C:\> Get-AzPolicyAlias

Namespace                     ResourceType                                   Aliases
---------                     ------------                                   -------
Microsoft.AnalysisServices    servers                                        {Microsoft.AnalysisServices/servers/state, Microsoft.AnalysisServices/s...
Microsoft.Authorization       roleAssignments                                {Microsoft.Authorization/roleAssignments/roleDefinitionId, Microsoft.Au...
Microsoft.Authorization       roleDefinitions                                {Microsoft.Authorization/roleDefinitions/type, Microsoft.Authorization/...

...                           ...                                            ...

Microsoft.Web                 hostingEnvironments                            {Microsoft.Web/hostingEnvironments/clusterSettings[*].name, Microsoft.W...
Microsoft.Web                 sites/config                                   {Microsoft.Web/sites/config/httpLoggingEnabled, Microsoft.Web/sites/con...
Microsoft.GuestConfiguration  guestConfigurationAssignments                  {Microsoft.GuestConfiguration/guestConfigurationAssignments/complianceS...


PS C:\>
```

<span data-ttu-id="75784-114">Elenca tutti i tipi di risorse provider che hanno un alias.</span><span class="sxs-lookup"><span data-stu-id="75784-114">Lists all provider resource types that have an alias.</span></span>

### <span data-ttu-id="75784-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="75784-115">Example 2</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ListAvailable

Namespace                                ResourceType                                                        Aliases
---------                                ------------                                                        -------

...                                      ...                                                                 ...

Microsoft.AlertsManagement               operations                                                          {}
Microsoft.AnalysisServices               servers                                                             {Microsoft.AnalysisServices/servers/sta...
Microsoft.AnalysisServices               locations                                                           {}

...                                      ...                                                                 ...


PS C:\>
```

<span data-ttu-id="75784-116">Elenco di tutti i tipi di risorse provider, inclusi quelli senza alias.</span><span class="sxs-lookup"><span data-stu-id="75784-116">Lists all provider resource types, including those without aliases.</span></span>

### <span data-ttu-id="75784-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="75784-117">Example 3</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -NamespaceMatch 'compute'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...
Microsoft.Compute disks                              {Microsoft.Compute/imagePublisher, Microsoft.Compute/imageOffer, Microsoft.Compute/imageSku, Mi...


PS C:\>
```

<span data-ttu-id="75784-118">Elenco di tutti i tipi di risorse provider il cui spazio dei nomi corrisponde a "compute" e contengono un alias.</span><span class="sxs-lookup"><span data-stu-id="75784-118">Lists all provider resource types whose namespace matches 'compute' and contain an alias.</span></span>

### <span data-ttu-id="75784-119">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="75784-119">Example 4</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ResourceTypeMatch 'virtual'

Namespace         ResourceType                           Aliases
---------         ------------                           -------
Microsoft.Compute virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Micro...
Microsoft.Compute virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualM...
Microsoft.Compute virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleS...
Microsoft.Compute virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/...
Microsoft.Network virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGateway...
Microsoft.Network virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetworks...
Microsoft.Network virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql     servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers/vi...


PS C:\>
```

<span data-ttu-id="75784-120">Elenco di tutti i tipi di risorse provider il cui tipo di risorsa corrisponde a "virtuale" e che contengono un alias.</span><span class="sxs-lookup"><span data-stu-id="75784-120">Lists all provider resource types whose resource type matches 'virtual' and contain an alias.</span></span>

### <span data-ttu-id="75784-121">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="75784-121">Example 5</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ResourceTypeMatch 'virtual' -ListAvailable

Namespace                    ResourceType                                               Aliases
---------                    ------------                                               -------

...                          ...                                                        ...

Microsoft.KeyVault           locations/deleteVirtualNetworkOrSubnets                    {}
Microsoft.Network            virtualNetworks                                            {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id,...
Microsoft.Network            virtualNetworkGateways                                     {Microsoft.Network/virtualNetworkGateways/sku.name, Microsof...
Microsoft.Network            locations/virtualNetworkAvailableEndpointServices          {}

...                          ...                                                        ...


PS C:\>
```

<span data-ttu-id="75784-122">Elenca tutti i tipi di risorse provider il cui tipo di risorsa corrisponde a "virtuale", inclusi quelli senza alias.</span><span class="sxs-lookup"><span data-stu-id="75784-122">Lists all provider resource types whose resource type matches 'virtual', including those without aliases.</span></span>

### <span data-ttu-id="75784-123">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="75784-123">Example 6</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -NamespaceMatch 'compute' -ResourceTypeMatch 'virtual'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...


PS C:\>
```

<span data-ttu-id="75784-124">Elenco di tutti i tipi di risorse provider il cui spazio dei nomi corrisponde a "calcolo" e il tipo di risorsa corrisponde a "virtuale" e contengono un alias.</span><span class="sxs-lookup"><span data-stu-id="75784-124">Lists all provider resource types whose namespace matches 'compute' and resource type matches 'virtual' and contain an alias.</span></span>
<span data-ttu-id="75784-125">Nota: -NamespaceMatch e -ResourceTypeMatch forniscono corrispondenze esclusive, mentre gli altri sono inclusi.</span><span class="sxs-lookup"><span data-stu-id="75784-125">Note: -NamespaceMatch and -ResourceTypeMatch provide exclusive matches, whereas the others are inclusive.</span></span>

### <span data-ttu-id="75784-126">Esempio 7</span><span class="sxs-lookup"><span data-stu-id="75784-126">Example 7</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -AliasMatch 'virtual'

Namespace            ResourceType                           Aliases
---------            ------------                           -------
Microsoft.Compute    virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Mi...
Microsoft.Compute    virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtu...
Microsoft.Compute    virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineSca...
Microsoft.Compute    virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compu...
Microsoft.DocumentDB databaseAccounts                       {Microsoft.DocumentDB/databaseAccounts/sku.name, Microsoft.DocumentDB/databaseAccounts/v...
Microsoft.HDInsight  clusters                               {Microsoft.HDInsight/clusters/clusterVersion, Microsoft.HDInsight/clusters/osType, Micro...
Microsoft.KeyVault   vaults                                 {Microsoft.KeyVault/vaults/sku.name, Microsoft.KeyVault/vaults/sku.family, Microsoft.Key...
Microsoft.Network    virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNe...
Microsoft.Network    virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGate...
Microsoft.Network    virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network    virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql        servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers...
Microsoft.Storage    storageAccounts                        {Microsoft.Storage/storageAccounts/accountType, Microsoft.Storage/storageAccounts/sku.na...


PS C:\>
```

<span data-ttu-id="75784-127">Elenco di tutti i tipi di risorse provider che contengono un alias corrispondente a 'virtuale'.</span><span class="sxs-lookup"><span data-stu-id="75784-127">Lists all provider resource types that contain an alias matching 'virtual'.</span></span>

### <span data-ttu-id="75784-128">Esempio 8</span><span class="sxs-lookup"><span data-stu-id="75784-128">Example 8</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -AliasMatch 'virtual' -PathMatch 'network'

Namespace            ResourceType                           Aliases
---------            ------------                           -------
Microsoft.Compute    virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Mi...
Microsoft.Compute    virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtu...
Microsoft.Compute    virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineSca...
Microsoft.Compute    virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compu...
Microsoft.DocumentDB databaseAccounts                       {Microsoft.DocumentDB/databaseAccounts/sku.name, Microsoft.DocumentDB/databaseAccounts/v...
Microsoft.HDInsight  clusters                               {Microsoft.HDInsight/clusters/clusterVersion, Microsoft.HDInsight/clusters/osType, Micro...
Microsoft.KeyVault   vaults                                 {Microsoft.KeyVault/vaults/sku.name, Microsoft.KeyVault/vaults/sku.family, Microsoft.Key...
Microsoft.Network    virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNe...
Microsoft.Network    networkInterfaces                      {Microsoft.Network/networkInterfaces/ipconfigurations[*].subnet.id, Microsoft.Network/ne...
Microsoft.Network    networkSecurityGroups                  {Microsoft.Network/networkSecurityGroups/securityRules[*].protocol, Microsoft.Network/ne...
Microsoft.Network    virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGate...
Microsoft.Network    virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network    virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql        servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers...
Microsoft.Storage    storageAccounts                        {Microsoft.Storage/storageAccounts/accountType, Microsoft.Storage/storageAccounts/sku.na...


PS C:\>
```

<span data-ttu-id="75784-129">Elenca tutti i tipi di risorse provider che contengono un alias che corrisponde a 'virtuale' o a un alias con un percorso che corrisponde a 'rete'.</span><span class="sxs-lookup"><span data-stu-id="75784-129">Lists all provider resource types that contain an alias matching 'virtual' or an alias with a path matching 'network'.</span></span>

### <span data-ttu-id="75784-130">Esempio 9</span><span class="sxs-lookup"><span data-stu-id="75784-130">Example 9</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ApiVersionMatch 'alpha'

Namespace          ResourceType        Aliases
---------          ------------        -------
Microsoft.Cache    Redis               {Microsoft.Cache/Redis/sku.name, Microsoft.Cache/Redis/sku.family, Microsoft.Cache/Redis/sku.capacity, Micros...
Microsoft.Cache    Redis/firewallrules {Microsoft.Cache/Redis/firewallrules/startIP, Microsoft.Cache/Redis/firewallrules/endIP}
Microsoft.Security alerts              {Microsoft.Security/alerts/state}
Microsoft.Security pricings            {Microsoft.Security/pricings/pricingTier}
Microsoft.Security complianceResults   {Microsoft.Security/complianceResults/resourceStatus}


PS C:\>
```

<span data-ttu-id="75784-131">Elenco di tutti i tipi di risorse provider con versione api alfa o che contengono un alias con una versione di api alfa.</span><span class="sxs-lookup"><span data-stu-id="75784-131">Lists all provider resource types with alpha api version or containing an alias with an alpha api version.</span></span>

## <span data-ttu-id="75784-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75784-132">PARAMETERS</span></span>

### <span data-ttu-id="75784-133">-AliasMatch</span><span class="sxs-lookup"><span data-stu-id="75784-133">-AliasMatch</span></span>
<span data-ttu-id="75784-134">Include negli elementi di output con alias il cui nome corrisponde a questo valore.</span><span class="sxs-lookup"><span data-stu-id="75784-134">Includes in the output items with aliases whose name matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Alias

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75784-135">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="75784-135">-ApiVersion</span></span>
<span data-ttu-id="75784-136">Se impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="75784-136">When set, indicates the version of the resource provider API to use.</span></span> <span data-ttu-id="75784-137">Se non viene specificato, la versione dell'API viene automaticamente determinata come la più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="75784-137">If not specified, the API version is automatically determined as the latest available.</span></span>


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

### <span data-ttu-id="75784-138">-ApiVersionMatch</span><span class="sxs-lookup"><span data-stu-id="75784-138">-ApiVersionMatch</span></span>
<span data-ttu-id="75784-139">Include negli elementi di output i cui tipi di risorse o alias hanno una versione API corrispondente.</span><span class="sxs-lookup"><span data-stu-id="75784-139">Includes in the output items whose resource types or aliases have a matching api version.</span></span>


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

### <span data-ttu-id="75784-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75784-140">-DefaultProfile</span></span>
<span data-ttu-id="75784-141">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75784-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="75784-142">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="75784-142">-ListAvailable</span></span>
<span data-ttu-id="75784-143">Include negli elementi che corrispondono all'output con e senza alias.</span><span class="sxs-lookup"><span data-stu-id="75784-143">Includes in the output matching items with and without aliases.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: ShowAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75784-144">-LocationMatch</span><span class="sxs-lookup"><span data-stu-id="75784-144">-LocationMatch</span></span>
<span data-ttu-id="75784-145">Include negli elementi di output i cui tipi di risorsa hanno una posizione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="75784-145">Includes in the output items whose resource types have a matching location.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75784-146">-NamespaceMatch</span><span class="sxs-lookup"><span data-stu-id="75784-146">-NamespaceMatch</span></span>
<span data-ttu-id="75784-147">Limita l'output agli elementi il cui spazio dei nomi corrisponde a questo valore.</span><span class="sxs-lookup"><span data-stu-id="75784-147">Limits the output to items whose namespace matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, Namespace

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75784-148">-PathMatch</span><span class="sxs-lookup"><span data-stu-id="75784-148">-PathMatch</span></span>
<span data-ttu-id="75784-149">Include negli elementi di output con alias contenenti un percorso che corrisponde a questo valore.</span><span class="sxs-lookup"><span data-stu-id="75784-149">Includes in the output items with aliases containing a path that matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75784-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="75784-150">-Pre</span></span>
<span data-ttu-id="75784-151">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="75784-151">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>


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

### <span data-ttu-id="75784-152">-ResourceTypeMatch</span><span class="sxs-lookup"><span data-stu-id="75784-152">-ResourceTypeMatch</span></span>
<span data-ttu-id="75784-153">Limita l'output agli elementi il cui tipo di risorsa corrisponde a questo valore.</span><span class="sxs-lookup"><span data-stu-id="75784-153">Limits the output to items whose resource type matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceType, Resource

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75784-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75784-154">CommonParameters</span></span>
<span data-ttu-id="75784-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75784-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75784-156">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="75784-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75784-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="75784-157">INPUTS</span></span>

### <span data-ttu-id="75784-158">Nessuno</span><span class="sxs-lookup"><span data-stu-id="75784-158">None</span></span>

## <span data-ttu-id="75784-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75784-159">OUTPUTS</span></span>

### <span data-ttu-id="75784-160">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.PsResourceProviderAlias</span><span class="sxs-lookup"><span data-stu-id="75784-160">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.PsResourceProviderAlias</span></span>

## <span data-ttu-id="75784-161">NOTE</span><span class="sxs-lookup"><span data-stu-id="75784-161">NOTES</span></span>

* <span data-ttu-id="75784-162">Per espandere gli alias o qualsiasi altra proprietà, eseguire il piping dell'output su `select -ExpandProperty <property>` .</span><span class="sxs-lookup"><span data-stu-id="75784-162">To expand the Aliases or any other property, pipe the output to `select -ExpandProperty <property>`.</span></span> <span data-ttu-id="75784-163">Per esempio: `Get-AzPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span><span class="sxs-lookup"><span data-stu-id="75784-163">For example: `Get-AzPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span></span>

* <span data-ttu-id="75784-164">Altre proprietà sono disponibili nell'output e possono essere visualizzate mediante l'esecuzione dell'piping dell'output su `Format-List` .</span><span class="sxs-lookup"><span data-stu-id="75784-164">Additional properties are available in the output and can be displayed by piping the output to `Format-List`.</span></span> <span data-ttu-id="75784-165">Per esempio: `Get-AzPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span><span class="sxs-lookup"><span data-stu-id="75784-165">For example: `Get-AzPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span></span>

## <span data-ttu-id="75784-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75784-166">RELATED LINKS</span></span>

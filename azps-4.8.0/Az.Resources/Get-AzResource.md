---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
ms.openlocfilehash: 2926aa351e7e9f1f9251c5a6e6a2292b27ef93b0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398190"
---
# <span data-ttu-id="42515-101">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="42515-101">Get-AzResource</span></span>

## <span data-ttu-id="42515-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42515-102">SYNOPSIS</span></span>

<span data-ttu-id="42515-103">Ottiene risorse.</span><span class="sxs-lookup"><span data-stu-id="42515-103">Gets resources.</span></span>

## <span data-ttu-id="42515-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42515-104">SYNTAX</span></span>

### <span data-ttu-id="42515-105">ByTagNameValueParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="42515-105">ByTagNameValueParameterSet (Default)</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 [-TagName <String>] [-TagValue <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42515-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="42515-106">ByResourceId</span></span>
```
Get-AzResource -ResourceId <String> [-ODataQuery <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42515-107">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42515-107">ByTagObjectParameterSet</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 -Tag <Hashtable> [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42515-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="42515-108">DESCRIPTION</span></span>

<span data-ttu-id="42515-109">Il cmdlet **Get-AzResource** ottiene risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="42515-109">The **Get-AzResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="42515-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42515-110">EXAMPLES</span></span>

### <span data-ttu-id="42515-111">Esempio 1: Ottenere tutte le risorse nella sottoscrizione corrente</span><span class="sxs-lookup"><span data-stu-id="42515-111">Example 1: Get all resources in the current subscription</span></span>

```
PS C:\> Get-AzResource | ft

Name    ResourceGroupName  ResourceType                            Location
----    -----------------  ------------                            --------
testVM  testRG             Microsoft.Compute/virtualMachines       westus
disk    testRG             Microsoft.Compute/disks                 westus
nic     testRG             Microsoft.Network/networkInterfaces     westus
nsg     testRG             Microsoft.Network/networkSecurityGroups westus
ip      testRG             Microsoft.Network/publicIPAddresses     westus
vnet    testRG             Microsoft.Network/virtualNetworks       westus
testKV  otherRG            Microsoft.KeyVault/vaults               eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts       eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines       eastus
```

<span data-ttu-id="42515-112">Questo comando recupera tutte le risorse nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="42515-112">This command gets all of the resources in the current subscription.</span></span>

### <span data-ttu-id="42515-113">Esempio 2: Recuperare tutte le risorse in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="42515-113">Example 2: Get all resources in a resource group</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName testRG | ft

Name   ResourceGroupName ResourceType                            Location
----   ----------------- ------------                            --------
testVM testRG            Microsoft.Compute/virtualMachines       westus
disk   testRG            Microsoft.Compute/disks                 westus
nic    testRG            Microsoft.Network/networkInterfaces     westus
nsg    testRG            Microsoft.Network/networkSecurityGroups westus
ip     testRG            Microsoft.Network/publicIPAddresses     westus
vnet   testRG            Microsoft.Network/virtualNetworks       westus
```

<span data-ttu-id="42515-114">Questo comando recupera tutte le risorse nel gruppo di risorse "testRG".</span><span class="sxs-lookup"><span data-stu-id="42515-114">This command gets all of the resources in the resource group "testRG".</span></span>

### <span data-ttu-id="42515-115">Esempio 3: Ottenere tutte le risorse il cui gruppo di risorse corrisponde al carattere jolly fornito</span><span class="sxs-lookup"><span data-stu-id="42515-115">Example 3: Get all resources whose resource group matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName other* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="42515-116">Questo comando recupera tutte le risorse il cui gruppo di risorse appartiene a un altro.</span><span class="sxs-lookup"><span data-stu-id="42515-116">This command gets all of the resources whose resource group they belong in beings with "other".</span></span>

### <span data-ttu-id="42515-117">Esempio 4: Ottenere tutte le risorse con un nome assegnato</span><span class="sxs-lookup"><span data-stu-id="42515-117">Example 4: Get all resources with a given name</span></span>

```
PS C:\> Get-AzResource -Name testVM | fl

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
Tags              :
                    Name    Value
                    ======  ========
                    Dept    IT
                    Year    2002
                    Status  Approved
```

<span data-ttu-id="42515-118">Questo comando recupera tutte le risorse il cui nome della risorsa è "testVM".</span><span class="sxs-lookup"><span data-stu-id="42515-118">This command gets all of the resources whose resource name is "testVM".</span></span>

### <span data-ttu-id="42515-119">Esempio 5: Ottenere tutte le risorse il cui nome corrisponde al carattere jolly fornito</span><span class="sxs-lookup"><span data-stu-id="42515-119">Example 5: Get all resources whose name matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -Name test* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="42515-120">Questo comando recupera tutte le risorse il cui nome di risorsa inizia con "test".</span><span class="sxs-lookup"><span data-stu-id="42515-120">This command gets all of the resources whose resource name begins with "test".</span></span>

### <span data-ttu-id="42515-121">Esempio 6: Recuperare tutte le risorse di un determinato tipo di risorsa</span><span class="sxs-lookup"><span data-stu-id="42515-121">Example 6: Get all resources of a given resource type</span></span>

```
PS C:\> Get-AzResource -ResourceType Microsoft.Compute/virtualMachines | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="42515-122">Questo comando recupera tutte le risorse nelle sottoscrizioni correnti che sono macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="42515-122">This command gets all of the resources in the current subscriptions that are virtual machines.</span></span>

### <span data-ttu-id="42515-123">Esempio 7: Ottenere una risorsa in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="42515-123">Example 7: Get a resource by resource id</span></span>

```
PS C:\> Get-AzResource -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
Tags              :
                    Name    Value
                    ======  ========
                    Dept    IT
                    Year    2002
                    Status  Approved
```

<span data-ttu-id="42515-124">Questo comando recupera la risorsa con l'ID risorsa fornito, ovvero una macchina virtuale denominata "testVM" nel gruppo di risorse "testRG".</span><span class="sxs-lookup"><span data-stu-id="42515-124">This command gets the resource with the provided resource id, which is a virtual machine called "testVM" in the resource group "testRG".</span></span>

## <span data-ttu-id="42515-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42515-125">PARAMETERS</span></span>

### <span data-ttu-id="42515-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="42515-126">-ApiVersion</span></span>

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

### <span data-ttu-id="42515-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42515-127">-DefaultProfile</span></span>
<span data-ttu-id="42515-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="42515-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42515-129">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="42515-129">-ExpandProperties</span></span>
<span data-ttu-id="42515-130">Se specificato, espande le proprietà della risorsa.</span><span class="sxs-lookup"><span data-stu-id="42515-130">When specified, expands the properties of the resource.</span></span>

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

### <span data-ttu-id="42515-131">-Name</span><span class="sxs-lookup"><span data-stu-id="42515-131">-Name</span></span>
<span data-ttu-id="42515-132">Nome delle risorse da recuperare.</span><span class="sxs-lookup"><span data-stu-id="42515-132">The name of the resource(s) to be retrieved.</span></span> <span data-ttu-id="42515-133">Questo parametro supporta i caratteri jolly all'inizio e/o alla fine della stringa.</span><span class="sxs-lookup"><span data-stu-id="42515-133">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="42515-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="42515-134">-ODataQuery</span></span>

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

### <span data-ttu-id="42515-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="42515-135">-Pre</span></span>

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

### <span data-ttu-id="42515-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42515-136">-ResourceGroupName</span></span>
<span data-ttu-id="42515-137">Gruppo di risorse a cui appartengono le risorse recuperate.</span><span class="sxs-lookup"><span data-stu-id="42515-137">The resource group the resource(s) that is retrieved belongs in.</span></span> <span data-ttu-id="42515-138">Questo parametro supporta i caratteri jolly all'inizio e/o alla fine della stringa.</span><span class="sxs-lookup"><span data-stu-id="42515-138">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="42515-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42515-139">-ResourceId</span></span>
<span data-ttu-id="42515-140">Specifica l'ID risorsa completo, come nell'esempio seguente `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span><span class="sxs-lookup"><span data-stu-id="42515-140">Specifies the fully qualified resource ID, as in the following example `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42515-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="42515-141">-ResourceType</span></span>
<span data-ttu-id="42515-142">Tipo di risorsa delle risorse da recuperare.</span><span class="sxs-lookup"><span data-stu-id="42515-142">The resource type of the resource(s) to be retrieved.</span></span> <span data-ttu-id="42515-143">Ad esempio, Microsoft.Compute/virtualMachines</span><span class="sxs-lookup"><span data-stu-id="42515-143">For example, Microsoft.Compute/virtualMachines</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42515-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="42515-144">-Tag</span></span>

<span data-ttu-id="42515-145">Recupera le risorse con il tag di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="42515-145">Gets resources that have the specified Azure tag.</span></span> <span data-ttu-id="42515-146">Immettere una tabella hash con una chiave Nome o le chiavi Nome e Valore.</span><span class="sxs-lookup"><span data-stu-id="42515-146">Enter a hash table with a Name key or Name and Value keys.</span></span> <span data-ttu-id="42515-147">I caratteri jolly non sono supportati. Un "tag" è una coppia nome-valore che è possibile applicare a risorse e gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="42515-147">Wildcard characters are not supported.A "tag" is a name-value pair that you can apply to resources and resource groups.</span></span> <span data-ttu-id="42515-148">Usare i contrassegni per categorizzare le risorse, ad esempio per reparto o centro di costo, oppure per tenere traccia di note o commenti sulle risorse.</span><span class="sxs-lookup"><span data-stu-id="42515-148">Use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span> <span data-ttu-id="42515-149">Per aggiungere un tag a una risorsa, usare il parametro Tag dei cmdlet New-AzResource o Set-AzResource risorsa.</span><span class="sxs-lookup"><span data-stu-id="42515-149">To add a tag to a resource, use the Tag parameter of the New-AzResource or Set-AzResource cmdlets.</span></span> <span data-ttu-id="42515-150">Per creare un tag predefinito, usare il cmdlet New-AzTag tag.</span><span class="sxs-lookup"><span data-stu-id="42515-150">To create a predefined tag, use the New-AzTag cmdlet.</span></span> <span data-ttu-id="42515-151">Per assistenza con le tabelle hash in Windows PowerShell, eseguire 'Get-Help about_Hashtables'.</span><span class="sxs-lookup"><span data-stu-id="42515-151">For help with hash tables in Windows PowerShell, run 'Get-Help about_Hashtables'.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42515-152">-TagName</span><span class="sxs-lookup"><span data-stu-id="42515-152">-TagName</span></span>
<span data-ttu-id="42515-153">Chiave nel tag delle risorse da recuperare.</span><span class="sxs-lookup"><span data-stu-id="42515-153">The key in the tag of the resource(s) to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42515-154">-TagValue</span><span class="sxs-lookup"><span data-stu-id="42515-154">-TagValue</span></span>
<span data-ttu-id="42515-155">Valore nel tag delle risorse da recuperare.</span><span class="sxs-lookup"><span data-stu-id="42515-155">The value in the tag of the resource(s) to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42515-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42515-156">CommonParameters</span></span>
<span data-ttu-id="42515-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42515-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42515-158">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="42515-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42515-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="42515-159">INPUTS</span></span>

### <span data-ttu-id="42515-160">System.String</span><span class="sxs-lookup"><span data-stu-id="42515-160">System.String</span></span>

## <span data-ttu-id="42515-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42515-161">OUTPUTS</span></span>

### <span data-ttu-id="42515-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span><span class="sxs-lookup"><span data-stu-id="42515-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

## <span data-ttu-id="42515-163">NOTE</span><span class="sxs-lookup"><span data-stu-id="42515-163">NOTES</span></span>

## <span data-ttu-id="42515-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42515-164">RELATED LINKS</span></span>


[<span data-ttu-id="42515-165">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="42515-165">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="42515-166">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="42515-166">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="42515-167">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="42515-167">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="42515-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="42515-168">Set-AzResource</span></span>](./Set-AzResource.md)

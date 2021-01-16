---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
ms.openlocfilehash: 738b2258f327cbe00b3162d39aaeebd647d1a2e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330232"
---
# <span data-ttu-id="8e7c7-101">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="8e7c7-101">Get-AzResource</span></span>

## <span data-ttu-id="8e7c7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8e7c7-102">SYNOPSIS</span></span>

<span data-ttu-id="8e7c7-103">Ottiene le risorse.</span><span class="sxs-lookup"><span data-stu-id="8e7c7-103">Gets resources.</span></span>

## <span data-ttu-id="8e7c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e7c7-104">SYNTAX</span></span>

### <span data-ttu-id="8e7c7-105">ByTagNameValueParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8e7c7-105">ByTagNameValueParameterSet (Default)</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 [-TagName <String>] [-TagValue <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e7c7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e7c7-106">ByResourceId</span></span>
```
Get-AzResource -ResourceId <String> [-ODataQuery <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e7c7-107">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e7c7-107">ByTagObjectParameterSet</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 -Tag <Hashtable> [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e7c7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e7c7-108">DESCRIPTION</span></span>

<span data-ttu-id="8e7c7-109">Il cmdlet **Get-AzResource** ottiene le risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="8e7c7-109">The **Get-AzResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="8e7c7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e7c7-110">EXAMPLES</span></span>

### <span data-ttu-id="8e7c7-111">Esempio 1: ottenere tutte le risorse nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="8e7c7-111">Example 1: Get all resources in the current subscription</span></span>

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

<span data-ttu-id="8e7c7-112">Questo comando consente di ottenere tutte le risorse dell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="8e7c7-112">This command gets all of the resources in the current subscription.</span></span>

### <span data-ttu-id="8e7c7-113">Esempio 2: ottenere tutte le risorse in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8e7c7-113">Example 2: Get all resources in a resource group</span></span>

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

<span data-ttu-id="8e7c7-114">Questo comando consente di ottenere tutte le risorse del gruppo di risorse "testRG".</span><span class="sxs-lookup"><span data-stu-id="8e7c7-114">This command gets all of the resources in the resource group "testRG".</span></span>

### <span data-ttu-id="8e7c7-115">Esempio 3: ottenere tutte le risorse il cui gruppo di risorse corrisponde al carattere jolly specificato</span><span class="sxs-lookup"><span data-stu-id="8e7c7-115">Example 3: Get all resources whose resource group matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName other* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="8e7c7-116">Questo comando consente di ottenere tutte le risorse il cui gruppo di risorse appartiene agli esseri con "altro".</span><span class="sxs-lookup"><span data-stu-id="8e7c7-116">This command gets all of the resources whose resource group they belong in beings with "other".</span></span>

### <span data-ttu-id="8e7c7-117">Esempio 4: ottenere tutte le risorse con un nome specifico</span><span class="sxs-lookup"><span data-stu-id="8e7c7-117">Example 4: Get all resources with a given name</span></span>

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

<span data-ttu-id="8e7c7-118">Questo comando consente di ottenere tutte le risorse il cui nome di risorsa è "testVM".</span><span class="sxs-lookup"><span data-stu-id="8e7c7-118">This command gets all of the resources whose resource name is "testVM".</span></span>

### <span data-ttu-id="8e7c7-119">Esempio 5: ottenere tutte le risorse il cui nome corrisponde al carattere jolly specificato</span><span class="sxs-lookup"><span data-stu-id="8e7c7-119">Example 5: Get all resources whose name matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -Name test* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="8e7c7-120">Questo comando consente di ottenere tutte le risorse il cui nome di risorsa inizia con "test".</span><span class="sxs-lookup"><span data-stu-id="8e7c7-120">This command gets all of the resources whose resource name begins with "test".</span></span>

### <span data-ttu-id="8e7c7-121">Esempio 6: ottenere tutte le risorse di un tipo di risorsa specifico</span><span class="sxs-lookup"><span data-stu-id="8e7c7-121">Example 6: Get all resources of a given resource type</span></span>

```
PS C:\> Get-AzResource -ResourceType Microsoft.Compute/virtualMachines | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="8e7c7-122">Questo comando consente di ottenere tutte le risorse degli abbonamenti correnti che sono macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="8e7c7-122">This command gets all of the resources in the current subscriptions that are virtual machines.</span></span>

### <span data-ttu-id="8e7c7-123">Esempio 7: ottenere una risorsa per ID risorsa</span><span class="sxs-lookup"><span data-stu-id="8e7c7-123">Example 7: Get a resource by resource id</span></span>

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

<span data-ttu-id="8e7c7-124">Questo comando consente di ottenere la risorsa con l'ID risorsa specificata, ovvero una macchina virtuale denominata "testVM" nel gruppo di risorse "testRG".</span><span class="sxs-lookup"><span data-stu-id="8e7c7-124">This command gets the resource with the provided resource id, which is a virtual machine called "testVM" in the resource group "testRG".</span></span>

## <span data-ttu-id="8e7c7-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8e7c7-125">PARAMETERS</span></span>

### <span data-ttu-id="8e7c7-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8e7c7-126">-ApiVersion</span></span>

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

### <span data-ttu-id="8e7c7-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e7c7-127">-DefaultProfile</span></span>
<span data-ttu-id="8e7c7-128">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8e7c7-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e7c7-129">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="8e7c7-129">-ExpandProperties</span></span>
<span data-ttu-id="8e7c7-130">Se specificato, espande le proprietà della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8e7c7-130">When specified, expands the properties of the resource.</span></span>

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

### <span data-ttu-id="8e7c7-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e7c7-131">-Name</span></span>
<span data-ttu-id="8e7c7-132">Il nome della risorsa o delle risorse da recuperare.</span><span class="sxs-lookup"><span data-stu-id="8e7c7-132">The name of the resource(s) to be retrieved.</span></span> <span data-ttu-id="8e7c7-133">Questo parametro supporta i caratteri jolly all'inizio e/o alla fine della stringa.</span><span class="sxs-lookup"><span data-stu-id="8e7c7-133">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

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

### <span data-ttu-id="8e7c7-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="8e7c7-134">-ODataQuery</span></span>

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

### <span data-ttu-id="8e7c7-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="8e7c7-135">-Pre</span></span>

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

### <span data-ttu-id="8e7c7-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e7c7-136">-ResourceGroupName</span></span>
<span data-ttu-id="8e7c7-137">Gruppo risorse a cui appartiene la risorsa recuperata.</span><span class="sxs-lookup"><span data-stu-id="8e7c7-137">The resource group the resource(s) that is retrieved belongs in.</span></span> <span data-ttu-id="8e7c7-138">Questo parametro supporta i caratteri jolly all'inizio e/o alla fine della stringa.</span><span class="sxs-lookup"><span data-stu-id="8e7c7-138">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

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

### <span data-ttu-id="8e7c7-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e7c7-139">-ResourceId</span></span>
<span data-ttu-id="8e7c7-140">Specifica l'ID risorsa completo, come nell'esempio seguente `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span><span class="sxs-lookup"><span data-stu-id="8e7c7-140">Specifies the fully qualified resource ID, as in the following example `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span></span>

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

### <span data-ttu-id="8e7c7-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8e7c7-141">-ResourceType</span></span>
<span data-ttu-id="8e7c7-142">Tipo di risorsa per la risorsa o le risorse da recuperare.</span><span class="sxs-lookup"><span data-stu-id="8e7c7-142">The resource type of the resource(s) to be retrieved.</span></span> <span data-ttu-id="8e7c7-143">Ad esempio, Microsoft. Compute/virtualMachines</span><span class="sxs-lookup"><span data-stu-id="8e7c7-143">For example, Microsoft.Compute/virtualMachines</span></span>

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

### <span data-ttu-id="8e7c7-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="8e7c7-144">-Tag</span></span>

<span data-ttu-id="8e7c7-145">Ottiene le risorse con il tag Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="8e7c7-145">Gets resources that have the specified Azure tag.</span></span> <span data-ttu-id="8e7c7-146">Immettere una tabella hash con una chiave nome o un nome e chiavi di valore.</span><span class="sxs-lookup"><span data-stu-id="8e7c7-146">Enter a hash table with a Name key or Name and Value keys.</span></span> <span data-ttu-id="8e7c7-147">I caratteri jolly non sono supportati. Un "tag" è una coppia nome-valore che puoi applicare alle risorse e ai gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="8e7c7-147">Wildcard characters are not supported.A "tag" is a name-value pair that you can apply to resources and resource groups.</span></span> <span data-ttu-id="8e7c7-148">Usare i contrassegni per suddividere in categorie le risorse, ad esempio per reparto o centro costo, oppure per tenere traccia di note o commenti sulle risorse.</span><span class="sxs-lookup"><span data-stu-id="8e7c7-148">Use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span> <span data-ttu-id="8e7c7-149">Per aggiungere un contrassegno a una risorsa, usare il parametro tag dei cmdlet New-AzResource o Set-AzResource.</span><span class="sxs-lookup"><span data-stu-id="8e7c7-149">To add a tag to a resource, use the Tag parameter of the New-AzResource or Set-AzResource cmdlets.</span></span> <span data-ttu-id="8e7c7-150">Per creare un tag predefinito, usare il cmdlet New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="8e7c7-150">To create a predefined tag, use the New-AzTag cmdlet.</span></span> <span data-ttu-id="8e7c7-151">Per informazioni sulle tabelle hash in Windows PowerShell, eseguire ' Get-Help about_Hashtables '.</span><span class="sxs-lookup"><span data-stu-id="8e7c7-151">For help with hash tables in Windows PowerShell, run 'Get-Help about_Hashtables'.</span></span>

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

### <span data-ttu-id="8e7c7-152">-TagName</span><span class="sxs-lookup"><span data-stu-id="8e7c7-152">-TagName</span></span>
<span data-ttu-id="8e7c7-153">La chiave nel contrassegno della risorsa o delle risorse da recuperare.</span><span class="sxs-lookup"><span data-stu-id="8e7c7-153">The key in the tag of the resource(s) to be retrieved.</span></span>

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

### <span data-ttu-id="8e7c7-154">-TagValue</span><span class="sxs-lookup"><span data-stu-id="8e7c7-154">-TagValue</span></span>
<span data-ttu-id="8e7c7-155">Il valore nel contrassegno della risorsa o delle risorse da recuperare.</span><span class="sxs-lookup"><span data-stu-id="8e7c7-155">The value in the tag of the resource(s) to be retrieved.</span></span>

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

### <span data-ttu-id="8e7c7-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e7c7-156">CommonParameters</span></span>
<span data-ttu-id="8e7c7-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e7c7-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e7c7-158">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e7c7-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e7c7-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8e7c7-159">INPUTS</span></span>

### <span data-ttu-id="8e7c7-160">System. String</span><span class="sxs-lookup"><span data-stu-id="8e7c7-160">System.String</span></span>

## <span data-ttu-id="8e7c7-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e7c7-161">OUTPUTS</span></span>

### <span data-ttu-id="8e7c7-162">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResource</span><span class="sxs-lookup"><span data-stu-id="8e7c7-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

## <span data-ttu-id="8e7c7-163">Note</span><span class="sxs-lookup"><span data-stu-id="8e7c7-163">NOTES</span></span>

## <span data-ttu-id="8e7c7-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e7c7-164">RELATED LINKS</span></span>

[<span data-ttu-id="8e7c7-165">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="8e7c7-165">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="8e7c7-166">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="8e7c7-166">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="8e7c7-167">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="8e7c7-167">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="8e7c7-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="8e7c7-168">Set-AzResource</span></span>](./Set-AzResource.md)
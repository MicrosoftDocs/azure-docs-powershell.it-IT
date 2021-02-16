---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 9b3991a24430afa74853f742bffa12b772dbeaf2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202769"
---
# <span data-ttu-id="d3c46-101">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="d3c46-101">New-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="d3c46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3c46-102">SYNOPSIS</span></span>
<span data-ttu-id="d3c46-103">Creare una risorsa Appliance virtuale di rete.</span><span class="sxs-lookup"><span data-stu-id="d3c46-103">Create a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="d3c46-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3c46-104">SYNTAX</span></span>

### <span data-ttu-id="d3c46-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d3c46-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> -Location <String>
 -VirtualHubId <String> -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32>
 [-Identity <PSManagedServiceIdentity>] [-BootStrapConfigurationBlob <String[]>]
 [-CloudInitConfigurationBlob <String[]>] [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3c46-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3c46-106">ResourceIdParameterSet</span></span>
```
New-AzNetworkVirtualAppliance -ResourceId <String> -Location <String> -VirtualHubId <String>
 -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32> [-Identity <PSManagedServiceIdentity>]
 [-BootStrapConfigurationBlob <String[]>] [-CloudInitConfigurationBlob <String[]>]
 [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3c46-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d3c46-107">DESCRIPTION</span></span>
<span data-ttu-id="d3c46-108">Il New-AzNetworkVirtualAppliance crea una risorsa Appliance virtuale di rete in Azure.</span><span class="sxs-lookup"><span data-stu-id="d3c46-108">The New-AzNetworkVirtualAppliance command creates a Network Virtual Appliance resource in Azure.</span></span>

## <span data-ttu-id="d3c46-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3c46-109">EXAMPLES</span></span>

### <span data-ttu-id="d3c46-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d3c46-110">Example 1</span></span>
```powershell
PS C:\> $sku=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
PS C:\> $hub=Get-AzVirtualHub -ResourceGroupName testrg -Name hub
PS C:\> $nva=New-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -Location eastus2 -VirtualApplianceAsn 1270 -VirtualHubId $hub.Id -Sku $sku -CloudInitConfiguration "echo Hello World!"

```

<span data-ttu-id="d3c46-111">Crea una nuova risorsa Appliance virtuale di rete nel gruppo di risorse: testrg.</span><span class="sxs-lookup"><span data-stu-id="d3c46-111">Creates a new Network Virtual Appliance resource in resource group: testrg.</span></span>

## <span data-ttu-id="d3c46-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3c46-112">PARAMETERS</span></span>

### <span data-ttu-id="d3c46-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3c46-113">-AsJob</span></span>
<span data-ttu-id="d3c46-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d3c46-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3c46-115">-BootStrapConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="d3c46-115">-BootStrapConfigurationBlob</span></span>
<span data-ttu-id="d3c46-116">URL BLOB della configurazione Bootstrap.</span><span class="sxs-lookup"><span data-stu-id="d3c46-116">The Bootstrap configuration blob URL.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c46-117">-CloudInitConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3c46-117">-CloudInitConfiguration</span></span>
<span data-ttu-id="d3c46-118">La configurazione Cloudinit come testo normale.</span><span class="sxs-lookup"><span data-stu-id="d3c46-118">The Cloudinit configuration as plain text.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c46-119">-CloudInitConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="d3c46-119">-CloudInitConfigurationBlob</span></span>
<span data-ttu-id="d3c46-120">URL di archiviazione BLOB di configurazione Cloudinit.</span><span class="sxs-lookup"><span data-stu-id="d3c46-120">The Cloudinit configuration blob storage URL.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c46-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3c46-121">-DefaultProfile</span></span>
<span data-ttu-id="d3c46-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3c46-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3c46-123">-Force</span><span class="sxs-lookup"><span data-stu-id="d3c46-123">-Force</span></span>
<span data-ttu-id="d3c46-124">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="d3c46-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d3c46-125">-Identity</span><span class="sxs-lookup"><span data-stu-id="d3c46-125">-Identity</span></span>
<span data-ttu-id="d3c46-126">Identità gestite.</span><span class="sxs-lookup"><span data-stu-id="d3c46-126">The Managed identity.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c46-127">-Location</span><span class="sxs-lookup"><span data-stu-id="d3c46-127">-Location</span></span>
<span data-ttu-id="d3c46-128">Posizione dell'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="d3c46-128">The public IP address location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c46-129">-Name</span><span class="sxs-lookup"><span data-stu-id="d3c46-129">-Name</span></span>
<span data-ttu-id="d3c46-130">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d3c46-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c46-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3c46-131">-ResourceGroupName</span></span>
<span data-ttu-id="d3c46-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d3c46-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c46-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3c46-133">-ResourceId</span></span>
<span data-ttu-id="d3c46-134">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d3c46-134">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c46-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="d3c46-135">-Sku</span></span>
<span data-ttu-id="d3c46-136">SKU dell'appliance virtuale.</span><span class="sxs-lookup"><span data-stu-id="d3c46-136">The Sku of the Virtual Appliance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c46-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="d3c46-137">-Tag</span></span>
<span data-ttu-id="d3c46-138">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="d3c46-138">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c46-139">-VirtualApplianceAsn</span><span class="sxs-lookup"><span data-stu-id="d3c46-139">-VirtualApplianceAsn</span></span>
<span data-ttu-id="d3c46-140">Numero ASN dell'appliance virtuale.</span><span class="sxs-lookup"><span data-stu-id="d3c46-140">The ASN number of the Virtual Appliance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c46-141">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="d3c46-141">-VirtualHubId</span></span>
<span data-ttu-id="d3c46-142">ID risorsa dell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="d3c46-142">The Resource Id of the Virtual Hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3c46-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3c46-143">-Confirm</span></span>
<span data-ttu-id="d3c46-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3c46-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3c46-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3c46-145">-WhatIf</span></span>
<span data-ttu-id="d3c46-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3c46-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3c46-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3c46-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3c46-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3c46-148">CommonParameters</span></span>
<span data-ttu-id="d3c46-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3c46-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3c46-150">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d3c46-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3c46-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="d3c46-151">INPUTS</span></span>

### <span data-ttu-id="d3c46-152">System.String</span><span class="sxs-lookup"><span data-stu-id="d3c46-152">System.String</span></span>

### <span data-ttu-id="d3c46-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="d3c46-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

### <span data-ttu-id="d3c46-154">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d3c46-154">System.Int32</span></span>

### <span data-ttu-id="d3c46-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="d3c46-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

### <span data-ttu-id="d3c46-156">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d3c46-156">System.String[]</span></span>

### <span data-ttu-id="d3c46-157">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="d3c46-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d3c46-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3c46-158">OUTPUTS</span></span>

### <span data-ttu-id="d3c46-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="d3c46-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="d3c46-160">NOTE</span><span class="sxs-lookup"><span data-stu-id="d3c46-160">NOTES</span></span>

## <span data-ttu-id="d3c46-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3c46-161">RELATED LINKS</span></span>

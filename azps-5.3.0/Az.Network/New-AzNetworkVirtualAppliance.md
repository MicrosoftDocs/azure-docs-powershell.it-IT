---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 9b3991a24430afa74853f742bffa12b772dbeaf2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474525"
---
# <span data-ttu-id="734ac-101">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="734ac-101">New-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="734ac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="734ac-102">SYNOPSIS</span></span>
<span data-ttu-id="734ac-103">Creare una risorsa di Virtual Appliance di rete.</span><span class="sxs-lookup"><span data-stu-id="734ac-103">Create a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="734ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="734ac-104">SYNTAX</span></span>

### <span data-ttu-id="734ac-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="734ac-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> -Location <String>
 -VirtualHubId <String> -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32>
 [-Identity <PSManagedServiceIdentity>] [-BootStrapConfigurationBlob <String[]>]
 [-CloudInitConfigurationBlob <String[]>] [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="734ac-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="734ac-106">ResourceIdParameterSet</span></span>
```
New-AzNetworkVirtualAppliance -ResourceId <String> -Location <String> -VirtualHubId <String>
 -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32> [-Identity <PSManagedServiceIdentity>]
 [-BootStrapConfigurationBlob <String[]>] [-CloudInitConfigurationBlob <String[]>]
 [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="734ac-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="734ac-107">DESCRIPTION</span></span>
<span data-ttu-id="734ac-108">Il comando New-AzNetworkVirtualAppliance crea una risorsa di Virtual Appliance di rete in Azure.</span><span class="sxs-lookup"><span data-stu-id="734ac-108">The New-AzNetworkVirtualAppliance command creates a Network Virtual Appliance resource in Azure.</span></span>

## <span data-ttu-id="734ac-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="734ac-109">EXAMPLES</span></span>

### <span data-ttu-id="734ac-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="734ac-110">Example 1</span></span>
```powershell
PS C:\> $sku=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
PS C:\> $hub=Get-AzVirtualHub -ResourceGroupName testrg -Name hub
PS C:\> $nva=New-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -Location eastus2 -VirtualApplianceAsn 1270 -VirtualHubId $hub.Id -Sku $sku -CloudInitConfiguration "echo Hello World!"

```

<span data-ttu-id="734ac-111">Crea una nuova risorsa di Virtual Appliance di rete in un gruppo di risorse: testrg.</span><span class="sxs-lookup"><span data-stu-id="734ac-111">Creates a new Network Virtual Appliance resource in resource group: testrg.</span></span>

## <span data-ttu-id="734ac-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="734ac-112">PARAMETERS</span></span>

### <span data-ttu-id="734ac-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="734ac-113">-AsJob</span></span>
<span data-ttu-id="734ac-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="734ac-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="734ac-115">-BootStrapConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="734ac-115">-BootStrapConfigurationBlob</span></span>
<span data-ttu-id="734ac-116">URL BLOB della configurazione bootstrap.</span><span class="sxs-lookup"><span data-stu-id="734ac-116">The Bootstrap configuration blob URL.</span></span>

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

### <span data-ttu-id="734ac-117">-CloudInitConfiguration</span><span class="sxs-lookup"><span data-stu-id="734ac-117">-CloudInitConfiguration</span></span>
<span data-ttu-id="734ac-118">La configurazione di Cloudinit come testo normale.</span><span class="sxs-lookup"><span data-stu-id="734ac-118">The Cloudinit configuration as plain text.</span></span>

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

### <span data-ttu-id="734ac-119">-CloudInitConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="734ac-119">-CloudInitConfigurationBlob</span></span>
<span data-ttu-id="734ac-120">URL di archiviazione BLOB di configurazione Cloudinit.</span><span class="sxs-lookup"><span data-stu-id="734ac-120">The Cloudinit configuration blob storage URL.</span></span>

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

### <span data-ttu-id="734ac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="734ac-121">-DefaultProfile</span></span>
<span data-ttu-id="734ac-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="734ac-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="734ac-123">-Force</span><span class="sxs-lookup"><span data-stu-id="734ac-123">-Force</span></span>
<span data-ttu-id="734ac-124">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="734ac-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="734ac-125">-Identità</span><span class="sxs-lookup"><span data-stu-id="734ac-125">-Identity</span></span>
<span data-ttu-id="734ac-126">Identità gestita.</span><span class="sxs-lookup"><span data-stu-id="734ac-126">The Managed identity.</span></span>

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

### <span data-ttu-id="734ac-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="734ac-127">-Location</span></span>
<span data-ttu-id="734ac-128">Posizione dell'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="734ac-128">The public IP address location.</span></span>

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

### <span data-ttu-id="734ac-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="734ac-129">-Name</span></span>
<span data-ttu-id="734ac-130">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="734ac-130">The resource name.</span></span>

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

### <span data-ttu-id="734ac-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="734ac-131">-ResourceGroupName</span></span>
<span data-ttu-id="734ac-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="734ac-132">The resource group name.</span></span>

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

### <span data-ttu-id="734ac-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="734ac-133">-ResourceId</span></span>
<span data-ttu-id="734ac-134">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="734ac-134">The resource Id.</span></span>

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

### <span data-ttu-id="734ac-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="734ac-135">-Sku</span></span>
<span data-ttu-id="734ac-136">SKU dell'appliance virtuale.</span><span class="sxs-lookup"><span data-stu-id="734ac-136">The Sku of the Virtual Appliance.</span></span>

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

### <span data-ttu-id="734ac-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="734ac-137">-Tag</span></span>
<span data-ttu-id="734ac-138">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="734ac-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="734ac-139">-VirtualApplianceAsn</span><span class="sxs-lookup"><span data-stu-id="734ac-139">-VirtualApplianceAsn</span></span>
<span data-ttu-id="734ac-140">Il numero ASN dell'appliance virtuale.</span><span class="sxs-lookup"><span data-stu-id="734ac-140">The ASN number of the Virtual Appliance.</span></span>

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

### <span data-ttu-id="734ac-141">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="734ac-141">-VirtualHubId</span></span>
<span data-ttu-id="734ac-142">ID risorsa dell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="734ac-142">The Resource Id of the Virtual Hub.</span></span>

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

### <span data-ttu-id="734ac-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="734ac-143">-Confirm</span></span>
<span data-ttu-id="734ac-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="734ac-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="734ac-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="734ac-145">-WhatIf</span></span>
<span data-ttu-id="734ac-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="734ac-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="734ac-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="734ac-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="734ac-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="734ac-148">CommonParameters</span></span>
<span data-ttu-id="734ac-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="734ac-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="734ac-150">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="734ac-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="734ac-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="734ac-151">INPUTS</span></span>

### <span data-ttu-id="734ac-152">System. String</span><span class="sxs-lookup"><span data-stu-id="734ac-152">System.String</span></span>

### <span data-ttu-id="734ac-153">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="734ac-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

### <span data-ttu-id="734ac-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="734ac-154">System.Int32</span></span>

### <span data-ttu-id="734ac-155">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="734ac-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

### <span data-ttu-id="734ac-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="734ac-156">System.String[]</span></span>

### <span data-ttu-id="734ac-157">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="734ac-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="734ac-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="734ac-158">OUTPUTS</span></span>

### <span data-ttu-id="734ac-159">Microsoft. Azure. Commands. Network. Models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="734ac-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="734ac-160">Note</span><span class="sxs-lookup"><span data-stu-id="734ac-160">NOTES</span></span>

## <span data-ttu-id="734ac-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="734ac-161">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 9b3991a24430afa74853f742bffa12b772dbeaf2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301482"
---
# <span data-ttu-id="23e8f-101">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="23e8f-101">New-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="23e8f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="23e8f-102">SYNOPSIS</span></span>
<span data-ttu-id="23e8f-103">Creare una risorsa di Virtual Appliance di rete.</span><span class="sxs-lookup"><span data-stu-id="23e8f-103">Create a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="23e8f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23e8f-104">SYNTAX</span></span>

### <span data-ttu-id="23e8f-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="23e8f-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> -Location <String>
 -VirtualHubId <String> -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32>
 [-Identity <PSManagedServiceIdentity>] [-BootStrapConfigurationBlob <String[]>]
 [-CloudInitConfigurationBlob <String[]>] [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23e8f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23e8f-106">ResourceIdParameterSet</span></span>
```
New-AzNetworkVirtualAppliance -ResourceId <String> -Location <String> -VirtualHubId <String>
 -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32> [-Identity <PSManagedServiceIdentity>]
 [-BootStrapConfigurationBlob <String[]>] [-CloudInitConfigurationBlob <String[]>]
 [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23e8f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23e8f-107">DESCRIPTION</span></span>
<span data-ttu-id="23e8f-108">Il comando New-AzNetworkVirtualAppliance crea una risorsa di Virtual Appliance di rete in Azure.</span><span class="sxs-lookup"><span data-stu-id="23e8f-108">The New-AzNetworkVirtualAppliance command creates a Network Virtual Appliance resource in Azure.</span></span>

## <span data-ttu-id="23e8f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23e8f-109">EXAMPLES</span></span>

### <span data-ttu-id="23e8f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="23e8f-110">Example 1</span></span>
```powershell
PS C:\> $sku=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
PS C:\> $hub=Get-AzVirtualHub -ResourceGroupName testrg -Name hub
PS C:\> $nva=New-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -Location eastus2 -VirtualApplianceAsn 1270 -VirtualHubId $hub.Id -Sku $sku -CloudInitConfiguration "echo Hello World!"

```

<span data-ttu-id="23e8f-111">Crea una nuova risorsa di Virtual Appliance di rete in un gruppo di risorse: testrg.</span><span class="sxs-lookup"><span data-stu-id="23e8f-111">Creates a new Network Virtual Appliance resource in resource group: testrg.</span></span>

## <span data-ttu-id="23e8f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="23e8f-112">PARAMETERS</span></span>

### <span data-ttu-id="23e8f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23e8f-113">-AsJob</span></span>
<span data-ttu-id="23e8f-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="23e8f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23e8f-115">-BootStrapConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="23e8f-115">-BootStrapConfigurationBlob</span></span>
<span data-ttu-id="23e8f-116">URL BLOB della configurazione bootstrap.</span><span class="sxs-lookup"><span data-stu-id="23e8f-116">The Bootstrap configuration blob URL.</span></span>

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

### <span data-ttu-id="23e8f-117">-CloudInitConfiguration</span><span class="sxs-lookup"><span data-stu-id="23e8f-117">-CloudInitConfiguration</span></span>
<span data-ttu-id="23e8f-118">La configurazione di Cloudinit come testo normale.</span><span class="sxs-lookup"><span data-stu-id="23e8f-118">The Cloudinit configuration as plain text.</span></span>

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

### <span data-ttu-id="23e8f-119">-CloudInitConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="23e8f-119">-CloudInitConfigurationBlob</span></span>
<span data-ttu-id="23e8f-120">URL di archiviazione BLOB di configurazione Cloudinit.</span><span class="sxs-lookup"><span data-stu-id="23e8f-120">The Cloudinit configuration blob storage URL.</span></span>

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

### <span data-ttu-id="23e8f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23e8f-121">-DefaultProfile</span></span>
<span data-ttu-id="23e8f-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="23e8f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23e8f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="23e8f-123">-Force</span></span>
<span data-ttu-id="23e8f-124">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="23e8f-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="23e8f-125">-Identità</span><span class="sxs-lookup"><span data-stu-id="23e8f-125">-Identity</span></span>
<span data-ttu-id="23e8f-126">Identità gestita.</span><span class="sxs-lookup"><span data-stu-id="23e8f-126">The Managed identity.</span></span>

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

### <span data-ttu-id="23e8f-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="23e8f-127">-Location</span></span>
<span data-ttu-id="23e8f-128">Posizione dell'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="23e8f-128">The public IP address location.</span></span>

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

### <span data-ttu-id="23e8f-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="23e8f-129">-Name</span></span>
<span data-ttu-id="23e8f-130">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="23e8f-130">The resource name.</span></span>

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

### <span data-ttu-id="23e8f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23e8f-131">-ResourceGroupName</span></span>
<span data-ttu-id="23e8f-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="23e8f-132">The resource group name.</span></span>

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

### <span data-ttu-id="23e8f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23e8f-133">-ResourceId</span></span>
<span data-ttu-id="23e8f-134">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="23e8f-134">The resource Id.</span></span>

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

### <span data-ttu-id="23e8f-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="23e8f-135">-Sku</span></span>
<span data-ttu-id="23e8f-136">SKU dell'appliance virtuale.</span><span class="sxs-lookup"><span data-stu-id="23e8f-136">The Sku of the Virtual Appliance.</span></span>

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

### <span data-ttu-id="23e8f-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="23e8f-137">-Tag</span></span>
<span data-ttu-id="23e8f-138">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="23e8f-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="23e8f-139">-VirtualApplianceAsn</span><span class="sxs-lookup"><span data-stu-id="23e8f-139">-VirtualApplianceAsn</span></span>
<span data-ttu-id="23e8f-140">Il numero ASN dell'appliance virtuale.</span><span class="sxs-lookup"><span data-stu-id="23e8f-140">The ASN number of the Virtual Appliance.</span></span>

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

### <span data-ttu-id="23e8f-141">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="23e8f-141">-VirtualHubId</span></span>
<span data-ttu-id="23e8f-142">ID risorsa dell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="23e8f-142">The Resource Id of the Virtual Hub.</span></span>

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

### <span data-ttu-id="23e8f-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="23e8f-143">-Confirm</span></span>
<span data-ttu-id="23e8f-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23e8f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23e8f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23e8f-145">-WhatIf</span></span>
<span data-ttu-id="23e8f-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23e8f-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23e8f-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23e8f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23e8f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23e8f-148">CommonParameters</span></span>
<span data-ttu-id="23e8f-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23e8f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23e8f-150">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23e8f-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23e8f-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="23e8f-151">INPUTS</span></span>

### <span data-ttu-id="23e8f-152">System. String</span><span class="sxs-lookup"><span data-stu-id="23e8f-152">System.String</span></span>

### <span data-ttu-id="23e8f-153">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="23e8f-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

### <span data-ttu-id="23e8f-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="23e8f-154">System.Int32</span></span>

### <span data-ttu-id="23e8f-155">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="23e8f-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

### <span data-ttu-id="23e8f-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="23e8f-156">System.String[]</span></span>

### <span data-ttu-id="23e8f-157">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="23e8f-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="23e8f-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23e8f-158">OUTPUTS</span></span>

### <span data-ttu-id="23e8f-159">Microsoft. Azure. Commands. Network. Models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="23e8f-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="23e8f-160">Note</span><span class="sxs-lookup"><span data-stu-id="23e8f-160">NOTES</span></span>

## <span data-ttu-id="23e8f-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23e8f-161">RELATED LINKS</span></span>

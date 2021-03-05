---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 380061134c94cdbd618aaa4d18ef39b0b3a11359
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985836"
---
# <span data-ttu-id="160bc-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="160bc-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="160bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="160bc-102">SYNOPSIS</span></span>
<span data-ttu-id="160bc-103">Crea un Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="160bc-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="160bc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="160bc-104">SYNTAX</span></span>

### <span data-ttu-id="160bc-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="160bc-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-Identity <PSManagedServiceIdentity>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="160bc-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="160bc-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="160bc-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="160bc-107">DESCRIPTION</span></span>
<span data-ttu-id="160bc-108">Il cmdlet **New-AzExpressRoutePort** crea un Azure ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="160bc-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="160bc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="160bc-109">EXAMPLES</span></span>

### <span data-ttu-id="160bc-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="160bc-110">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    Name='ExpressRoutePort'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

### <span data-ttu-id="160bc-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="160bc-111">Example 2</span></span>
```powershell
PS C:\> $parameters = @{
    ResourceId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.Network/expressRoutePorts/<PortName>'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

## <span data-ttu-id="160bc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="160bc-112">PARAMETERS</span></span>

### <span data-ttu-id="160bc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="160bc-113">-AsJob</span></span>
<span data-ttu-id="160bc-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="160bc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="160bc-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="160bc-115">-BandwidthInGbps</span></span>
<span data-ttu-id="160bc-116">Larghezza di banda delle porte in Gbps</span><span class="sxs-lookup"><span data-stu-id="160bc-116">Bandwidth of procured ports in Gbps</span></span>

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

### <span data-ttu-id="160bc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="160bc-117">-DefaultProfile</span></span>
<span data-ttu-id="160bc-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="160bc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="160bc-119">-Encapsulation</span><span class="sxs-lookup"><span data-stu-id="160bc-119">-Encapsulation</span></span>
<span data-ttu-id="160bc-120">Metodo di encapsulation sulle porte fisiche.</span><span class="sxs-lookup"><span data-stu-id="160bc-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="160bc-121">-Force</span><span class="sxs-lookup"><span data-stu-id="160bc-121">-Force</span></span>
<span data-ttu-id="160bc-122">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="160bc-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="160bc-123">-Identity</span><span class="sxs-lookup"><span data-stu-id="160bc-123">-Identity</span></span>
<span data-ttu-id="160bc-124">Identità assegnate dall'utente per la lettura della configurazione MacSec</span><span class="sxs-lookup"><span data-stu-id="160bc-124">User Assigned Identity for reading MacSec configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="160bc-125">-Link</span><span class="sxs-lookup"><span data-stu-id="160bc-125">-Link</span></span>
<span data-ttu-id="160bc-126">Set di collegamenti fisici della risorsa ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="160bc-126">The set of physical links of the ExpressRoutePort resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="160bc-127">-Location</span><span class="sxs-lookup"><span data-stu-id="160bc-127">-Location</span></span>
<span data-ttu-id="160bc-128">Posizione.</span><span class="sxs-lookup"><span data-stu-id="160bc-128">The location.</span></span>

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

### <span data-ttu-id="160bc-129">-Name</span><span class="sxs-lookup"><span data-stu-id="160bc-129">-Name</span></span>
<span data-ttu-id="160bc-130">Nome di ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="160bc-130">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="160bc-131">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="160bc-131">-PeeringLocation</span></span>
<span data-ttu-id="160bc-132">Nome della posizione di peering a cui è mappato ExpressRoutePort fisicamente.</span><span class="sxs-lookup"><span data-stu-id="160bc-132">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="160bc-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="160bc-133">-ResourceGroupName</span></span>
<span data-ttu-id="160bc-134">Nome del gruppo di risorse di ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="160bc-134">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="160bc-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="160bc-135">-ResourceId</span></span>
<span data-ttu-id="160bc-136">ResourceId della porta express route.</span><span class="sxs-lookup"><span data-stu-id="160bc-136">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="160bc-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="160bc-137">-Tag</span></span>
<span data-ttu-id="160bc-138">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="160bc-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="160bc-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="160bc-139">-Confirm</span></span>
<span data-ttu-id="160bc-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="160bc-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="160bc-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="160bc-141">-WhatIf</span></span>
<span data-ttu-id="160bc-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="160bc-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="160bc-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="160bc-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="160bc-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="160bc-144">CommonParameters</span></span>
<span data-ttu-id="160bc-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="160bc-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="160bc-146">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="160bc-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="160bc-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="160bc-147">INPUTS</span></span>

### <span data-ttu-id="160bc-148">System.String</span><span class="sxs-lookup"><span data-stu-id="160bc-148">System.String</span></span>

### <span data-ttu-id="160bc-149">System.Int32</span><span class="sxs-lookup"><span data-stu-id="160bc-149">System.Int32</span></span>

### <span data-ttu-id="160bc-150">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="160bc-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="160bc-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span><span class="sxs-lookup"><span data-stu-id="160bc-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="160bc-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="160bc-152">OUTPUTS</span></span>

### <span data-ttu-id="160bc-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="160bc-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="160bc-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="160bc-154">NOTES</span></span>

## <span data-ttu-id="160bc-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="160bc-155">RELATED LINKS</span></span>

[<span data-ttu-id="160bc-156">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="160bc-156">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="160bc-157">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="160bc-157">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="160bc-158">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="160bc-158">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)

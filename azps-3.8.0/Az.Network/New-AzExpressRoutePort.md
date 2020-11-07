---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 54cdcbbd1d9564dde4fbe4a9aa0b0bea8a0325a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864634"
---
# <span data-ttu-id="c7075-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c7075-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="c7075-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7075-102">SYNOPSIS</span></span>
<span data-ttu-id="c7075-103">Crea un ExpressRoutePort di Azure.</span><span class="sxs-lookup"><span data-stu-id="c7075-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="c7075-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7075-104">SYNTAX</span></span>

### <span data-ttu-id="c7075-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c7075-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-Identity <PSManagedServiceIdentity>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7075-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7075-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7075-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7075-107">DESCRIPTION</span></span>
<span data-ttu-id="c7075-108">Il cmdlet **New-AzExpressRoutePort** crea un ExpressRoutePort di Azure</span><span class="sxs-lookup"><span data-stu-id="c7075-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="c7075-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7075-109">EXAMPLES</span></span>

### <span data-ttu-id="c7075-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c7075-110">Example 1</span></span>
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

### <span data-ttu-id="c7075-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c7075-111">Example 2</span></span>
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

## <span data-ttu-id="c7075-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7075-112">PARAMETERS</span></span>

### <span data-ttu-id="c7075-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7075-113">-AsJob</span></span>
<span data-ttu-id="c7075-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c7075-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7075-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="c7075-115">-BandwidthInGbps</span></span>
<span data-ttu-id="c7075-116">Larghezza di banda delle porte procurate in Gbps</span><span class="sxs-lookup"><span data-stu-id="c7075-116">Bandwidth of procured ports in Gbps</span></span>

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

### <span data-ttu-id="c7075-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7075-117">-DefaultProfile</span></span>
<span data-ttu-id="c7075-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7075-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7075-119">-Incapsulamento</span><span class="sxs-lookup"><span data-stu-id="c7075-119">-Encapsulation</span></span>
<span data-ttu-id="c7075-120">Metodo di incapsulamento sulle porte fisiche.</span><span class="sxs-lookup"><span data-stu-id="c7075-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="c7075-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c7075-121">-Force</span></span>
<span data-ttu-id="c7075-122">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="c7075-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c7075-123">-Identità</span><span class="sxs-lookup"><span data-stu-id="c7075-123">-Identity</span></span>
<span data-ttu-id="c7075-124">Identità assegnata dall'utente per la lettura della configurazione di MacSec</span><span class="sxs-lookup"><span data-stu-id="c7075-124">User Assigned Identity for reading MacSec configuration</span></span>

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

### <span data-ttu-id="c7075-125">-Collegamento</span><span class="sxs-lookup"><span data-stu-id="c7075-125">-Link</span></span>
<span data-ttu-id="c7075-126">Set di collegamenti fisici della risorsa ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c7075-126">The set of physical links of the ExpressRoutePort resource</span></span>

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

### <span data-ttu-id="c7075-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c7075-127">-Location</span></span>
<span data-ttu-id="c7075-128">La posizione.</span><span class="sxs-lookup"><span data-stu-id="c7075-128">The location.</span></span>

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

### <span data-ttu-id="c7075-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7075-129">-Name</span></span>
<span data-ttu-id="c7075-130">Il nome del ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="c7075-130">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="c7075-131">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="c7075-131">-PeeringLocation</span></span>
<span data-ttu-id="c7075-132">Il nome della posizione di peering a cui è associato il mapping di ExpressRoutePort fisicamente.</span><span class="sxs-lookup"><span data-stu-id="c7075-132">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="c7075-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7075-133">-ResourceGroupName</span></span>
<span data-ttu-id="c7075-134">Nome del gruppo di risorse di ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="c7075-134">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="c7075-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7075-135">-ResourceId</span></span>
<span data-ttu-id="c7075-136">ResourceId della porta di route espressa.</span><span class="sxs-lookup"><span data-stu-id="c7075-136">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="c7075-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="c7075-137">-Tag</span></span>
<span data-ttu-id="c7075-138">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="c7075-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c7075-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c7075-139">-Confirm</span></span>
<span data-ttu-id="c7075-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7075-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7075-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7075-141">-WhatIf</span></span>
<span data-ttu-id="c7075-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7075-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7075-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7075-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7075-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7075-144">CommonParameters</span></span>
<span data-ttu-id="c7075-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7075-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7075-146">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7075-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7075-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7075-147">INPUTS</span></span>

### <span data-ttu-id="c7075-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c7075-148">System.String</span></span>

### <span data-ttu-id="c7075-149">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c7075-149">System.Int32</span></span>

### <span data-ttu-id="c7075-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c7075-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c7075-151">Microsoft. Azure. Commands. Network. Models. PSExpressRouteLink []</span><span class="sxs-lookup"><span data-stu-id="c7075-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="c7075-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7075-152">OUTPUTS</span></span>

### <span data-ttu-id="c7075-153">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c7075-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="c7075-154">Note</span><span class="sxs-lookup"><span data-stu-id="c7075-154">NOTES</span></span>

## <span data-ttu-id="c7075-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7075-155">RELATED LINKS</span></span>

[<span data-ttu-id="c7075-156">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c7075-156">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="c7075-157">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c7075-157">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="c7075-158">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c7075-158">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)

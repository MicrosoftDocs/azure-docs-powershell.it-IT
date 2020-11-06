---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRoutePort.md
ms.openlocfilehash: 8d3b204815fc273f97a549582a193002f5f4a48d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513684"
---
# <span data-ttu-id="6914f-101">New-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6914f-101">New-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="6914f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6914f-102">SYNOPSIS</span></span>
<span data-ttu-id="6914f-103">Crea un ExpressRoutePort di Azure.</span><span class="sxs-lookup"><span data-stu-id="6914f-103">Creates an Azure ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6914f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6914f-104">SYNTAX</span></span>

### <span data-ttu-id="6914f-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6914f-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6914f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6914f-106">ResourceIdParameterSet</span></span>
```
New-AzureRmExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6914f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6914f-107">DESCRIPTION</span></span>
<span data-ttu-id="6914f-108">Il cmdlet **New-AzureRmExpressRoutePort** crea un ExpressRoutePort di Azure</span><span class="sxs-lookup"><span data-stu-id="6914f-108">The **New-AzureRmExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="6914f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6914f-109">EXAMPLES</span></span>

### <span data-ttu-id="6914f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6914f-110">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    Name='ExpressRoutePort'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzureRmExpressRoutePort @parameters
```

### <span data-ttu-id="6914f-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6914f-111">Example 2</span></span>
```powershell
PS C:\> $parameters = @{
    ResourceId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.Network/expressRoutePorts/<PortName>'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzureRmExpressRoutePort @parameters
```

## <span data-ttu-id="6914f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6914f-112">PARAMETERS</span></span>

### <span data-ttu-id="6914f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6914f-113">-AsJob</span></span>
<span data-ttu-id="6914f-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6914f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6914f-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="6914f-115">-BandwidthInGbps</span></span>
<span data-ttu-id="6914f-116">Larghezza di banda delle porte procurate in Gbps</span><span class="sxs-lookup"><span data-stu-id="6914f-116">Bandwidth of procured ports in Gbps</span></span>

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

### <span data-ttu-id="6914f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6914f-117">-DefaultProfile</span></span>
<span data-ttu-id="6914f-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6914f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6914f-119">-Incapsulamento</span><span class="sxs-lookup"><span data-stu-id="6914f-119">-Encapsulation</span></span>
<span data-ttu-id="6914f-120">Metodo di incapsulamento sulle porte fisiche.</span><span class="sxs-lookup"><span data-stu-id="6914f-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="6914f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6914f-121">-Force</span></span>
<span data-ttu-id="6914f-122">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="6914f-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6914f-123">-Collegamento</span><span class="sxs-lookup"><span data-stu-id="6914f-123">-Link</span></span>
<span data-ttu-id="6914f-124">Set di collegamenti fisici della risorsa ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6914f-124">The set of physical links of the ExpressRoutePort resource</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6914f-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6914f-125">-Location</span></span>
<span data-ttu-id="6914f-126">La posizione.</span><span class="sxs-lookup"><span data-stu-id="6914f-126">The location.</span></span>

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

### <span data-ttu-id="6914f-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="6914f-127">-Name</span></span>
<span data-ttu-id="6914f-128">Il nome del ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="6914f-128">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="6914f-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="6914f-129">-PeeringLocation</span></span>
<span data-ttu-id="6914f-130">Il nome della posizione di peering a cui è associato il mapping di ExpressRoutePort fisicamente.</span><span class="sxs-lookup"><span data-stu-id="6914f-130">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="6914f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6914f-131">-ResourceGroupName</span></span>
<span data-ttu-id="6914f-132">Nome del gruppo di risorse di ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="6914f-132">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="6914f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6914f-133">-ResourceId</span></span>
<span data-ttu-id="6914f-134">ResourceId della porta di route espressa.</span><span class="sxs-lookup"><span data-stu-id="6914f-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="6914f-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="6914f-135">-Tag</span></span>
<span data-ttu-id="6914f-136">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="6914f-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6914f-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6914f-137">-Confirm</span></span>
<span data-ttu-id="6914f-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6914f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6914f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6914f-139">-WhatIf</span></span>
<span data-ttu-id="6914f-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6914f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6914f-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6914f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6914f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6914f-142">CommonParameters</span></span>
<span data-ttu-id="6914f-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6914f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6914f-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6914f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6914f-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6914f-145">INPUTS</span></span>

### <span data-ttu-id="6914f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="6914f-146">System.String</span></span>

### <span data-ttu-id="6914f-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6914f-147">System.Int32</span></span>

### <span data-ttu-id="6914f-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6914f-148">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6914f-149">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Network. Models. PSExpressRouteLink, Microsoft. Azure. Commands. Network, Version = 6.3.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6914f-149">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink, Microsoft.Azure.Commands.Network, Version=6.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6914f-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6914f-150">OUTPUTS</span></span>

### <span data-ttu-id="6914f-151">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6914f-151">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="6914f-152">Note</span><span class="sxs-lookup"><span data-stu-id="6914f-152">NOTES</span></span>

## <span data-ttu-id="6914f-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6914f-153">RELATED LINKS</span></span>

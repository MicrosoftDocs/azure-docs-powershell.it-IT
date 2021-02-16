---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteServer.md
ms.openlocfilehash: 15a613f4d2c695fe42df5b02012187bdeee615b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179623"
---
# <span data-ttu-id="3752e-101">New-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="3752e-101">New-AzRouteServer</span></span>

## <span data-ttu-id="3752e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3752e-102">SYNOPSIS</span></span>
<span data-ttu-id="3752e-103">Crea un server di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="3752e-103">Creates an Azure RouteServer.</span></span>

## <span data-ttu-id="3752e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3752e-104">SYNTAX</span></span>

```
New-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> -HostedSubnet <String>
 -Location <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3752e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3752e-105">DESCRIPTION</span></span>
<span data-ttu-id="3752e-106">Il cmdlet **New-AzRouteServer** crea un Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="3752e-106">The **New-AzRouteServer** cmdlet creates an Azure RouteServer</span></span>

## <span data-ttu-id="3752e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3752e-107">EXAMPLES</span></span>

### <span data-ttu-id="3752e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3752e-108">Example 1</span></span>
```powershell
PS C:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzRouteServer -RouteServerName $routeServerName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="3752e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3752e-109">PARAMETERS</span></span>

### <span data-ttu-id="3752e-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3752e-110">-AsJob</span></span>
<span data-ttu-id="3752e-111">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3752e-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3752e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3752e-112">-DefaultProfile</span></span>
<span data-ttu-id="3752e-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3752e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3752e-114">-Force</span><span class="sxs-lookup"><span data-stu-id="3752e-114">-Force</span></span>
<span data-ttu-id="3752e-115">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="3752e-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="3752e-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="3752e-116">-HostedSubnet</span></span>
<span data-ttu-id="3752e-117">Subnet in cui è ospitato il server delle route.</span><span class="sxs-lookup"><span data-stu-id="3752e-117">The subnet where the route server is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3752e-118">-Location</span><span class="sxs-lookup"><span data-stu-id="3752e-118">-Location</span></span>
<span data-ttu-id="3752e-119">Posizione.</span><span class="sxs-lookup"><span data-stu-id="3752e-119">The location.</span></span>

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

### <span data-ttu-id="3752e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3752e-120">-ResourceGroupName</span></span>
<span data-ttu-id="3752e-121">Nome del gruppo di risorse del server di route.</span><span class="sxs-lookup"><span data-stu-id="3752e-121">The resource group name of the route server.</span></span>

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

### <span data-ttu-id="3752e-122">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="3752e-122">-RouteServerName</span></span>
<span data-ttu-id="3752e-123">Nome del server di route.</span><span class="sxs-lookup"><span data-stu-id="3752e-123">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3752e-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="3752e-124">-Tag</span></span>
<span data-ttu-id="3752e-125">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="3752e-125">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="3752e-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3752e-126">-Confirm</span></span>
<span data-ttu-id="3752e-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3752e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3752e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3752e-128">-WhatIf</span></span>
<span data-ttu-id="3752e-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3752e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3752e-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3752e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3752e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3752e-131">CommonParameters</span></span>
<span data-ttu-id="3752e-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3752e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3752e-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3752e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3752e-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="3752e-134">INPUTS</span></span>

### <span data-ttu-id="3752e-135">System.String</span><span class="sxs-lookup"><span data-stu-id="3752e-135">System.String</span></span>

### <span data-ttu-id="3752e-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3752e-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3752e-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3752e-137">OUTPUTS</span></span>

### <span data-ttu-id="3752e-138">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="3752e-138">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="3752e-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="3752e-139">NOTES</span></span>

## <span data-ttu-id="3752e-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3752e-140">RELATED LINKS</span></span>

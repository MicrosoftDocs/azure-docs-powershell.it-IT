---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azrouteserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServer.md
ms.openlocfilehash: 9f00ccfb01cd6e6b0d80b120364f8ac0c81daae0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184127"
---
# <span data-ttu-id="f9740-101">Update-AzRouteServer</span><span class="sxs-lookup"><span data-stu-id="f9740-101">Update-AzRouteServer</span></span>

## <span data-ttu-id="f9740-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9740-102">SYNOPSIS</span></span>
<span data-ttu-id="f9740-103">Aggiornare un server di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="f9740-103">Update an Azure RouteServer.</span></span>

## <span data-ttu-id="f9740-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9740-104">SYNTAX</span></span>

### <span data-ttu-id="f9740-105">RouteServerNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f9740-105">RouteServerNameParameterSet (Default)</span></span>
```
Update-AzRouteServer -ResourceGroupName <String> -RouteServerName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9740-106">RouteServerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9740-106">RouteServerResourceIdParameterSet</span></span>
```
Update-AzRouteServer [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9740-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f9740-107">DESCRIPTION</span></span>
<span data-ttu-id="f9740-108">Il cmdlet **Update-AzRouteServer** passa il traffico branch-to-branch a un Azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="f9740-108">The **Update-AzRouteServer** cmdlet switches the branch-to-branch traffic to an Azure RouteServer.</span></span>

## <span data-ttu-id="f9740-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9740-109">EXAMPLES</span></span>

### <span data-ttu-id="f9740-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f9740-110">Example 1</span></span>
```powershell
PS C:\>  Update-AzRouteServer -ResourceGroupName $rgname -RouteServerName $routeServerName -AllowBranchToBranchTraffic
```
<span data-ttu-id="f9740-111">Per abilitare il traffico di succursale per il server delle route.</span><span class="sxs-lookup"><span data-stu-id="f9740-111">To enable branch to branch traffic for route server.</span></span>

### <span data-ttu-id="f9740-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f9740-112">Example 1</span></span>
```powershell
PS C:\>  Update-AzRouteServer -ResourceGroupName $rgname -RouteServerName $routeServerName
```
<span data-ttu-id="f9740-113">Per disabilitare il traffico di succursale per il server delle route.</span><span class="sxs-lookup"><span data-stu-id="f9740-113">To disable branch to branch traffic for route server.</span></span>

## <span data-ttu-id="f9740-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9740-114">PARAMETERS</span></span>

### <span data-ttu-id="f9740-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="f9740-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="f9740-116">Flag per consentire il traffico di succursale per il server delle route.</span><span class="sxs-lookup"><span data-stu-id="f9740-116">Flag to allow branch to branch traffic for route server.</span></span>

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

### <span data-ttu-id="f9740-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9740-117">-DefaultProfile</span></span>
<span data-ttu-id="f9740-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f9740-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9740-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9740-119">-ResourceGroupName</span></span>
<span data-ttu-id="f9740-120">Nome del gruppo di risorse del server di route.</span><span class="sxs-lookup"><span data-stu-id="f9740-120">The resource group name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9740-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9740-121">-ResourceId</span></span>
<span data-ttu-id="f9740-122">ResourceId del server delle route.</span><span class="sxs-lookup"><span data-stu-id="f9740-122">ResourceId of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9740-123">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="f9740-123">-RouteServerName</span></span>
<span data-ttu-id="f9740-124">Nome del server di route.</span><span class="sxs-lookup"><span data-stu-id="f9740-124">The name of the route server.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9740-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9740-125">-Confirm</span></span>
<span data-ttu-id="f9740-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9740-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9740-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9740-127">-WhatIf</span></span>
<span data-ttu-id="f9740-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9740-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9740-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9740-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9740-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9740-130">CommonParameters</span></span>
<span data-ttu-id="f9740-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9740-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9740-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f9740-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9740-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="f9740-133">INPUTS</span></span>

### <span data-ttu-id="f9740-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f9740-134">System.String</span></span>

## <span data-ttu-id="f9740-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9740-135">OUTPUTS</span></span>

### <span data-ttu-id="f9740-136">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="f9740-136">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="f9740-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="f9740-137">NOTES</span></span>

## <span data-ttu-id="f9740-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9740-138">RELATED LINKS</span></span>

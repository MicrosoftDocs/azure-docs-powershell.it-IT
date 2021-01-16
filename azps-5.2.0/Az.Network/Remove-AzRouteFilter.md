---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteFilter.md
ms.openlocfilehash: dc6af2cb623e2d2d67b337e3a6e3ff27b5aebd69
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344788"
---
# <span data-ttu-id="a315e-101">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a315e-101">Remove-AzRouteFilter</span></span>

## <span data-ttu-id="a315e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a315e-102">SYNOPSIS</span></span>
<span data-ttu-id="a315e-103">Rimuove un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="a315e-103">Removes a route filter.</span></span>

## <span data-ttu-id="a315e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a315e-104">SYNTAX</span></span>

```
Remove-AzRouteFilter -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a315e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a315e-105">DESCRIPTION</span></span>
<span data-ttu-id="a315e-106">Il cmdlet **Remove-AzRouteFilter** rimuove un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="a315e-106">The **Remove-AzRouteFilter** cmdlet removes a route filter.</span></span>

## <span data-ttu-id="a315e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a315e-107">EXAMPLES</span></span>

### <span data-ttu-id="a315e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a315e-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteFilter -Name "RouteFilter01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a315e-109">Il comando rimuove il filtro della route denominato RouteFilter01 nel gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="a315e-109">The command removes the route filter named RouteFilter01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="a315e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a315e-110">PARAMETERS</span></span>

### <span data-ttu-id="a315e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a315e-111">-DefaultProfile</span></span>
<span data-ttu-id="a315e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a315e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a315e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a315e-113">-Force</span></span>
<span data-ttu-id="a315e-114">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="a315e-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a315e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a315e-115">-Name</span></span>
<span data-ttu-id="a315e-116">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a315e-116">The resource name.</span></span>

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

### <span data-ttu-id="a315e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a315e-117">-PassThru</span></span>
<span data-ttu-id="a315e-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="a315e-118">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="a315e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a315e-119">-ResourceGroupName</span></span>
<span data-ttu-id="a315e-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a315e-120">The resource group name.</span></span>

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

### <span data-ttu-id="a315e-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a315e-121">-Confirm</span></span>
<span data-ttu-id="a315e-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a315e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a315e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a315e-123">-WhatIf</span></span>
<span data-ttu-id="a315e-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a315e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a315e-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a315e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a315e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a315e-126">CommonParameters</span></span>
<span data-ttu-id="a315e-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a315e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a315e-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a315e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a315e-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a315e-129">INPUTS</span></span>

### <span data-ttu-id="a315e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a315e-130">System.String</span></span>

## <span data-ttu-id="a315e-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a315e-131">OUTPUTS</span></span>

### <span data-ttu-id="a315e-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a315e-132">System.Boolean</span></span>

## <span data-ttu-id="a315e-133">Note</span><span class="sxs-lookup"><span data-stu-id="a315e-133">NOTES</span></span>

## <span data-ttu-id="a315e-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a315e-134">RELATED LINKS</span></span>

[<span data-ttu-id="a315e-135">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a315e-135">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="a315e-136">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a315e-136">New-AzRouteFilter</span></span>](./New-AzRouteFilter.md)

[<span data-ttu-id="a315e-137">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="a315e-137">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="a315e-138">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a315e-138">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="a315e-139">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a315e-139">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="a315e-140">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a315e-140">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="a315e-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a315e-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="a315e-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a315e-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

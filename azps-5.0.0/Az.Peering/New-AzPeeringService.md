---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
ms.openlocfilehash: 60772963530d14eeb93f2f28fbf5e067ac5833ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199499"
---
# <span data-ttu-id="c7429-101">New-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="c7429-101">New-AzPeeringService</span></span>

## <span data-ttu-id="c7429-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7429-102">SYNOPSIS</span></span>
<span data-ttu-id="c7429-103">Crea un nuovo servizio di peering.</span><span class="sxs-lookup"><span data-stu-id="c7429-103">Creates a new peering service.</span></span>

## <span data-ttu-id="c7429-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7429-104">SYNTAX</span></span>

```
New-AzPeeringService [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeeringServiceProvider] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7429-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7429-105">DESCRIPTION</span></span>
<span data-ttu-id="c7429-106">Crea un servizio di peering.</span><span class="sxs-lookup"><span data-stu-id="c7429-106">Creates peering service.</span></span>

## <span data-ttu-id="c7429-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7429-107">EXAMPLES</span></span>

### <span data-ttu-id="c7429-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c7429-108">Example 1</span></span>
```powershell
PS C:\> New-AzPeeringService -ResourceGroupName $resourceGroup -Name $name -Location $loc -PeeringServiceProvider $provider

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="c7429-109">Crea un oggetto servizio peering con il provider e la posizione di peering.</span><span class="sxs-lookup"><span data-stu-id="c7429-109">Creates a peering service object with provider and peering location.</span></span> <span data-ttu-id="c7429-110">Usare in congiunzione con `Get-AzPeeringServiceProvider` e `Get-AzPeeringServiceLocation`</span><span class="sxs-lookup"><span data-stu-id="c7429-110">Use in conjuction with `Get-AzPeeringServiceProvider` and `Get-AzPeeringServiceLocation`</span></span>

## <span data-ttu-id="c7429-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7429-111">PARAMETERS</span></span>

### <span data-ttu-id="c7429-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7429-112">-AsJob</span></span>
<span data-ttu-id="c7429-113">Eseguire in background.</span><span class="sxs-lookup"><span data-stu-id="c7429-113">Run in the background.</span></span>

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

### <span data-ttu-id="c7429-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7429-114">-DefaultProfile</span></span>
<span data-ttu-id="c7429-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7429-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7429-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7429-116">-Name</span></span>
<span data-ttu-id="c7429-117">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="c7429-117">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7429-118">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="c7429-118">-PeeringLocation</span></span>
<span data-ttu-id="c7429-119">Posizione fisica diversa dall'area di Azure.</span><span class="sxs-lookup"><span data-stu-id="c7429-119">The Physical Location Different from Azure Region.</span></span> <span data-ttu-id="c7429-120">Usare Get-AzPeeringServiceLocation [-Country <country> ]</span><span class="sxs-lookup"><span data-stu-id="c7429-120">Use Get-AzPeeringServiceLocation [-Country <country>]</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7429-121">-PeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="c7429-121">-PeeringServiceProvider</span></span>
<span data-ttu-id="c7429-122">Nome del provider del servizio peering.</span><span class="sxs-lookup"><span data-stu-id="c7429-122">The peering service provider name.</span></span>
<span data-ttu-id="c7429-123">Usare Get-AzPeeringServiceProvider cmdlet per un elenco</span><span class="sxs-lookup"><span data-stu-id="c7429-123">Use Get-AzPeeringServiceProvider cmdlet for a list</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7429-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7429-124">-ResourceGroupName</span></span>
<span data-ttu-id="c7429-125">Il nome della risorsa crea o usa un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="c7429-125">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7429-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="c7429-126">-Tag</span></span>
<span data-ttu-id="c7429-127">Tag da associare al servizio Microsoft InputObject.</span><span class="sxs-lookup"><span data-stu-id="c7429-127">The tags to associate with the Microsoft InputObject Service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7429-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c7429-128">-Confirm</span></span>
<span data-ttu-id="c7429-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7429-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7429-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7429-130">-WhatIf</span></span>
<span data-ttu-id="c7429-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7429-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7429-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7429-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7429-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7429-133">CommonParameters</span></span>
<span data-ttu-id="c7429-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7429-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7429-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7429-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7429-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7429-136">INPUTS</span></span>

### <span data-ttu-id="c7429-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c7429-137">None</span></span>

## <span data-ttu-id="c7429-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7429-138">OUTPUTS</span></span>

### <span data-ttu-id="c7429-139">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="c7429-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="c7429-140">Note</span><span class="sxs-lookup"><span data-stu-id="c7429-140">NOTES</span></span>

## <span data-ttu-id="c7429-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7429-141">RELATED LINKS</span></span>
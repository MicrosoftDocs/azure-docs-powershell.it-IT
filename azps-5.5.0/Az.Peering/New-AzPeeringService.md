---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringService.md
ms.openlocfilehash: 60772963530d14eeb93f2f28fbf5e067ac5833ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179167"
---
# <span data-ttu-id="b3bc9-101">New-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="b3bc9-101">New-AzPeeringService</span></span>

## <span data-ttu-id="b3bc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3bc9-102">SYNOPSIS</span></span>
<span data-ttu-id="b3bc9-103">Crea un nuovo servizio di peering.</span><span class="sxs-lookup"><span data-stu-id="b3bc9-103">Creates a new peering service.</span></span>

## <span data-ttu-id="b3bc9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3bc9-104">SYNTAX</span></span>

```
New-AzPeeringService [-ResourceGroupName] <String> [-Name] <String> [-PeeringLocation] <String>
 [-PeeringServiceProvider] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3bc9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b3bc9-105">DESCRIPTION</span></span>
<span data-ttu-id="b3bc9-106">Crea un servizio di peering.</span><span class="sxs-lookup"><span data-stu-id="b3bc9-106">Creates peering service.</span></span>

## <span data-ttu-id="b3bc9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3bc9-107">EXAMPLES</span></span>

### <span data-ttu-id="b3bc9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b3bc9-108">Example 1</span></span>
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

<span data-ttu-id="b3bc9-109">Crea un oggetto servizio di peering con provider e posizione di peering.</span><span class="sxs-lookup"><span data-stu-id="b3bc9-109">Creates a peering service object with provider and peering location.</span></span> <span data-ttu-id="b3bc9-110">Uso in coniugato con `Get-AzPeeringServiceProvider` e `Get-AzPeeringServiceLocation`</span><span class="sxs-lookup"><span data-stu-id="b3bc9-110">Use in conjuction with `Get-AzPeeringServiceProvider` and `Get-AzPeeringServiceLocation`</span></span>

## <span data-ttu-id="b3bc9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3bc9-111">PARAMETERS</span></span>

### <span data-ttu-id="b3bc9-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3bc9-112">-AsJob</span></span>
<span data-ttu-id="b3bc9-113">Esegui in background.</span><span class="sxs-lookup"><span data-stu-id="b3bc9-113">Run in the background.</span></span>

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

### <span data-ttu-id="b3bc9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3bc9-114">-DefaultProfile</span></span>
<span data-ttu-id="b3bc9-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3bc9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3bc9-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b3bc9-116">-Name</span></span>
<span data-ttu-id="b3bc9-117">Nome univoco di PSCollectioning.</span><span class="sxs-lookup"><span data-stu-id="b3bc9-117">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="b3bc9-118">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="b3bc9-118">-PeeringLocation</span></span>
<span data-ttu-id="b3bc9-119">Posizione fisica diversa dall'area geografica di Azure.</span><span class="sxs-lookup"><span data-stu-id="b3bc9-119">The Physical Location Different from Azure Region.</span></span> <span data-ttu-id="b3bc9-120">Usare Get-AzPeeringServiceLocation [-Country <country> ]</span><span class="sxs-lookup"><span data-stu-id="b3bc9-120">Use Get-AzPeeringServiceLocation [-Country <country>]</span></span>

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

### <span data-ttu-id="b3bc9-121">-PeeringServiceProvider</span><span class="sxs-lookup"><span data-stu-id="b3bc9-121">-PeeringServiceProvider</span></span>
<span data-ttu-id="b3bc9-122">Nome del provider del servizio di peering.</span><span class="sxs-lookup"><span data-stu-id="b3bc9-122">The peering service provider name.</span></span>
<span data-ttu-id="b3bc9-123">Usare Get-AzPeeringServiceProvider cmdlet per un elenco</span><span class="sxs-lookup"><span data-stu-id="b3bc9-123">Use Get-AzPeeringServiceProvider cmdlet for a list</span></span>

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

### <span data-ttu-id="b3bc9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3bc9-124">-ResourceGroupName</span></span>
<span data-ttu-id="b3bc9-125">Creare o usare il nome di un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="b3bc9-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="b3bc9-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="b3bc9-126">-Tag</span></span>
<span data-ttu-id="b3bc9-127">I tag da associare al servizio Microsoft InputObject.</span><span class="sxs-lookup"><span data-stu-id="b3bc9-127">The tags to associate with the Microsoft InputObject Service.</span></span>

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

### <span data-ttu-id="b3bc9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3bc9-128">-Confirm</span></span>
<span data-ttu-id="b3bc9-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3bc9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3bc9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3bc9-130">-WhatIf</span></span>
<span data-ttu-id="b3bc9-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3bc9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3bc9-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3bc9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3bc9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3bc9-133">CommonParameters</span></span>
<span data-ttu-id="b3bc9-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3bc9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3bc9-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b3bc9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3bc9-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="b3bc9-136">INPUTS</span></span>

### <span data-ttu-id="b3bc9-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b3bc9-137">None</span></span>

## <span data-ttu-id="b3bc9-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3bc9-138">OUTPUTS</span></span>

### <span data-ttu-id="b3bc9-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSCollectioningService</span><span class="sxs-lookup"><span data-stu-id="b3bc9-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="b3bc9-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="b3bc9-140">NOTES</span></span>

## <span data-ttu-id="b3bc9-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3bc9-141">RELATED LINKS</span></span>

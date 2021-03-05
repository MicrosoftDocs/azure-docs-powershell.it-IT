---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
ms.openlocfilehash: 154cededf20ceb88fdbc851b96189282e1b6123a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003597"
---
# <span data-ttu-id="e98db-101">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="e98db-101">Get-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="e98db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e98db-102">SYNOPSIS</span></span>
<span data-ttu-id="e98db-103">Tocca una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="e98db-103">Gets a virtual network tap</span></span>

## <span data-ttu-id="e98db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e98db-104">SYNTAX</span></span>

### <span data-ttu-id="e98db-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e98db-105">ListParameterSet (Default)</span></span>
```
Get-AzVirtualNetworkTap [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e98db-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e98db-106">GetByResourceIdParameterSet</span></span>
```
Get-AzVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e98db-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e98db-107">DESCRIPTION</span></span>
<span data-ttu-id="e98db-108">Il cmdlet **Get-AzVirtualNetworkTap** ottiene un tocco di rete virtuale di Azure o un elenco di tocchi di rete virtuale di Azure in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e98db-108">The **Get-AzVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="e98db-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e98db-109">EXAMPLES</span></span>

### <span data-ttu-id="e98db-110">Esempio 1: Toccare una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="e98db-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="e98db-111">Questo comando ottiene un riferimento tocco VirtualNetwork per dato "VirtualTap1" in "ResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="e98db-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

### <span data-ttu-id="e98db-112">Esempio 2: Usare i filtri per ottenere tutti i tocchi della rete virtuale</span><span class="sxs-lookup"><span data-stu-id="e98db-112">Example 2: Get all virtual network taps using filtering</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -Name "VirtualTap*"
```

<span data-ttu-id="e98db-113">Questo comando recupera tutti i riferimenti per il tocco di VirtualNetwork che iniziano con "VirtualTap".</span><span class="sxs-lookup"><span data-stu-id="e98db-113">This command gets all VirtualNetwork tap references that start with "VirtualTap".</span></span>

## <span data-ttu-id="e98db-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e98db-114">PARAMETERS</span></span>

### <span data-ttu-id="e98db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e98db-115">-DefaultProfile</span></span>
<span data-ttu-id="e98db-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e98db-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e98db-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e98db-117">-Name</span></span>
<span data-ttu-id="e98db-118">Nome del tocco.</span><span class="sxs-lookup"><span data-stu-id="e98db-118">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e98db-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e98db-119">-ResourceGroupName</span></span>
<span data-ttu-id="e98db-120">Il nome del gruppo di risorse del tocco della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="e98db-120">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="e98db-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e98db-121">-ResourceId</span></span>
<span data-ttu-id="e98db-122">ResourceId della risorsa VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="e98db-122">ResourceId of the VirtualNetworkTap resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e98db-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e98db-123">-Confirm</span></span>
<span data-ttu-id="e98db-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e98db-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e98db-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e98db-125">-WhatIf</span></span>
<span data-ttu-id="e98db-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e98db-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e98db-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e98db-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e98db-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e98db-128">CommonParameters</span></span>
<span data-ttu-id="e98db-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e98db-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e98db-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e98db-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e98db-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="e98db-131">INPUTS</span></span>

### <span data-ttu-id="e98db-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e98db-132">System.String</span></span>

## <span data-ttu-id="e98db-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e98db-133">OUTPUTS</span></span>

### <span data-ttu-id="e98db-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="e98db-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="e98db-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="e98db-135">NOTES</span></span>

## <span data-ttu-id="e98db-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e98db-136">RELATED LINKS</span></span>

[<span data-ttu-id="e98db-137">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="e98db-137">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="e98db-138">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="e98db-138">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="e98db-139">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="e98db-139">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)

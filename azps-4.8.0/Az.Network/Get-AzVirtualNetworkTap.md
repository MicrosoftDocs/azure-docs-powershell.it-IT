---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
ms.openlocfilehash: dc6ca5c41e5f819c8f1db3d0c601b48273e3d78e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032382"
---
# <span data-ttu-id="9fc10-101">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="9fc10-101">Get-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="9fc10-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9fc10-102">SYNOPSIS</span></span>
<span data-ttu-id="9fc10-103">Ottiene un tocco di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="9fc10-103">Gets a virtual network tap</span></span>

## <span data-ttu-id="9fc10-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9fc10-104">SYNTAX</span></span>

### <span data-ttu-id="9fc10-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9fc10-105">ListParameterSet (Default)</span></span>
```
Get-AzVirtualNetworkTap [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fc10-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fc10-106">GetByResourceIdParameterSet</span></span>
```
Get-AzVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9fc10-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9fc10-107">DESCRIPTION</span></span>
<span data-ttu-id="9fc10-108">Il cmdlet **Get-AzVirtualNetworkTap** ottiene un tocco di rete virtuale di Azure o un elenco di rubinetti di rete virtuali Azure in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9fc10-108">The **Get-AzVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="9fc10-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9fc10-109">EXAMPLES</span></span>

### <span data-ttu-id="9fc10-110">Esempio 1: ottenere un tocco di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="9fc10-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="9fc10-111">Questo comando ottiene un riferimento VirtualNetwork tap per "VirtualTap1" in "ResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="9fc10-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

### <span data-ttu-id="9fc10-112">Esempio 2: ottenere tutti i rubinetti di rete virtuale tramite filtro</span><span class="sxs-lookup"><span data-stu-id="9fc10-112">Example 2: Get all virtual network taps using filtering</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -Name "VirtualTap*"
```

<span data-ttu-id="9fc10-113">Questo comando ottiene tutti i riferimenti di VirtualNetwork tap che iniziano con "VirtualTap".</span><span class="sxs-lookup"><span data-stu-id="9fc10-113">This command gets all VirtualNetwork tap references that start with "VirtualTap".</span></span>

## <span data-ttu-id="9fc10-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9fc10-114">PARAMETERS</span></span>

### <span data-ttu-id="9fc10-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fc10-115">-DefaultProfile</span></span>
<span data-ttu-id="9fc10-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9fc10-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fc10-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="9fc10-117">-Name</span></span>
<span data-ttu-id="9fc10-118">Nome del tocco.</span><span class="sxs-lookup"><span data-stu-id="9fc10-118">The name of the tap.</span></span>

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

### <span data-ttu-id="9fc10-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fc10-119">-ResourceGroupName</span></span>
<span data-ttu-id="9fc10-120">Nome del gruppo di risorse del tocco di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9fc10-120">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="9fc10-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fc10-121">-ResourceId</span></span>
<span data-ttu-id="9fc10-122">ResourceId della risorsa VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="9fc10-122">ResourceId of the VirtualNetworkTap resource</span></span>

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

### <span data-ttu-id="9fc10-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9fc10-123">-Confirm</span></span>
<span data-ttu-id="9fc10-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fc10-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fc10-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fc10-125">-WhatIf</span></span>
<span data-ttu-id="9fc10-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9fc10-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9fc10-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9fc10-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fc10-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fc10-128">CommonParameters</span></span>
<span data-ttu-id="9fc10-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fc10-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fc10-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9fc10-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fc10-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9fc10-131">INPUTS</span></span>

### <span data-ttu-id="9fc10-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9fc10-132">System.String</span></span>

## <span data-ttu-id="9fc10-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9fc10-133">OUTPUTS</span></span>

### <span data-ttu-id="9fc10-134">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="9fc10-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="9fc10-135">Note</span><span class="sxs-lookup"><span data-stu-id="9fc10-135">NOTES</span></span>

## <span data-ttu-id="9fc10-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9fc10-136">RELATED LINKS</span></span>

[<span data-ttu-id="9fc10-137">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="9fc10-137">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="9fc10-138">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="9fc10-138">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="9fc10-139">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="9fc10-139">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)

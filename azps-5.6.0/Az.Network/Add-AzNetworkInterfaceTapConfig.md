---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 2da755a4ac3044c6499faee82a74e2c9ec7d9f6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982446"
---
# <span data-ttu-id="8d5e7-101">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8d5e7-101">Add-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="8d5e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d5e7-102">SYNOPSIS</span></span>
<span data-ttu-id="8d5e7-103">Crea una risorsa TapConfiguration associata a un oggetto NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="8d5e7-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="8d5e7-104">Questo fa riferimento a una risorsa VirtualNetworkTap esistente.</span><span class="sxs-lookup"><span data-stu-id="8d5e7-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="8d5e7-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8d5e7-105">SYNTAX</span></span>

### <span data-ttu-id="8d5e7-106">SetByResource (Default)</span><span class="sxs-lookup"><span data-stu-id="8d5e7-106">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d5e7-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8d5e7-107">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d5e7-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8d5e7-108">DESCRIPTION</span></span>
<span data-ttu-id="8d5e7-109">Il cmdlet **Add-AzNetworkInterfaceTapConfig crea** una risorsa TapConfiguration associata a un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="8d5e7-109">The **Add-AzNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="8d5e7-110">Questo fa riferimento a una risorsa VirtualNetworkTap esistente.</span><span class="sxs-lookup"><span data-stu-id="8d5e7-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="8d5e7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8d5e7-111">EXAMPLES</span></span>

### <span data-ttu-id="8d5e7-112">Esempio 1: Aggiungere TapConfiguration a un dato NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8d5e7-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="8d5e7-113">Aggiungere TapConfiguration a un sourceNic.</span><span class="sxs-lookup"><span data-stu-id="8d5e7-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="8d5e7-114">Il traffico da sourceNic VM verrà speculare alla macchina virtuale di destinazione a cui fa riferimento la risorsa vVirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="8d5e7-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="8d5e7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d5e7-115">PARAMETERS</span></span>

### <span data-ttu-id="8d5e7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d5e7-116">-DefaultProfile</span></span>
<span data-ttu-id="8d5e7-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8d5e7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d5e7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8d5e7-118">-Name</span></span>
<span data-ttu-id="8d5e7-119">Nome della configurazione di tocco.</span><span class="sxs-lookup"><span data-stu-id="8d5e7-119">Name of the tap configuration.</span></span>

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

### <span data-ttu-id="8d5e7-120">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8d5e7-120">-NetworkInterface</span></span>
<span data-ttu-id="8d5e7-121">Riferimento alla risorsa dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="8d5e7-121">The reference of the network interface resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d5e7-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8d5e7-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="8d5e7-123">Riferimento alla risorsa Tocco della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8d5e7-123">The reference of the virtual network tap resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d5e7-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="8d5e7-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="8d5e7-125">Riferimento alla risorsa Tocco della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8d5e7-125">The reference of the virtual network tap resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d5e7-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d5e7-126">-Confirm</span></span>
<span data-ttu-id="8d5e7-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d5e7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d5e7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d5e7-128">-WhatIf</span></span>
<span data-ttu-id="8d5e7-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8d5e7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d5e7-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8d5e7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d5e7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d5e7-131">CommonParameters</span></span>
<span data-ttu-id="8d5e7-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d5e7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d5e7-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d5e7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d5e7-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="8d5e7-134">INPUTS</span></span>

### <span data-ttu-id="8d5e7-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8d5e7-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="8d5e7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8d5e7-136">System.String</span></span>

### <span data-ttu-id="8d5e7-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8d5e7-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="8d5e7-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8d5e7-138">OUTPUTS</span></span>

### <span data-ttu-id="8d5e7-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8d5e7-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="8d5e7-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="8d5e7-140">NOTES</span></span>

## <span data-ttu-id="8d5e7-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8d5e7-141">RELATED LINKS</span></span>

[<span data-ttu-id="8d5e7-142">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8d5e7-142">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="8d5e7-143">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8d5e7-143">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="8d5e7-144">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8d5e7-144">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)

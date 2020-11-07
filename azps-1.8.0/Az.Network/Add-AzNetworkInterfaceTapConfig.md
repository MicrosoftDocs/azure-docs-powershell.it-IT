---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: c5c2481244de752a76eb1a1863d1fcc49d93ddb2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678658"
---
# <span data-ttu-id="d541d-101">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d541d-101">Add-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="d541d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d541d-102">SYNOPSIS</span></span>
<span data-ttu-id="d541d-103">Crea una risorsa TapConfiguration associata a un NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="d541d-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="d541d-104">Verrà fatto riferimento a una risorsa VirtualNetworkTap esistente.</span><span class="sxs-lookup"><span data-stu-id="d541d-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="d541d-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d541d-105">SYNTAX</span></span>

### <span data-ttu-id="d541d-106">SetByResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d541d-106">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d541d-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d541d-107">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d541d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d541d-108">DESCRIPTION</span></span>
<span data-ttu-id="d541d-109">Il cmdlet **Add-AzNetworkInterfaceTapConfig** crea una risorsa TapConfiguration associata a un NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="d541d-109">The **Add-AzNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="d541d-110">Verrà fatto riferimento a una risorsa VirtualNetworkTap esistente.</span><span class="sxs-lookup"><span data-stu-id="d541d-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="d541d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d541d-111">EXAMPLES</span></span>

### <span data-ttu-id="d541d-112">Esempio 1: aggiungere TapConfiguration a un NetworkInterface specifico</span><span class="sxs-lookup"><span data-stu-id="d541d-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="d541d-113">Aggiungere il TapConfiguration a un sourceNic.</span><span class="sxs-lookup"><span data-stu-id="d541d-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="d541d-114">Il traffico da sourceNic VM verrà speculato alla VM di destinazione di cui si fa riferimento nella risorsa vVirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="d541d-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="d541d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d541d-115">PARAMETERS</span></span>

### <span data-ttu-id="d541d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d541d-116">-DefaultProfile</span></span>
<span data-ttu-id="d541d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d541d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d541d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d541d-118">-Name</span></span>
<span data-ttu-id="d541d-119">Nome della configurazione del tocco.</span><span class="sxs-lookup"><span data-stu-id="d541d-119">Name of the tap configuration.</span></span>

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

### <span data-ttu-id="d541d-120">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d541d-120">-NetworkInterface</span></span>
<span data-ttu-id="d541d-121">Riferimento della risorsa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="d541d-121">The reference of the network interface resource.</span></span>

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

### <span data-ttu-id="d541d-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d541d-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="d541d-123">Riferimento della risorsa Virtual Network tap.</span><span class="sxs-lookup"><span data-stu-id="d541d-123">The reference of the virtual network tap resource.</span></span>

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

### <span data-ttu-id="d541d-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="d541d-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="d541d-125">Riferimento della risorsa Virtual Network tap.</span><span class="sxs-lookup"><span data-stu-id="d541d-125">The reference of the virtual network tap resource.</span></span>

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

### <span data-ttu-id="d541d-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d541d-126">-Confirm</span></span>
<span data-ttu-id="d541d-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d541d-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d541d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d541d-128">-WhatIf</span></span>
<span data-ttu-id="d541d-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d541d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d541d-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d541d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d541d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d541d-131">CommonParameters</span></span>
<span data-ttu-id="d541d-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d541d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d541d-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d541d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d541d-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d541d-134">INPUTS</span></span>

### <span data-ttu-id="d541d-135">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d541d-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="d541d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d541d-136">System.String</span></span>

### <span data-ttu-id="d541d-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d541d-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="d541d-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d541d-138">OUTPUTS</span></span>

### <span data-ttu-id="d541d-139">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d541d-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="d541d-140">Note</span><span class="sxs-lookup"><span data-stu-id="d541d-140">NOTES</span></span>

## <span data-ttu-id="d541d-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d541d-141">RELATED LINKS</span></span>

[<span data-ttu-id="d541d-142">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d541d-142">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="d541d-143">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d541d-143">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="d541d-144">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d541d-144">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)

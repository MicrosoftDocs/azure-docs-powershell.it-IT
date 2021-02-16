---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: b17f6e7245cb79a5b1098463e3c6dc0ca2b01c68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179847"
---
# <span data-ttu-id="d679f-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d679f-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="d679f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d679f-102">SYNOPSIS</span></span>
<span data-ttu-id="d679f-103">Ottiene un Gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="d679f-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="d679f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d679f-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d679f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d679f-105">DESCRIPTION</span></span>
<span data-ttu-id="d679f-106">Gateway di rete virtuale è l'oggetto che rappresenta il gateway in Azure.</span><span class="sxs-lookup"><span data-stu-id="d679f-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="d679f-107">Il cmdlet **Get-AzVirtualNetworkGateway** restituisce l'oggetto del gateway in Azure in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d679f-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="d679f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d679f-108">EXAMPLES</span></span>

### <span data-ttu-id="d679f-109">Esempio 1: Ottenere un Gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="d679f-109">Example 1: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="d679f-110">Restituisce l'oggetto di Gateway di rete virtuale con il nome "myGateway1" all'interno del gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="d679f-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="d679f-111">Esempio 2: Ottenere un Gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="d679f-111">Example 2: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="d679f-112">Restituisce tutti i gateway di rete virtuale che iniziano con "myGateway" all'interno del gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="d679f-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="d679f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d679f-113">PARAMETERS</span></span>

### <span data-ttu-id="d679f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d679f-114">-DefaultProfile</span></span>
<span data-ttu-id="d679f-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d679f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d679f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d679f-116">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d679f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d679f-117">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d679f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d679f-118">CommonParameters</span></span>
<span data-ttu-id="d679f-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d679f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d679f-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d679f-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d679f-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="d679f-121">INPUTS</span></span>

### <span data-ttu-id="d679f-122">System.String</span><span class="sxs-lookup"><span data-stu-id="d679f-122">System.String</span></span>

## <span data-ttu-id="d679f-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d679f-123">OUTPUTS</span></span>

### <span data-ttu-id="d679f-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d679f-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d679f-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="d679f-125">NOTES</span></span>

## <span data-ttu-id="d679f-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d679f-126">RELATED LINKS</span></span>

[<span data-ttu-id="d679f-127">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d679f-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d679f-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d679f-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d679f-129">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d679f-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d679f-130">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d679f-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d679f-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d679f-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

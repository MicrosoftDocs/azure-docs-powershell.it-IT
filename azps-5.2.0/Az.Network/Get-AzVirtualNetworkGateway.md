---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: b17f6e7245cb79a5b1098463e3c6dc0ca2b01c68
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356083"
---
# <span data-ttu-id="a7236-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a7236-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="a7236-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a7236-102">SYNOPSIS</span></span>
<span data-ttu-id="a7236-103">Ottiene un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a7236-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="a7236-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7236-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7236-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7236-105">DESCRIPTION</span></span>
<span data-ttu-id="a7236-106">Il gateway di rete virtuale è l'oggetto che rappresenta il gateway in Azure.</span><span class="sxs-lookup"><span data-stu-id="a7236-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="a7236-107">Il cmdlet **Get-AzVirtualNetworkGateway** restituisce l'oggetto del gateway in Azure in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a7236-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="a7236-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7236-108">EXAMPLES</span></span>

### <span data-ttu-id="a7236-109">Esempio 1: ottenere un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a7236-109">Example 1: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway1 -ResourceGroupName myRG
```

<span data-ttu-id="a7236-110">Restituisce l'oggetto del gateway di rete virtuale con il nome "myGateway1" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="a7236-110">Returns the object of the Virtual Network Gateway with the name "myGateway1" within the resource group "myRG"</span></span>

### <span data-ttu-id="a7236-111">Esempio 2: ottenere un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a7236-111">Example 2: Get a Virtual Network Gateway</span></span>
```powershell
Get-AzVirtualNetworkGateway -Name myGateway* -ResourceGroupName myRG
```

<span data-ttu-id="a7236-112">Restituisce tutti i gateway di rete virtuali che iniziano con "gateway" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="a7236-112">Returns all Virtual Network Gateways that start with "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="a7236-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a7236-113">PARAMETERS</span></span>

### <span data-ttu-id="a7236-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7236-114">-DefaultProfile</span></span>
<span data-ttu-id="a7236-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7236-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7236-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7236-116">-Name</span></span>
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

### <span data-ttu-id="a7236-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7236-117">-ResourceGroupName</span></span>
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

### <span data-ttu-id="a7236-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7236-118">CommonParameters</span></span>
<span data-ttu-id="a7236-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7236-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7236-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7236-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7236-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a7236-121">INPUTS</span></span>

### <span data-ttu-id="a7236-122">System. String</span><span class="sxs-lookup"><span data-stu-id="a7236-122">System.String</span></span>

## <span data-ttu-id="a7236-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7236-123">OUTPUTS</span></span>

### <span data-ttu-id="a7236-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a7236-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="a7236-125">Note</span><span class="sxs-lookup"><span data-stu-id="a7236-125">NOTES</span></span>

## <span data-ttu-id="a7236-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7236-126">RELATED LINKS</span></span>

[<span data-ttu-id="a7236-127">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a7236-127">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a7236-128">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a7236-128">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a7236-129">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a7236-129">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a7236-130">Ridimensionare-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a7236-130">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="a7236-131">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a7236-131">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)

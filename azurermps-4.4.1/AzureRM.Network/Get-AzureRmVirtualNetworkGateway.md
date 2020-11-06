---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: ed57a1832e3581d4d49b285fa9e61c93b17be02c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516951"
---
# <span data-ttu-id="fe140-101">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fe140-101">Get-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="fe140-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe140-102">SYNOPSIS</span></span>
<span data-ttu-id="fe140-103">Ottiene un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="fe140-103">Gets a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe140-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe140-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe140-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe140-105">DESCRIPTION</span></span>
<span data-ttu-id="fe140-106">Il gateway di rete virtuale è l'oggetto che rappresenta il gateway in Azure.</span><span class="sxs-lookup"><span data-stu-id="fe140-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="fe140-107">Il cmdlet **Get-AzureRmVirtualNetworkGateway** restituisce l'oggetto del gateway in Azure in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fe140-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="fe140-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe140-108">EXAMPLES</span></span>

### <span data-ttu-id="fe140-109">1: ottenere un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="fe140-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="fe140-110">Restituisce l'oggetto del gateway di rete virtuale con il nome "gateway" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="fe140-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="fe140-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe140-111">PARAMETERS</span></span>

### <span data-ttu-id="fe140-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe140-112">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe140-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe140-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="fe140-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe140-114">-DefaultProfile</span></span>
<span data-ttu-id="fe140-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fe140-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe140-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe140-116">CommonParameters</span></span>
<span data-ttu-id="fe140-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe140-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe140-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe140-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe140-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe140-119">INPUTS</span></span>

## <span data-ttu-id="fe140-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe140-120">OUTPUTS</span></span>

### <span data-ttu-id="fe140-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fe140-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="fe140-122">Note</span><span class="sxs-lookup"><span data-stu-id="fe140-122">NOTES</span></span>

## <span data-ttu-id="fe140-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe140-123">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9CBF592E-734B-4A0C-A45D-358C226D08C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGateway.md
ms.openlocfilehash: 490e61142bdbc0bcdd64f18aeeb2fa527e5180b9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860670"
---
# <span data-ttu-id="fbbb7-101">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fbbb7-101">Get-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="fbbb7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fbbb7-102">SYNOPSIS</span></span>
<span data-ttu-id="fbbb7-103">Ottiene un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="fbbb7-103">Gets a Virtual Network Gateway</span></span>

## <span data-ttu-id="fbbb7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fbbb7-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbbb7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbbb7-105">DESCRIPTION</span></span>
<span data-ttu-id="fbbb7-106">Il gateway di rete virtuale è l'oggetto che rappresenta il gateway in Azure.</span><span class="sxs-lookup"><span data-stu-id="fbbb7-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="fbbb7-107">Il cmdlet **Get-AzVirtualNetworkGateway** restituisce l'oggetto del gateway in Azure in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fbbb7-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="fbbb7-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fbbb7-108">EXAMPLES</span></span>

### <span data-ttu-id="fbbb7-109">1: ottenere un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="fbbb7-109">1: Get a Virtual Network Gateway</span></span>
```
Get-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="fbbb7-110">Restituisce l'oggetto del gateway di rete virtuale con il nome "gateway" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="fbbb7-110">Returns the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="fbbb7-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fbbb7-111">PARAMETERS</span></span>

### <span data-ttu-id="fbbb7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbbb7-112">-DefaultProfile</span></span>
<span data-ttu-id="fbbb7-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fbbb7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbbb7-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="fbbb7-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbbb7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbbb7-115">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbbb7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbbb7-116">CommonParameters</span></span>
<span data-ttu-id="fbbb7-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbbb7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbbb7-118">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbbb7-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbbb7-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fbbb7-119">INPUTS</span></span>

## <span data-ttu-id="fbbb7-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fbbb7-120">OUTPUTS</span></span>

### <span data-ttu-id="fbbb7-121">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fbbb7-121">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="fbbb7-122">Note</span><span class="sxs-lookup"><span data-stu-id="fbbb7-122">NOTES</span></span>

## <span data-ttu-id="fbbb7-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fbbb7-123">RELATED LINKS</span></span>


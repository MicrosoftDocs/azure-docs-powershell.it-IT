---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: 0179a033d9cc99ff2f373dbaceb1bcb97ab3468f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006174"
---
# <span data-ttu-id="0743c-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="0743c-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="0743c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0743c-102">SYNOPSIS</span></span>
<span data-ttu-id="0743c-103">Definire una SKU Appliance virtuale di rete per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0743c-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="0743c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0743c-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0743c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0743c-105">DESCRIPTION</span></span>
<span data-ttu-id="0743c-106">Il New-AzVirtualApplianceSkuProperties di ricerca definisce una SKU per la risorsa Appliance virtuale di rete.</span><span class="sxs-lookup"><span data-stu-id="0743c-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="0743c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0743c-107">EXAMPLES</span></span>

### <span data-ttu-id="0743c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0743c-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="0743c-109">Creare un oggetto Proprietà SKU dell'appliance virtuale da usare con New-AzNetworkVirtualAppliance virtuale.</span><span class="sxs-lookup"><span data-stu-id="0743c-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="0743c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0743c-110">PARAMETERS</span></span>

### <span data-ttu-id="0743c-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="0743c-111">-BundledScaleUnit</span></span>
<span data-ttu-id="0743c-112">L'unità di scala in bundle.</span><span class="sxs-lookup"><span data-stu-id="0743c-112">The bundled scale unit.</span></span>

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

### <span data-ttu-id="0743c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0743c-113">-DefaultProfile</span></span>
<span data-ttu-id="0743c-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0743c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0743c-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="0743c-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="0743c-116">Versione sul mercato.</span><span class="sxs-lookup"><span data-stu-id="0743c-116">The market place version.</span></span>

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

### <span data-ttu-id="0743c-117">-VendorName</span><span class="sxs-lookup"><span data-stu-id="0743c-117">-VendorName</span></span>
<span data-ttu-id="0743c-118">Nome del fornitore.</span><span class="sxs-lookup"><span data-stu-id="0743c-118">The name of the vendor.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0743c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0743c-119">CommonParameters</span></span>
<span data-ttu-id="0743c-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0743c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0743c-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0743c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0743c-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="0743c-122">INPUTS</span></span>

### <span data-ttu-id="0743c-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0743c-123">None</span></span>

## <span data-ttu-id="0743c-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0743c-124">OUTPUTS</span></span>

### <span data-ttu-id="0743c-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="0743c-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="0743c-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="0743c-126">NOTES</span></span>

## <span data-ttu-id="0743c-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0743c-127">RELATED LINKS</span></span>

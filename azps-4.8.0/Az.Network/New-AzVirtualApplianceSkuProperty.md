---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: cfe9fb07854fcc5850e1c5f73f4da7fe43f172a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189510"
---
# <span data-ttu-id="1e4e7-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="1e4e7-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="1e4e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1e4e7-102">SYNOPSIS</span></span>
<span data-ttu-id="1e4e7-103">Definire una SKU di Virtual Appliance di rete per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="1e4e7-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="1e4e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e4e7-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e4e7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e4e7-105">DESCRIPTION</span></span>
<span data-ttu-id="1e4e7-106">Il comando New-AzVirtualApplianceSkuProperties definisce un SKU per la risorsa Virtual Appliance di rete.</span><span class="sxs-lookup"><span data-stu-id="1e4e7-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="1e4e7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e4e7-107">EXAMPLES</span></span>

### <span data-ttu-id="1e4e7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1e4e7-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="1e4e7-109">Creare un oggetto delle proprietà SKU di Virtual Appliance da usare con il comando New-AzNetworkVirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="1e4e7-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="1e4e7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1e4e7-110">PARAMETERS</span></span>

### <span data-ttu-id="1e4e7-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="1e4e7-111">-BundledScaleUnit</span></span>
<span data-ttu-id="1e4e7-112">Unità di scala in bundle.</span><span class="sxs-lookup"><span data-stu-id="1e4e7-112">The bundled scale unit.</span></span>

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

### <span data-ttu-id="1e4e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e4e7-113">-DefaultProfile</span></span>
<span data-ttu-id="1e4e7-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e4e7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e4e7-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="1e4e7-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="1e4e7-116">Versione Market Place.</span><span class="sxs-lookup"><span data-stu-id="1e4e7-116">The market place version.</span></span>

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

### <span data-ttu-id="1e4e7-117">-VendorName</span><span class="sxs-lookup"><span data-stu-id="1e4e7-117">-VendorName</span></span>
<span data-ttu-id="1e4e7-118">Nome del fornitore.</span><span class="sxs-lookup"><span data-stu-id="1e4e7-118">The name of the vendor.</span></span>

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

### <span data-ttu-id="1e4e7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e4e7-119">CommonParameters</span></span>
<span data-ttu-id="1e4e7-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e4e7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e4e7-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e4e7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e4e7-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1e4e7-122">INPUTS</span></span>

### <span data-ttu-id="1e4e7-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1e4e7-123">None</span></span>

## <span data-ttu-id="1e4e7-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e4e7-124">OUTPUTS</span></span>

### <span data-ttu-id="1e4e7-125">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="1e4e7-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="1e4e7-126">Note</span><span class="sxs-lookup"><span data-stu-id="1e4e7-126">NOTES</span></span>

## <span data-ttu-id="1e4e7-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e4e7-127">RELATED LINKS</span></span>
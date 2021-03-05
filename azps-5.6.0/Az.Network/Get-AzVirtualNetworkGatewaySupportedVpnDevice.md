---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 45cb703d6fdc87238f4d1ed35ada90aadeed501b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987809"
---
# <span data-ttu-id="13288-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="13288-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="13288-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13288-102">SYNOPSIS</span></span>
<span data-ttu-id="13288-103">Questo commandlet restituisce un elenco di marche, modelli e versioni del firmware supportati per i dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="13288-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="13288-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13288-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13288-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="13288-105">DESCRIPTION</span></span>
<span data-ttu-id="13288-106">Questo commandlet restituisce un elenco di marche, modelli e versioni del firmware supportati per i dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="13288-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="13288-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13288-107">EXAMPLES</span></span>

### <span data-ttu-id="13288-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="13288-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway 
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>
```

<span data-ttu-id="13288-109">Restituisce l'elenco dei marchi, dei modelli e delle versioni del firmware supportati per i dispositivi VPN:</span><span class="sxs-lookup"><span data-stu-id="13288-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="13288-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13288-110">PARAMETERS</span></span>

### <span data-ttu-id="13288-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13288-111">-DefaultProfile</span></span>
<span data-ttu-id="13288-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="13288-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13288-113">-Name</span><span class="sxs-lookup"><span data-stu-id="13288-113">-Name</span></span>
<span data-ttu-id="13288-114">Nome del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="13288-114">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13288-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13288-115">-ResourceGroupName</span></span>
<span data-ttu-id="13288-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="13288-116">The resource group name.</span></span>

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

### <span data-ttu-id="13288-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13288-117">CommonParameters</span></span>
<span data-ttu-id="13288-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13288-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13288-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="13288-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13288-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="13288-120">INPUTS</span></span>

### <span data-ttu-id="13288-121">System.String</span><span class="sxs-lookup"><span data-stu-id="13288-121">System.String</span></span>

## <span data-ttu-id="13288-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13288-122">OUTPUTS</span></span>

### <span data-ttu-id="13288-123">System.String</span><span class="sxs-lookup"><span data-stu-id="13288-123">System.String</span></span>

## <span data-ttu-id="13288-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="13288-124">NOTES</span></span>

## <span data-ttu-id="13288-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13288-125">RELATED LINKS</span></span>

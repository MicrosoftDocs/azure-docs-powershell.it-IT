---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
ms.openlocfilehash: 46eccff9ad7b4fc525a864eab4c4477df4503dc2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866279"
---
# <span data-ttu-id="15e5d-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="15e5d-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="15e5d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="15e5d-102">SYNOPSIS</span></span>
<span data-ttu-id="15e5d-103">Questo unifiedgroup restituisce un elenco di marchi, modelli e versioni del firmware supportati per i dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="15e5d-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15e5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15e5d-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15e5d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15e5d-105">DESCRIPTION</span></span>
<span data-ttu-id="15e5d-106">Questo unifiedgroup restituisce un elenco di marchi, modelli e versioni del firmware supportati per i dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="15e5d-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="15e5d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15e5d-107">EXAMPLES</span></span>

### <span data-ttu-id="15e5d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="15e5d-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway 
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>
```

<span data-ttu-id="15e5d-109">Restituisce un elenco di marchi, modelli e versioni del firmware supportati per i dispositivi VPN:</span><span class="sxs-lookup"><span data-stu-id="15e5d-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="15e5d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="15e5d-110">PARAMETERS</span></span>

### <span data-ttu-id="15e5d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15e5d-111">-DefaultProfile</span></span>
<span data-ttu-id="15e5d-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="15e5d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15e5d-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="15e5d-113">-Name</span></span>
<span data-ttu-id="15e5d-114">Nome del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="15e5d-114">The virtual network gateway name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e5d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15e5d-115">-ResourceGroupName</span></span>
<span data-ttu-id="15e5d-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="15e5d-116">The resource group name.</span></span>

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

### <span data-ttu-id="15e5d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15e5d-117">CommonParameters</span></span>
<span data-ttu-id="15e5d-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15e5d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15e5d-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15e5d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15e5d-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="15e5d-120">INPUTS</span></span>

### <span data-ttu-id="15e5d-121">System. String</span><span class="sxs-lookup"><span data-stu-id="15e5d-121">System.String</span></span>

## <span data-ttu-id="15e5d-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15e5d-122">OUTPUTS</span></span>

### <span data-ttu-id="15e5d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="15e5d-123">System.String</span></span>

## <span data-ttu-id="15e5d-124">Note</span><span class="sxs-lookup"><span data-stu-id="15e5d-124">NOTES</span></span>

## <span data-ttu-id="15e5d-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15e5d-125">RELATED LINKS</span></span>


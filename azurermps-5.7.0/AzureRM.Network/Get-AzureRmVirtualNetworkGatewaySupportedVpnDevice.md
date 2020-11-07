---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 30937c856d1961a1f342c73588aa00c74790ec81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686095"
---
# <span data-ttu-id="96f8f-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="96f8f-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="96f8f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96f8f-102">SYNOPSIS</span></span>
<span data-ttu-id="96f8f-103">Questo unifiedgroup restituisce un elenco di marchi, modelli e versioni del firmware supportati per i dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="96f8f-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96f8f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96f8f-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96f8f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96f8f-105">DESCRIPTION</span></span>
<span data-ttu-id="96f8f-106">Questo unifiedgroup restituisce un elenco di marchi, modelli e versioni del firmware supportati per i dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="96f8f-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="96f8f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96f8f-107">EXAMPLES</span></span>

### <span data-ttu-id="96f8f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="96f8f-108">Example 1</span></span>
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

<span data-ttu-id="96f8f-109">Restituisce un elenco di marchi, modelli e versioni del firmware supportati per i dispositivi VPN:</span><span class="sxs-lookup"><span data-stu-id="96f8f-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="96f8f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96f8f-110">PARAMETERS</span></span>

### <span data-ttu-id="96f8f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96f8f-111">-DefaultProfile</span></span>
<span data-ttu-id="96f8f-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="96f8f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96f8f-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="96f8f-113">-Name</span></span>
<span data-ttu-id="96f8f-114">Nome del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="96f8f-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="96f8f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96f8f-115">-ResourceGroupName</span></span>
<span data-ttu-id="96f8f-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="96f8f-116">The resource group name.</span></span>

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

### <span data-ttu-id="96f8f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96f8f-117">CommonParameters</span></span>
<span data-ttu-id="96f8f-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96f8f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96f8f-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96f8f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96f8f-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96f8f-120">INPUTS</span></span>

### <span data-ttu-id="96f8f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="96f8f-121">System.String</span></span>

## <span data-ttu-id="96f8f-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96f8f-122">OUTPUTS</span></span>

### <span data-ttu-id="96f8f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="96f8f-123">System.String</span></span>

## <span data-ttu-id="96f8f-124">Note</span><span class="sxs-lookup"><span data-stu-id="96f8f-124">NOTES</span></span>

## <span data-ttu-id="96f8f-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96f8f-125">RELATED LINKS</span></span>


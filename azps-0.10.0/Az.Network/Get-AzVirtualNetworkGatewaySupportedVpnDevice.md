---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 794f432b06c693d6758603975a98ca6b2f5e3511
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860641"
---
# <span data-ttu-id="db93e-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="db93e-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="db93e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db93e-102">SYNOPSIS</span></span>
<span data-ttu-id="db93e-103">Questo unifiedgroup restituisce un elenco di marchi, modelli e versioni del firmware supportati per i dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="db93e-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="db93e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db93e-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db93e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db93e-105">DESCRIPTION</span></span>
<span data-ttu-id="db93e-106">Questo unifiedgroup restituisce un elenco di marchi, modelli e versioni del firmware supportati per i dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="db93e-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="db93e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db93e-107">EXAMPLES</span></span>

### <span data-ttu-id="db93e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="db93e-108">Example 1</span></span>
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

<span data-ttu-id="db93e-109">Restituisce un elenco di marchi, modelli e versioni del firmware supportati per i dispositivi VPN:</span><span class="sxs-lookup"><span data-stu-id="db93e-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="db93e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db93e-110">PARAMETERS</span></span>

### <span data-ttu-id="db93e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db93e-111">-DefaultProfile</span></span>
<span data-ttu-id="db93e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db93e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db93e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="db93e-113">-Name</span></span>
<span data-ttu-id="db93e-114">Nome del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="db93e-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="db93e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db93e-115">-ResourceGroupName</span></span>
<span data-ttu-id="db93e-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="db93e-116">The resource group name.</span></span>

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

### <span data-ttu-id="db93e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db93e-117">CommonParameters</span></span>
<span data-ttu-id="db93e-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db93e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db93e-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db93e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db93e-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db93e-120">INPUTS</span></span>

### <span data-ttu-id="db93e-121">System. String</span><span class="sxs-lookup"><span data-stu-id="db93e-121">System.String</span></span>

## <span data-ttu-id="db93e-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db93e-122">OUTPUTS</span></span>

### <span data-ttu-id="db93e-123">System. String</span><span class="sxs-lookup"><span data-stu-id="db93e-123">System.String</span></span>

## <span data-ttu-id="db93e-124">Note</span><span class="sxs-lookup"><span data-stu-id="db93e-124">NOTES</span></span>

## <span data-ttu-id="db93e-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db93e-125">RELATED LINKS</span></span>


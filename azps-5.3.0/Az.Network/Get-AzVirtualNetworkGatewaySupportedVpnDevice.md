---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: f643b280e0777f3251380ecf36f4fcc070b545c1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380992"
---
# <span data-ttu-id="4b491-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="4b491-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="4b491-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4b491-102">SYNOPSIS</span></span>
<span data-ttu-id="4b491-103">Questo unifiedgroup restituisce un elenco di marchi, modelli e versioni del firmware supportati per i dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="4b491-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="4b491-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b491-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b491-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b491-105">DESCRIPTION</span></span>
<span data-ttu-id="4b491-106">Questo unifiedgroup restituisce un elenco di marchi, modelli e versioni del firmware supportati per i dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="4b491-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="4b491-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b491-107">EXAMPLES</span></span>

### <span data-ttu-id="4b491-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4b491-108">Example 1</span></span>
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

<span data-ttu-id="4b491-109">Restituisce un elenco di marchi, modelli e versioni del firmware supportati per i dispositivi VPN:</span><span class="sxs-lookup"><span data-stu-id="4b491-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="4b491-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4b491-110">PARAMETERS</span></span>

### <span data-ttu-id="4b491-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b491-111">-DefaultProfile</span></span>
<span data-ttu-id="4b491-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4b491-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b491-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b491-113">-Name</span></span>
<span data-ttu-id="4b491-114">Nome del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="4b491-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="4b491-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b491-115">-ResourceGroupName</span></span>
<span data-ttu-id="4b491-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4b491-116">The resource group name.</span></span>

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

### <span data-ttu-id="4b491-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b491-117">CommonParameters</span></span>
<span data-ttu-id="4b491-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b491-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b491-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b491-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b491-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4b491-120">INPUTS</span></span>

### <span data-ttu-id="4b491-121">System. String</span><span class="sxs-lookup"><span data-stu-id="4b491-121">System.String</span></span>

## <span data-ttu-id="4b491-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b491-122">OUTPUTS</span></span>

### <span data-ttu-id="4b491-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4b491-123">System.String</span></span>

## <span data-ttu-id="4b491-124">Note</span><span class="sxs-lookup"><span data-stu-id="4b491-124">NOTES</span></span>

## <span data-ttu-id="4b491-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b491-125">RELATED LINKS</span></span>

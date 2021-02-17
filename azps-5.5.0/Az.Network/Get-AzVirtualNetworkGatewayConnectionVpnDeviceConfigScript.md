---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 5421c33c4858c99be4dd84ba7f0c1bff401e1182
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184646"
---
# <span data-ttu-id="d3cae-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="d3cae-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="d3cae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3cae-102">SYNOPSIS</span></span>
<span data-ttu-id="d3cae-103">Questo commandlet prende la risorsa di connessione, il marchio del dispositivo VPN, il modello, la versione del firmware e restituisce lo script di configurazione corrispondente che i clienti possono applicare direttamente sui loro dispositivi VPN locali.</span><span class="sxs-lookup"><span data-stu-id="d3cae-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="d3cae-104">Lo script segue la sintassi del dispositivo selezionato e inserisce i parametri necessari, ad esempio gli indirizzi IP pubblici del gateway di Azure, i prefissi degli indirizzi di rete virtuale, la chiave precondi condivisione tunnel VPN e così via, in modo che i clienti possano semplicemente copiare e incollare nelle configurazioni di dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="d3cae-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="d3cae-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3cae-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3cae-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d3cae-106">DESCRIPTION</span></span>
<span data-ttu-id="d3cae-107">Questo commandlet prende la risorsa di connessione, il marchio del dispositivo VPN, il modello, la versione del firmware e restituisce lo script di configurazione corrispondente che i clienti possono applicare direttamente sui loro dispositivi VPN locali.</span><span class="sxs-lookup"><span data-stu-id="d3cae-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="d3cae-108">Lo script segue la sintassi del dispositivo selezionato e inserisce i parametri necessari, ad esempio gli indirizzi IP pubblici del gateway di Azure, i prefissi degli indirizzi di rete virtuale, la chiave precondi condivisione tunnel VPN e così via, in modo che i clienti possano semplicemente copiare e incollare nelle configurazioni di dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="d3cae-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="d3cae-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3cae-109">EXAMPLES</span></span>

### <span data-ttu-id="d3cae-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d3cae-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="d3cae-111">L'esempio precedente usa Get-AzVirtualNetworkGatewaySupportedVpnDevice per ottenere i marchi, i modelli e le versioni del firmware supportati per dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="d3cae-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="d3cae-112">Usa quindi uno dei modelli restituiti per generare uno script di configurazione del dispositivo VPN per VirtualNetworkGatewayConnection "TestConnection".</span><span class="sxs-lookup"><span data-stu-id="d3cae-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="d3cae-113">Il dispositivo usato in questo esempio ha DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" e FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="d3cae-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="d3cae-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3cae-114">PARAMETERS</span></span>

### <span data-ttu-id="d3cae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3cae-115">-DefaultProfile</span></span>
<span data-ttu-id="d3cae-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3cae-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3cae-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="d3cae-117">-DeviceFamily</span></span>
<span data-ttu-id="d3cae-118">Nome del modello/famiglia di dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="d3cae-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="d3cae-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="d3cae-119">-DeviceVendor</span></span>
<span data-ttu-id="d3cae-120">Nome del fornitore di dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="d3cae-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="d3cae-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="d3cae-121">-FirmwareVersion</span></span>
<span data-ttu-id="d3cae-122">Versione firmware del dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="d3cae-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="d3cae-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d3cae-123">-Name</span></span>
<span data-ttu-id="d3cae-124">Nome della risorsa della connessione per cui deve essere generata la configurazione.</span><span class="sxs-lookup"><span data-stu-id="d3cae-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="d3cae-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3cae-125">-ResourceGroupName</span></span>
<span data-ttu-id="d3cae-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d3cae-126">The resource group name.</span></span>

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

### <span data-ttu-id="d3cae-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3cae-127">-Confirm</span></span>
<span data-ttu-id="d3cae-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3cae-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3cae-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3cae-129">-WhatIf</span></span>
<span data-ttu-id="d3cae-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3cae-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3cae-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3cae-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3cae-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3cae-132">CommonParameters</span></span>
<span data-ttu-id="d3cae-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3cae-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3cae-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d3cae-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3cae-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="d3cae-135">INPUTS</span></span>

### <span data-ttu-id="d3cae-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d3cae-136">System.String</span></span>

## <span data-ttu-id="d3cae-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3cae-137">OUTPUTS</span></span>

### <span data-ttu-id="d3cae-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d3cae-138">System.String</span></span>

## <span data-ttu-id="d3cae-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="d3cae-139">NOTES</span></span>

## <span data-ttu-id="d3cae-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3cae-140">RELATED LINKS</span></span>

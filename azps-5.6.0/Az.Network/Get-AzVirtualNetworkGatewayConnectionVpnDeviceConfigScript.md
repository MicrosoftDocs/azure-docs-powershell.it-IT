---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 967e45ce124ead583a7c2f3e36a80dedb80d4e20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978286"
---
# <span data-ttu-id="301f9-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="301f9-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="301f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="301f9-102">SYNOPSIS</span></span>
<span data-ttu-id="301f9-103">Questo commandlet prende la risorsa di connessione, il marchio del dispositivo VPN, il modello, la versione del firmware e restituisce lo script di configurazione corrispondente che i clienti possono applicare direttamente sui loro dispositivi VPN locali.</span><span class="sxs-lookup"><span data-stu-id="301f9-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="301f9-104">Lo script segue la sintassi del dispositivo selezionato e inserisce i parametri necessari, ad esempio gli indirizzi IP pubblici del gateway di Azure, i prefissi degli indirizzi di rete virtuale, la chiave precondi condivisione tunnel VPN e così via, in modo che i clienti possano semplicemente copiare e incollare nella propria configurazione di dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="301f9-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="301f9-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="301f9-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="301f9-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="301f9-106">DESCRIPTION</span></span>
<span data-ttu-id="301f9-107">Questo commandlet prende la risorsa di connessione, il marchio del dispositivo VPN, il modello, la versione del firmware e restituisce lo script di configurazione corrispondente che i clienti possono applicare direttamente sui loro dispositivi VPN locali.</span><span class="sxs-lookup"><span data-stu-id="301f9-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="301f9-108">Lo script segue la sintassi del dispositivo selezionato e inserisce i parametri necessari, ad esempio gli indirizzi IP pubblici del gateway di Azure, i prefissi degli indirizzi di rete virtuale, la chiave precondi condivisione tunnel VPN e così via, in modo che i clienti possano semplicemente copiare e incollare nella propria configurazione di dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="301f9-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="301f9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="301f9-109">EXAMPLES</span></span>

### <span data-ttu-id="301f9-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="301f9-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="301f9-111">L'esempio precedente usa Get-AzVirtualNetworkGatewaySupportedVpnDevice per ottenere i marchi, i modelli e le versioni del firmware supportati per dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="301f9-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="301f9-112">Usa quindi una delle informazioni dei modelli restituiti per generare uno script di configurazione del dispositivo VPN per VirtualNetworkGatewayConnection "TestConnection".</span><span class="sxs-lookup"><span data-stu-id="301f9-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="301f9-113">Il dispositivo usato in questo esempio ha DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" e FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="301f9-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="301f9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="301f9-114">PARAMETERS</span></span>

### <span data-ttu-id="301f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="301f9-115">-DefaultProfile</span></span>
<span data-ttu-id="301f9-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="301f9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="301f9-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="301f9-117">-DeviceFamily</span></span>
<span data-ttu-id="301f9-118">Nome del modello/famiglia di dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="301f9-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="301f9-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="301f9-119">-DeviceVendor</span></span>
<span data-ttu-id="301f9-120">Nome del fornitore di dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="301f9-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="301f9-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="301f9-121">-FirmwareVersion</span></span>
<span data-ttu-id="301f9-122">Versione firmware del dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="301f9-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="301f9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="301f9-123">-Name</span></span>
<span data-ttu-id="301f9-124">Nome della risorsa della connessione per cui deve essere generata la configurazione.</span><span class="sxs-lookup"><span data-stu-id="301f9-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="301f9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="301f9-125">-ResourceGroupName</span></span>
<span data-ttu-id="301f9-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="301f9-126">The resource group name.</span></span>

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

### <span data-ttu-id="301f9-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="301f9-127">-Confirm</span></span>
<span data-ttu-id="301f9-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="301f9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="301f9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="301f9-129">-WhatIf</span></span>
<span data-ttu-id="301f9-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="301f9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="301f9-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="301f9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="301f9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="301f9-132">CommonParameters</span></span>
<span data-ttu-id="301f9-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="301f9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="301f9-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="301f9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="301f9-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="301f9-135">INPUTS</span></span>

### <span data-ttu-id="301f9-136">System.String</span><span class="sxs-lookup"><span data-stu-id="301f9-136">System.String</span></span>

## <span data-ttu-id="301f9-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="301f9-137">OUTPUTS</span></span>

### <span data-ttu-id="301f9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="301f9-138">System.String</span></span>

## <span data-ttu-id="301f9-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="301f9-139">NOTES</span></span>

## <span data-ttu-id="301f9-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="301f9-140">RELATED LINKS</span></span>

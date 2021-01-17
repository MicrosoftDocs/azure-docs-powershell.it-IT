---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 5421c33c4858c99be4dd84ba7f0c1bff401e1182
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486747"
---
# <span data-ttu-id="9e7d2-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="9e7d2-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="9e7d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e7d2-102">SYNOPSIS</span></span>
<span data-ttu-id="9e7d2-103">Questo unifiedgroup accetta la risorsa di connessione, la marca del dispositivo VPN, il modello, la versione del firmware e restituisce lo script di configurazione corrispondente che i clienti possono applicare direttamente ai loro dispositivi VPN locali.</span><span class="sxs-lookup"><span data-stu-id="9e7d2-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="9e7d2-104">Lo script seguirà la sintassi del dispositivo selezionato e compilerà i parametri necessari, ad esempio gli indirizzi IP pubblici di Azure gateway, i prefissi degli indirizzi di rete virtuali, la chiave pre-condivisa del tunnel VPN e così via, quindi i clienti possono semplicemente copiare e incollare le configurazioni dei dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="9e7d2-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="9e7d2-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e7d2-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e7d2-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e7d2-106">DESCRIPTION</span></span>
<span data-ttu-id="9e7d2-107">Questo unifiedgroup accetta la risorsa di connessione, la marca del dispositivo VPN, il modello, la versione del firmware e restituisce lo script di configurazione corrispondente che i clienti possono applicare direttamente ai loro dispositivi VPN locali.</span><span class="sxs-lookup"><span data-stu-id="9e7d2-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="9e7d2-108">Lo script seguirà la sintassi del dispositivo selezionato e compilerà i parametri necessari, ad esempio gli indirizzi IP pubblici di Azure gateway, i prefissi degli indirizzi di rete virtuali, la chiave pre-condivisa del tunnel VPN e così via, quindi i clienti possono semplicemente copiare e incollare le configurazioni dei dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="9e7d2-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="9e7d2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e7d2-109">EXAMPLES</span></span>

### <span data-ttu-id="9e7d2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9e7d2-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="9e7d2-111">L'esempio precedente USA Get-AzVirtualNetworkGatewaySupportedVpnDevice per ottenere i marchi, i modelli e le versioni del firmware supportati per i dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="9e7d2-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="9e7d2-112">USA quindi una delle informazioni sui modelli restituiti per generare uno script di configurazione dei dispositivi VPN per il VirtualNetworkGatewayConnection "TestConnection".</span><span class="sxs-lookup"><span data-stu-id="9e7d2-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="9e7d2-113">Il dispositivo usato in questo esempio è DeviceFamily "IOS-test", DeviceVendor "Cisco-test" e FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="9e7d2-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="9e7d2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e7d2-114">PARAMETERS</span></span>

### <span data-ttu-id="9e7d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e7d2-115">-DefaultProfile</span></span>
<span data-ttu-id="9e7d2-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e7d2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e7d2-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="9e7d2-117">-DeviceFamily</span></span>
<span data-ttu-id="9e7d2-118">Nome del modello/famiglia di dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="9e7d2-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="9e7d2-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="9e7d2-119">-DeviceVendor</span></span>
<span data-ttu-id="9e7d2-120">Nome del fornitore di dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="9e7d2-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="9e7d2-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="9e7d2-121">-FirmwareVersion</span></span>
<span data-ttu-id="9e7d2-122">Versione del firmware del dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="9e7d2-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="9e7d2-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e7d2-123">-Name</span></span>
<span data-ttu-id="9e7d2-124">Il nome della risorsa della connessione per cui deve essere generata la configurazione.</span><span class="sxs-lookup"><span data-stu-id="9e7d2-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="9e7d2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e7d2-125">-ResourceGroupName</span></span>
<span data-ttu-id="9e7d2-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9e7d2-126">The resource group name.</span></span>

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

### <span data-ttu-id="9e7d2-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9e7d2-127">-Confirm</span></span>
<span data-ttu-id="9e7d2-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e7d2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e7d2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e7d2-129">-WhatIf</span></span>
<span data-ttu-id="9e7d2-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e7d2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e7d2-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e7d2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e7d2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e7d2-132">CommonParameters</span></span>
<span data-ttu-id="9e7d2-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e7d2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e7d2-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e7d2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e7d2-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e7d2-135">INPUTS</span></span>

### <span data-ttu-id="9e7d2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9e7d2-136">System.String</span></span>

## <span data-ttu-id="9e7d2-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e7d2-137">OUTPUTS</span></span>

### <span data-ttu-id="9e7d2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9e7d2-138">System.String</span></span>

## <span data-ttu-id="9e7d2-139">Note</span><span class="sxs-lookup"><span data-stu-id="9e7d2-139">NOTES</span></span>

## <span data-ttu-id="9e7d2-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e7d2-140">RELATED LINKS</span></span>

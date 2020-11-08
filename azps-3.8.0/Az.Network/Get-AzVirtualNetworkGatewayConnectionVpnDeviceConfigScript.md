---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 5421c33c4858c99be4dd84ba7f0c1bff401e1182
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019581"
---
# <span data-ttu-id="50751-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="50751-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="50751-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50751-102">SYNOPSIS</span></span>
<span data-ttu-id="50751-103">Questo unifiedgroup accetta la risorsa di connessione, la marca del dispositivo VPN, il modello, la versione del firmware e restituisce lo script di configurazione corrispondente che i clienti possono applicare direttamente ai loro dispositivi VPN locali.</span><span class="sxs-lookup"><span data-stu-id="50751-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="50751-104">Lo script seguirà la sintassi del dispositivo selezionato e compilerà i parametri necessari, ad esempio gli indirizzi IP pubblici di Azure gateway, i prefissi degli indirizzi di rete virtuali, la chiave pre-condivisa del tunnel VPN e così via, quindi i clienti possono semplicemente copiare e incollare le configurazioni dei dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="50751-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="50751-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50751-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50751-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50751-106">DESCRIPTION</span></span>
<span data-ttu-id="50751-107">Questo unifiedgroup accetta la risorsa di connessione, la marca del dispositivo VPN, il modello, la versione del firmware e restituisce lo script di configurazione corrispondente che i clienti possono applicare direttamente ai loro dispositivi VPN locali.</span><span class="sxs-lookup"><span data-stu-id="50751-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="50751-108">Lo script seguirà la sintassi del dispositivo selezionato e compilerà i parametri necessari, ad esempio gli indirizzi IP pubblici di Azure gateway, i prefissi degli indirizzi di rete virtuali, la chiave pre-condivisa del tunnel VPN e così via, quindi i clienti possono semplicemente copiare e incollare le configurazioni dei dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="50751-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="50751-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50751-109">EXAMPLES</span></span>

### <span data-ttu-id="50751-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="50751-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="50751-111">L'esempio precedente USA Get-AzVirtualNetworkGatewaySupportedVpnDevice per ottenere i marchi, i modelli e le versioni del firmware supportati per i dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="50751-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="50751-112">USA quindi una delle informazioni sui modelli restituiti per generare uno script di configurazione dei dispositivi VPN per il VirtualNetworkGatewayConnection "TestConnection".</span><span class="sxs-lookup"><span data-stu-id="50751-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="50751-113">Il dispositivo usato in questo esempio è DeviceFamily "IOS-test", DeviceVendor "Cisco-test" e FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="50751-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="50751-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50751-114">PARAMETERS</span></span>

### <span data-ttu-id="50751-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50751-115">-DefaultProfile</span></span>
<span data-ttu-id="50751-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50751-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50751-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="50751-117">-DeviceFamily</span></span>
<span data-ttu-id="50751-118">Nome del modello/famiglia di dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="50751-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="50751-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="50751-119">-DeviceVendor</span></span>
<span data-ttu-id="50751-120">Nome del fornitore di dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="50751-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="50751-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="50751-121">-FirmwareVersion</span></span>
<span data-ttu-id="50751-122">Versione del firmware del dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="50751-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="50751-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="50751-123">-Name</span></span>
<span data-ttu-id="50751-124">Il nome della risorsa della connessione per cui deve essere generata la configurazione.</span><span class="sxs-lookup"><span data-stu-id="50751-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="50751-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50751-125">-ResourceGroupName</span></span>
<span data-ttu-id="50751-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="50751-126">The resource group name.</span></span>

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

### <span data-ttu-id="50751-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="50751-127">-Confirm</span></span>
<span data-ttu-id="50751-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50751-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50751-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50751-129">-WhatIf</span></span>
<span data-ttu-id="50751-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50751-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50751-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50751-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50751-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50751-132">CommonParameters</span></span>
<span data-ttu-id="50751-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50751-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50751-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50751-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50751-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50751-135">INPUTS</span></span>

### <span data-ttu-id="50751-136">System. String</span><span class="sxs-lookup"><span data-stu-id="50751-136">System.String</span></span>

## <span data-ttu-id="50751-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50751-137">OUTPUTS</span></span>

### <span data-ttu-id="50751-138">System. String</span><span class="sxs-lookup"><span data-stu-id="50751-138">System.String</span></span>

## <span data-ttu-id="50751-139">Note</span><span class="sxs-lookup"><span data-stu-id="50751-139">NOTES</span></span>

## <span data-ttu-id="50751-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50751-140">RELATED LINKS</span></span>

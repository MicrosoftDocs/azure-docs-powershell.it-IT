---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 5421c33c4858c99be4dd84ba7f0c1bff401e1182
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335620"
---
# <span data-ttu-id="f8481-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="f8481-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="f8481-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8481-102">SYNOPSIS</span></span>
<span data-ttu-id="f8481-103">Questo unifiedgroup accetta la risorsa di connessione, la marca del dispositivo VPN, il modello, la versione del firmware e restituisce lo script di configurazione corrispondente che i clienti possono applicare direttamente ai loro dispositivi VPN locali.</span><span class="sxs-lookup"><span data-stu-id="f8481-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="f8481-104">Lo script seguirà la sintassi del dispositivo selezionato e compilerà i parametri necessari, ad esempio gli indirizzi IP pubblici di Azure gateway, i prefissi degli indirizzi di rete virtuali, la chiave pre-condivisa del tunnel VPN e così via, quindi i clienti possono semplicemente copiare e incollare le configurazioni dei dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="f8481-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="f8481-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8481-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8481-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8481-106">DESCRIPTION</span></span>
<span data-ttu-id="f8481-107">Questo unifiedgroup accetta la risorsa di connessione, la marca del dispositivo VPN, il modello, la versione del firmware e restituisce lo script di configurazione corrispondente che i clienti possono applicare direttamente ai loro dispositivi VPN locali.</span><span class="sxs-lookup"><span data-stu-id="f8481-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="f8481-108">Lo script seguirà la sintassi del dispositivo selezionato e compilerà i parametri necessari, ad esempio gli indirizzi IP pubblici di Azure gateway, i prefissi degli indirizzi di rete virtuali, la chiave pre-condivisa del tunnel VPN e così via, quindi i clienti possono semplicemente copiare e incollare le configurazioni dei dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="f8481-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="f8481-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8481-109">EXAMPLES</span></span>

### <span data-ttu-id="f8481-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f8481-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="f8481-111">L'esempio precedente USA Get-AzVirtualNetworkGatewaySupportedVpnDevice per ottenere i marchi, i modelli e le versioni del firmware supportati per i dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="f8481-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="f8481-112">USA quindi una delle informazioni sui modelli restituiti per generare uno script di configurazione dei dispositivi VPN per il VirtualNetworkGatewayConnection "TestConnection".</span><span class="sxs-lookup"><span data-stu-id="f8481-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="f8481-113">Il dispositivo usato in questo esempio è DeviceFamily "IOS-test", DeviceVendor "Cisco-test" e FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="f8481-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="f8481-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8481-114">PARAMETERS</span></span>

### <span data-ttu-id="f8481-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8481-115">-DefaultProfile</span></span>
<span data-ttu-id="f8481-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8481-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8481-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="f8481-117">-DeviceFamily</span></span>
<span data-ttu-id="f8481-118">Nome del modello/famiglia di dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="f8481-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="f8481-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="f8481-119">-DeviceVendor</span></span>
<span data-ttu-id="f8481-120">Nome del fornitore di dispositivi VPN.</span><span class="sxs-lookup"><span data-stu-id="f8481-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="f8481-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="f8481-121">-FirmwareVersion</span></span>
<span data-ttu-id="f8481-122">Versione del firmware del dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="f8481-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="f8481-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8481-123">-Name</span></span>
<span data-ttu-id="f8481-124">Il nome della risorsa della connessione per cui deve essere generata la configurazione.</span><span class="sxs-lookup"><span data-stu-id="f8481-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="f8481-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8481-125">-ResourceGroupName</span></span>
<span data-ttu-id="f8481-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f8481-126">The resource group name.</span></span>

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

### <span data-ttu-id="f8481-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f8481-127">-Confirm</span></span>
<span data-ttu-id="f8481-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8481-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8481-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8481-129">-WhatIf</span></span>
<span data-ttu-id="f8481-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8481-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8481-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8481-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8481-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8481-132">CommonParameters</span></span>
<span data-ttu-id="f8481-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8481-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8481-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8481-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8481-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8481-135">INPUTS</span></span>

### <span data-ttu-id="f8481-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f8481-136">System.String</span></span>

## <span data-ttu-id="f8481-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8481-137">OUTPUTS</span></span>

### <span data-ttu-id="f8481-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f8481-138">System.String</span></span>

## <span data-ttu-id="f8481-139">Note</span><span class="sxs-lookup"><span data-stu-id="f8481-139">NOTES</span></span>

## <span data-ttu-id="f8481-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8481-140">RELATED LINKS</span></span>

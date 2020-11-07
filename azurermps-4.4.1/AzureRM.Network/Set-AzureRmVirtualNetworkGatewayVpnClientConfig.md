---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
ms.openlocfilehash: a0c4e6835525dfbecd4bb7eca239f8327df6ff8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687142"
---
# <span data-ttu-id="2a149-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="2a149-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>

## <span data-ttu-id="2a149-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2a149-102">SYNOPSIS</span></span>
<span data-ttu-id="2a149-103">Imposta il pool di indirizzi del client VPN per un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="2a149-103">Sets the VPN client address pool for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a149-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a149-104">SYNTAX</span></span>

### <span data-ttu-id="2a149-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2a149-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a149-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a149-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a149-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a149-107">DESCRIPTION</span></span>
<span data-ttu-id="2a149-108">Il cmdlet **set-AzureRmVirtualNetworkVpnClientConfig** configura il pool di indirizzi client per un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="2a149-108">The **Set-AzureRmVirtualNetworkVpnClientConfig** cmdlet configures the client address pool for a virtual network gateway.</span></span>
<span data-ttu-id="2a149-109">I client di reti private virtuali (VPN) che si connettono a questo gateway verranno assegnati a un indirizzo IP da questo pool di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="2a149-109">Virtual private network (VPN) clients that connect to this gateway will be assigned an IP address from this address pool.</span></span>

## <span data-ttu-id="2a149-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a149-110">EXAMPLES</span></span>

### <span data-ttu-id="2a149-111">Esempio 1: assegnare un pool di indirizzi client VPN a un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="2a149-111">Example 1: Assign a VPN client address pool to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

<span data-ttu-id="2a149-112">Questo esempio assegna un pool di indirizzi client VPN a un gateway di rete virtuale denominato ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="2a149-112">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="2a149-113">Il primo comando crea un riferimento a un oggetto al gateway e l'oggetto viene archiviato in una variabile denominata $Gateway.</span><span class="sxs-lookup"><span data-stu-id="2a149-113">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="2a149-114">Il secondo comando nell'esempio usa il cmdlet **set-AzureRmVirtualNetworkGatewayVpnClientConfig** per assegnare il pool di indirizzi 10.0.0.0/16 a ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="2a149-114">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span>

### <span data-ttu-id="2a149-115">Esempio 2: configurare l'autenticazione basata su RADIUS esterna nel gateway esistente</span><span class="sxs-lookup"><span data-stu-id="2a149-115">Example 2: Configure external radius based authentication on existing gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="2a149-116">Questo esempio assegna un pool di indirizzi client VPN a un gateway di rete virtuale denominato ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="2a149-116">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="2a149-117">Il primo comando crea un riferimento a un oggetto al gateway e l'oggetto viene archiviato in una variabile denominata $Gateway.</span><span class="sxs-lookup"><span data-stu-id="2a149-117">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="2a149-118">Il secondo comando nell'esempio usa il cmdlet **set-AzureRmVirtualNetworkGatewayVpnClientConfig** per assegnare il pool di indirizzi 10.0.0.0/16 a ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="2a149-118">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span> <span data-ttu-id="2a149-119">Configura anche il server RADIUS esterno "TestRadiusServer" da usare per l'autenticazione per i client VPN.</span><span class="sxs-lookup"><span data-stu-id="2a149-119">It also configures the external radius server "TestRadiusServer" to be used for authentication for vpn clients.</span></span>

## <span data-ttu-id="2a149-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a149-120">PARAMETERS</span></span>

### <span data-ttu-id="2a149-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a149-121">-DefaultProfile</span></span>
<span data-ttu-id="2a149-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a149-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a149-123">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="2a149-123">-RadiusServerAddress</span></span>
<span data-ttu-id="2a149-124">Indirizzo del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="2a149-124">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a149-125">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="2a149-125">-RadiusServerSecret</span></span>
<span data-ttu-id="2a149-126">Segreto del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="2a149-126">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a149-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2a149-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="2a149-128">Specifica un riferimento a un oggetto al gateway di rete virtuale che contiene le impostazioni di configurazione del client VPN modificate dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a149-128">Specifies an object reference to the virtual network gateway that contains the VPN client configuration settings that this cmdlet modifies.</span></span>
<span data-ttu-id="2a149-129">Puoi creare un riferimento a un oggetto a un gateway di rete virtuale usando la Get-AzureRmVirtualNetworkGateway e specificando il nome del gateway.</span><span class="sxs-lookup"><span data-stu-id="2a149-129">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a149-130">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="2a149-130">-VpnClientAddressPool</span></span>
<span data-ttu-id="2a149-131">Specifica gli indirizzi IP da assegnare ai client che si connettono a questo gateway</span><span class="sxs-lookup"><span data-stu-id="2a149-131">Specifies the IP addresses to be assigned to clients connecting to this gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a149-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2a149-132">-Confirm</span></span>
<span data-ttu-id="2a149-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a149-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a149-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a149-134">-WhatIf</span></span>
<span data-ttu-id="2a149-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a149-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a149-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a149-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a149-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a149-137">CommonParameters</span></span>
<span data-ttu-id="2a149-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a149-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a149-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a149-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a149-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2a149-140">INPUTS</span></span>

###  
<span data-ttu-id="2a149-141">Questo cmdlet accetta le istanze pipeline dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="2a149-141">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="2a149-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a149-142">OUTPUTS</span></span>

###  
<span data-ttu-id="2a149-143">Questo cmdlet modifica le istanze esistenti dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="2a149-143">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="2a149-144">Note</span><span class="sxs-lookup"><span data-stu-id="2a149-144">NOTES</span></span>

## <span data-ttu-id="2a149-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a149-145">RELATED LINKS</span></span>

[<span data-ttu-id="2a149-146">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="2a149-146">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="2a149-147">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2a149-147">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="2a149-148">Ridimensionare-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2a149-148">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


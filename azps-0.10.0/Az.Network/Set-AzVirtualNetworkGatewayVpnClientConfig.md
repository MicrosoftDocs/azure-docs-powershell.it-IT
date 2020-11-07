---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayvpnclientconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayVpnClientConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayVpnClientConfig.md
ms.openlocfilehash: 1c85bc5e2a935378630728083b19544ace8670b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862693"
---
# <span data-ttu-id="85f7e-101">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="85f7e-101">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>

## <span data-ttu-id="85f7e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85f7e-102">SYNOPSIS</span></span>
<span data-ttu-id="85f7e-103">Imposta il pool di indirizzi del client VPN per un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="85f7e-103">Sets the VPN client address pool for a virtual network gateway.</span></span>

## <span data-ttu-id="85f7e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85f7e-104">SYNTAX</span></span>

### <span data-ttu-id="85f7e-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="85f7e-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85f7e-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="85f7e-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85f7e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85f7e-107">DESCRIPTION</span></span>
<span data-ttu-id="85f7e-108">Il cmdlet **set-AzVirtualNetworkVpnClientConfig** configura il pool di indirizzi client per un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="85f7e-108">The **Set-AzVirtualNetworkVpnClientConfig** cmdlet configures the client address pool for a virtual network gateway.</span></span>
<span data-ttu-id="85f7e-109">I client di reti private virtuali (VPN) che si connettono a questo gateway verranno assegnati a un indirizzo IP da questo pool di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="85f7e-109">Virtual private network (VPN) clients that connect to this gateway will be assigned an IP address from this address pool.</span></span>

## <span data-ttu-id="85f7e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85f7e-110">EXAMPLES</span></span>

### <span data-ttu-id="85f7e-111">Esempio 1: assegnare un pool di indirizzi client VPN a un gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="85f7e-111">Example 1: Assign a VPN client address pool to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

<span data-ttu-id="85f7e-112">Questo esempio assegna un pool di indirizzi client VPN a un gateway di rete virtuale denominato ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="85f7e-112">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="85f7e-113">Il primo comando crea un riferimento a un oggetto al gateway e l'oggetto viene archiviato in una variabile denominata $Gateway.</span><span class="sxs-lookup"><span data-stu-id="85f7e-113">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="85f7e-114">Il secondo comando nell'esempio usa il cmdlet **set-AzVirtualNetworkGatewayVpnClientConfig** per assegnare il pool di indirizzi 10.0.0.0/16 a ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="85f7e-114">The second command in the example then uses the **Set-AzVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span>

### <span data-ttu-id="85f7e-115">Esempio 2: configurare l'autenticazione basata su RADIUS esterna nel gateway esistente</span><span class="sxs-lookup"><span data-stu-id="85f7e-115">Example 2: Configure external radius based authentication on existing gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="85f7e-116">Questo esempio assegna un pool di indirizzi client VPN a un gateway di rete virtuale denominato ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="85f7e-116">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="85f7e-117">Il primo comando crea un riferimento a un oggetto al gateway e l'oggetto viene archiviato in una variabile denominata $Gateway.</span><span class="sxs-lookup"><span data-stu-id="85f7e-117">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="85f7e-118">Il secondo comando nell'esempio usa il cmdlet **set-AzVirtualNetworkGatewayVpnClientConfig** per assegnare il pool di indirizzi 10.0.0.0/16 a ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="85f7e-118">The second command in the example then uses the **Set-AzVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span> <span data-ttu-id="85f7e-119">Configura anche il server RADIUS esterno "TestRadiusServer" da usare per l'autenticazione per i client VPN.</span><span class="sxs-lookup"><span data-stu-id="85f7e-119">It also configures the external radius server "TestRadiusServer" to be used for authentication for vpn clients.</span></span>

## <span data-ttu-id="85f7e-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85f7e-120">PARAMETERS</span></span>

### <span data-ttu-id="85f7e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85f7e-121">-DefaultProfile</span></span>
<span data-ttu-id="85f7e-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85f7e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85f7e-123">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="85f7e-123">-RadiusServerAddress</span></span>
<span data-ttu-id="85f7e-124">Indirizzo del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="85f7e-124">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85f7e-125">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="85f7e-125">-RadiusServerSecret</span></span>
<span data-ttu-id="85f7e-126">Segreto del server RADIUS esterno P2S.</span><span class="sxs-lookup"><span data-stu-id="85f7e-126">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85f7e-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="85f7e-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="85f7e-128">Specifica un riferimento a un oggetto al gateway di rete virtuale che contiene le impostazioni di configurazione del client VPN modificate dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85f7e-128">Specifies an object reference to the virtual network gateway that contains the VPN client configuration settings that this cmdlet modifies.</span></span>
<span data-ttu-id="85f7e-129">Puoi creare un riferimento a un oggetto a un gateway di rete virtuale usando la Get-AzVirtualNetworkGateway e specificando il nome del gateway.</span><span class="sxs-lookup"><span data-stu-id="85f7e-129">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85f7e-130">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="85f7e-130">-VpnClientAddressPool</span></span>
<span data-ttu-id="85f7e-131">Specifica gli indirizzi IP da assegnare ai client che si connettono a questo gateway</span><span class="sxs-lookup"><span data-stu-id="85f7e-131">Specifies the IP addresses to be assigned to clients connecting to this gateway</span></span>

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

### <span data-ttu-id="85f7e-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="85f7e-132">-Confirm</span></span>
<span data-ttu-id="85f7e-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85f7e-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85f7e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85f7e-134">-WhatIf</span></span>
<span data-ttu-id="85f7e-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85f7e-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85f7e-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85f7e-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85f7e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85f7e-137">CommonParameters</span></span>
<span data-ttu-id="85f7e-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85f7e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85f7e-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85f7e-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85f7e-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85f7e-140">INPUTS</span></span>

###  
<span data-ttu-id="85f7e-141">Questo cmdlet accetta le istanze pipeline dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="85f7e-141">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="85f7e-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85f7e-142">OUTPUTS</span></span>

###  
<span data-ttu-id="85f7e-143">Questo cmdlet modifica le istanze esistenti dell'oggetto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="85f7e-143">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="85f7e-144">Note</span><span class="sxs-lookup"><span data-stu-id="85f7e-144">NOTES</span></span>

## <span data-ttu-id="85f7e-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85f7e-145">RELATED LINKS</span></span>

[<span data-ttu-id="85f7e-146">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="85f7e-146">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

[<span data-ttu-id="85f7e-147">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="85f7e-147">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="85f7e-148">Ridimensionare-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="85f7e-148">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)



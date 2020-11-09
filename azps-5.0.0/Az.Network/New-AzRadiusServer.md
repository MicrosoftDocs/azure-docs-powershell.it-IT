---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azradiusserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRadiusServer.md
ms.openlocfilehash: 0f92f09d3caf481f845c96942fd038a82c1078ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301920"
---
# <span data-ttu-id="b3a4f-101">New-AzRadiusServer</span><span class="sxs-lookup"><span data-stu-id="b3a4f-101">New-AzRadiusServer</span></span>

## <span data-ttu-id="b3a4f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3a4f-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a4f-103">Crea una configurazione del server RADIUS esterno</span><span class="sxs-lookup"><span data-stu-id="b3a4f-103">Creates an external radius server configuration</span></span>

## <span data-ttu-id="b3a4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3a4f-104">SYNTAX</span></span>

```
New-AzRadiusServer -RadiusServerAddress <String> -RadiusServerSecret <SecureString>
 [-RadiusServerScore <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3a4f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3a4f-105">DESCRIPTION</span></span>
<span data-ttu-id="b3a4f-106">Il cmdlet New-AzRadiusServer crea una configurazione del server RADIUS esterna da usare nella configurazione del gateway di rete virtuale e del server VPN.</span><span class="sxs-lookup"><span data-stu-id="b3a4f-106">The New-AzRadiusServer cmdlet creates an external radius server configuration to be used in virtual network gateway and VPN server configuration.</span></span>

## <span data-ttu-id="b3a4f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3a4f-107">EXAMPLES</span></span>

### <span data-ttu-id="b3a4f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b3a4f-108">Example 1</span></span>
```powershell
PS C:\> $radiusServer1 = New-AzRadiusServer -RadiusServerAddress 10.1.0.1 -RadiusServerSecret $radiuspd -RadiusServerScore 30
PS C:\> $radiusServer2 = New-AzRadiusServer -RadiusServerAddress 10.1.0.2 -RadiusServerSecret $radiuspd -RadiusServerScore 1
PS C:\> New-AzVirtualNetworkGateway -ResourceGroupName $rgname -name $rname -location $location -IpConfigurations $vnetIpConfig -GatewayType Vpn -VpnType RouteBased -EnableBgp $false -GatewaySku VpnGw1 -VpnClientAddressPool 201.169.0.0/16 -VpnClientProtocol "IkeV2" -RadiusServerList $radiusServers
```

<span data-ttu-id="b3a4f-109">Creazione di più configurazioni di server RADIUS esterni da usare per la configurazione di P2S in un nuovo gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="b3a4f-109">Creating multiple external radius server configurations to be used for configuring P2S on a new virtual network gateway.</span></span>

## <span data-ttu-id="b3a4f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3a4f-110">PARAMETERS</span></span>

### <span data-ttu-id="b3a4f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a4f-111">-DefaultProfile</span></span>
<span data-ttu-id="b3a4f-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a4f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3a4f-113">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="b3a4f-113">-RadiusServerAddress</span></span>
<span data-ttu-id="b3a4f-114">Indirizzo del server RADIUS esterno</span><span class="sxs-lookup"><span data-stu-id="b3a4f-114">External radius server address</span></span>

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

### <span data-ttu-id="b3a4f-115">-RadiusServerScore</span><span class="sxs-lookup"><span data-stu-id="b3a4f-115">-RadiusServerScore</span></span>
<span data-ttu-id="b3a4f-116">Punteggio del server RADIUS esterno</span><span class="sxs-lookup"><span data-stu-id="b3a4f-116">External radius server score</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a4f-117">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="b3a4f-117">-RadiusServerSecret</span></span>
<span data-ttu-id="b3a4f-118">Segreto del server RADIUS esterno</span><span class="sxs-lookup"><span data-stu-id="b3a4f-118">External radius server secret</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a4f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a4f-119">CommonParameters</span></span>
<span data-ttu-id="b3a4f-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3a4f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a4f-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3a4f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a4f-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3a4f-122">INPUTS</span></span>

### <span data-ttu-id="b3a4f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b3a4f-123">System.String</span></span>

### <span data-ttu-id="b3a4f-124">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="b3a4f-124">System.Security.SecureString</span></span>

### <span data-ttu-id="b3a4f-125">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b3a4f-125">System.Int32</span></span>

## <span data-ttu-id="b3a4f-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3a4f-126">OUTPUTS</span></span>

### <span data-ttu-id="b3a4f-127">Microsoft. Azure. Commands. Network. Models. PSRadiusServer</span><span class="sxs-lookup"><span data-stu-id="b3a4f-127">Microsoft.Azure.Commands.Network.Models.PSRadiusServer</span></span>

## <span data-ttu-id="b3a4f-128">Note</span><span class="sxs-lookup"><span data-stu-id="b3a4f-128">NOTES</span></span>

## <span data-ttu-id="b3a4f-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3a4f-129">RELATED LINKS</span></span>

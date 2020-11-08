---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
ms.openlocfilehash: 4b9778275f58025c82922133cb5d6f6142df4fc8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202949"
---
# <span data-ttu-id="31bab-101">Get-AzP2sVpnGatewayConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="31bab-101">Get-AzP2sVpnGatewayConnectionHealth</span></span>

## <span data-ttu-id="31bab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31bab-102">SYNOPSIS</span></span>
<span data-ttu-id="31bab-103">Ottiene il punto di aggregared corrente per le informazioni sull'integrità delle connessioni del sito da P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="31bab-103">Gets the current aggregared point to site connections health information from P2SVpnGateway.</span></span>

## <span data-ttu-id="31bab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31bab-104">SYNTAX</span></span>

### <span data-ttu-id="31bab-105">ByP2SVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="31bab-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31bab-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="31bab-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -InputObject <PSP2SVpnGateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31bab-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="31bab-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31bab-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31bab-108">DESCRIPTION</span></span>
<span data-ttu-id="31bab-109">Il cmdlet **Get-AzP2sVpnGatewayConnectionHealth** consente di ottenere lo stato aggregato corrente di Point to Connections sito da P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="31bab-109">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="31bab-110">L'integrità aggregata Mostra il numero di punti per i client del sito connessi a P2SVpnGateway, l'ingresso totale e i byte di uscita trasferiti tramite P2SVpnGateway e gli indirizzi IP assegnati per il punto collegato ai client del sito.</span><span class="sxs-lookup"><span data-stu-id="31bab-110">Aggregated health shows number of point to site clients connected to P2SVpnGateway, total ingress and egress bytes transferred through P2SVpnGateway and allocated ip addresses for connected point to site clients.</span></span>

## <span data-ttu-id="31bab-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31bab-111">EXAMPLES</span></span>

### <span data-ttu-id="31bab-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="31bab-112">Example 1</span></span>
```powershell
PS C:\> Get-AzP2sVpnGatewayConnectionHealth -ResourceGroupName P2SCortexGATesting -Name 683482ade8564515aed4b8448c9757ea-westus-gw

ResourceGroupName              : P2SCortexGATesting
Name                           : 683482ade8564515aed4b8448c9757ea-westus-gw
Id                             : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482ade8564515a
                                 ed4b8448c9757ea-westus-gw
Location                       : westus
VpnGatewayScaleUnit            : 1
VirtualHub                     : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/virtualHubs/WestUsVirtualHub
VpnServerConfiguration         : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig
VpnServerConfigurationLocation :
VpnClientConnectionHealth      : { 
                  "VpnClientConnectionsCount": 2,
                      "AllocatedIpAddresses": { "192.168.2.1", "192.168.2.2" },
                      "TotalIngressBytesTransferred": 100,
                      "TotalEgressBytesTransferred": 200
                 }
Type                           : Microsoft.Network/p2sVpnGateways
ProvisioningState              : Succeeded
P2SConnectionConfigurations    : [
                                   {
                                     "ProvisioningState": "Succeeded",
                                     "VpnClientAddressPool": {
                                       "AddressPrefixes": [
                                         "192.168.2.0/24"
                                       ]
                                     },
                                     "Name": "P2SConnectionConfigDefault",
                                     "Etag": "W/\"4b96e6a2-b4d8-46b3-9210-76d40f359bef\"",
                                     "Id": "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/p2sVpnGateways/683482
                                 ade8564515aed4b8448c9757ea-westus-gw/p2sConnectionConfigurations/P2SConnectionConfigDefault"
                                   }
                                 ]
```

<span data-ttu-id="31bab-113">Il cmdlet **Get-AzP2sVpnGatewayConnectionHealth** consente di ottenere lo stato aggregato corrente di Point to Connections sito da P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="31bab-113">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="31bab-114">Sopra comando consente l'integrità dell'output indica che il numero di punti per i client del sito connessi a P2SVpnGateway è 2.</span><span class="sxs-lookup"><span data-stu-id="31bab-114">Above command let output health shows that number of point to site clients connected to P2SVpnGateway are 2.</span></span> <span data-ttu-id="31bab-115">I byte totali di ingresso e di uscita trasferiti tramite P2SVpnGateway sono rispettivamente 100 e 200.</span><span class="sxs-lookup"><span data-stu-id="31bab-115">Total ingress and egress bytes transferred through P2SVpnGateway are 100 and 200 respectively.</span></span> <span data-ttu-id="31bab-116">Gli indirizzi IP assegnati per il punto connesso ai client del sito sono "192.168.2.1", "192.168.2.2".</span><span class="sxs-lookup"><span data-stu-id="31bab-116">Allocated ip addresses for connected point to site clients are "192.168.2.1", "192.168.2.2".</span></span>

## <span data-ttu-id="31bab-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31bab-117">PARAMETERS</span></span>

### <span data-ttu-id="31bab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31bab-118">-DefaultProfile</span></span>
<span data-ttu-id="31bab-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31bab-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31bab-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31bab-120">-InputObject</span></span>
<span data-ttu-id="31bab-121">L'oggetto gateway VPN di P2S da modificare</span><span class="sxs-lookup"><span data-stu-id="31bab-121">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31bab-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="31bab-122">-Name</span></span>
<span data-ttu-id="31bab-123">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="31bab-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31bab-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31bab-124">-ResourceGroupName</span></span>
<span data-ttu-id="31bab-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="31bab-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31bab-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31bab-126">-ResourceId</span></span>
<span data-ttu-id="31bab-127">ID risorsa di Azure della P2SVpnGateway da modificare.</span><span class="sxs-lookup"><span data-stu-id="31bab-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31bab-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31bab-128">CommonParameters</span></span>
<span data-ttu-id="31bab-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31bab-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31bab-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31bab-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31bab-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31bab-131">INPUTS</span></span>

### <span data-ttu-id="31bab-132">System. String</span><span class="sxs-lookup"><span data-stu-id="31bab-132">System.String</span></span>
<span data-ttu-id="31bab-133">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="31bab-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="31bab-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31bab-134">OUTPUTS</span></span>

### <span data-ttu-id="31bab-135">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="31bab-135">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="31bab-136">Note</span><span class="sxs-lookup"><span data-stu-id="31bab-136">NOTES</span></span>

## <span data-ttu-id="31bab-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31bab-137">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewayconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayConnectionHealth.md
ms.openlocfilehash: 4b9778275f58025c82922133cb5d6f6142df4fc8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193782"
---
# <span data-ttu-id="cdb83-101">Get-AzP2sVpnGatewayConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="cdb83-101">Get-AzP2sVpnGatewayConnectionHealth</span></span>

## <span data-ttu-id="cdb83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdb83-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb83-103">Recupera le informazioni sull'integrità delle connessioni del sito dal punto aggregato corrente da P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="cdb83-103">Gets the current aggregared point to site connections health information from P2SVpnGateway.</span></span>

## <span data-ttu-id="cdb83-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cdb83-104">SYNTAX</span></span>

### <span data-ttu-id="cdb83-105">ByP2SVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cdb83-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdb83-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="cdb83-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -InputObject <PSP2SVpnGateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cdb83-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="cdb83-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayConnectionHealth -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cdb83-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cdb83-108">DESCRIPTION</span></span>
<span data-ttu-id="cdb83-109">Il cmdlet **Get-AzP2sVpnGatewayConnectionHealth** consente di ottenere l'integrità aggregata corrente delle connessioni punto a sito da P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="cdb83-109">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="cdb83-110">L'integrità aggregata mostra il numero di client del sito connessi a P2SVpnGateway, il numero totale di byte in ingresso e in uscita trasferiti tramite P2SVpnGateway e gli indirizzi IP allocati per il punto connesso ai client del sito.</span><span class="sxs-lookup"><span data-stu-id="cdb83-110">Aggregated health shows number of point to site clients connected to P2SVpnGateway, total ingress and egress bytes transferred through P2SVpnGateway and allocated ip addresses for connected point to site clients.</span></span>

## <span data-ttu-id="cdb83-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cdb83-111">EXAMPLES</span></span>

### <span data-ttu-id="cdb83-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cdb83-112">Example 1</span></span>
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

<span data-ttu-id="cdb83-113">Il cmdlet **Get-AzP2sVpnGatewayConnectionHealth** consente di ottenere l'integrità aggregata corrente delle connessioni punto a sito da P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="cdb83-113">The **Get-AzP2sVpnGatewayConnectionHealth** cmdlet enables you to get the current aggregated health of point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="cdb83-114">Il comando precedente consente l'integrità dell'output indica che il numero di client del sito connessi a P2SVpnGateway è 2.</span><span class="sxs-lookup"><span data-stu-id="cdb83-114">Above command let output health shows that number of point to site clients connected to P2SVpnGateway are 2.</span></span> <span data-ttu-id="cdb83-115">I byte totali in ingresso e in uscita trasferiti tramite P2SVpnGateway sono rispettivamente di 100 e 200.</span><span class="sxs-lookup"><span data-stu-id="cdb83-115">Total ingress and egress bytes transferred through P2SVpnGateway are 100 and 200 respectively.</span></span> <span data-ttu-id="cdb83-116">Gli indirizzi IP allocati per i client dei punti connessi ai client del sito sono "192.168.2.1", "192.168.2.2".</span><span class="sxs-lookup"><span data-stu-id="cdb83-116">Allocated ip addresses for connected point to site clients are "192.168.2.1", "192.168.2.2".</span></span>

## <span data-ttu-id="cdb83-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdb83-117">PARAMETERS</span></span>

### <span data-ttu-id="cdb83-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdb83-118">-DefaultProfile</span></span>
<span data-ttu-id="cdb83-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cdb83-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdb83-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdb83-120">-InputObject</span></span>
<span data-ttu-id="cdb83-121">Oggetto gateway VPN p2s da modificare</span><span class="sxs-lookup"><span data-stu-id="cdb83-121">The p2s vpn gateway object to be modified</span></span>

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

### <span data-ttu-id="cdb83-122">-Name</span><span class="sxs-lookup"><span data-stu-id="cdb83-122">-Name</span></span>
<span data-ttu-id="cdb83-123">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cdb83-123">The resource name.</span></span>

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

### <span data-ttu-id="cdb83-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdb83-124">-ResourceGroupName</span></span>
<span data-ttu-id="cdb83-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cdb83-125">The resource group name.</span></span>

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

### <span data-ttu-id="cdb83-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cdb83-126">-ResourceId</span></span>
<span data-ttu-id="cdb83-127">ID della risorsa Azure di P2SVpnGateway da modificare.</span><span class="sxs-lookup"><span data-stu-id="cdb83-127">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

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

### <span data-ttu-id="cdb83-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb83-128">CommonParameters</span></span>
<span data-ttu-id="cdb83-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdb83-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb83-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdb83-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb83-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="cdb83-131">INPUTS</span></span>

### <span data-ttu-id="cdb83-132">System.String</span><span class="sxs-lookup"><span data-stu-id="cdb83-132">System.String</span></span>
<span data-ttu-id="cdb83-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="cdb83-133">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="cdb83-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cdb83-134">OUTPUTS</span></span>

### <span data-ttu-id="cdb83-135">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="cdb83-135">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="cdb83-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="cdb83-136">NOTES</span></span>

## <span data-ttu-id="cdb83-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cdb83-137">RELATED LINKS</span></span>

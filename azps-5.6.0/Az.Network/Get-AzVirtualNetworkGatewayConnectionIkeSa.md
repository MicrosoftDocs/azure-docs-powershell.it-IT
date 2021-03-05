---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionikesa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
ms.openlocfilehash: 0f5cedd29b7dcc296494519fe40f8ea7e0edb445
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964253"
---
# <span data-ttu-id="b3197-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="b3197-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="b3197-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3197-102">SYNOPSIS</span></span>
<span data-ttu-id="b3197-103">Ottenere le associazioni di sicurezza IKE di una connessione a Gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="b3197-103">Get IKE Security Associations of a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="b3197-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3197-104">SYNTAX</span></span>

### <span data-ttu-id="b3197-105">ByName</span><span class="sxs-lookup"><span data-stu-id="b3197-105">ByName</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-Name <String>] -ResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3197-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b3197-106">ByInputObject</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa -InputObject <PSVirtualNetworkGatewayConnection> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3197-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b3197-107">ByResourceId</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-ResourceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3197-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b3197-108">DESCRIPTION</span></span>
<span data-ttu-id="b3197-109">Il cmdlet **Get-AzVirtualNetworkGatewayConnectionIkeSa** restituisce le associazioni di sicurezza IKE della connessione in base al nome della connessione e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b3197-109">The **Get-AzVirtualNetworkGatewayConnectionIkeSa** cmdlet returns the IKE Security Associations of your connection based on the Connection Name and Resource Group Name.</span></span>
<span data-ttu-id="b3197-110">Se il cmdlet **Get-AzVirtualNetworkGatewayConnection** viene generato senza specificare il parametro -Name, l'output non mostrerà le associazioni di sicurezza IKE.</span><span class="sxs-lookup"><span data-stu-id="b3197-110">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show the IKE Security Associations.</span></span>

## <span data-ttu-id="b3197-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3197-111">EXAMPLES</span></span>

### <span data-ttu-id="b3197-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b3197-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualNetworkGatewayConnectionIkeSa -ResourceGroupName myRG -Name myTunnel
localEndpoint              : 52.180.160.154
remoteEndpoint             : 104.208.54.1
initiatorCookie            : 5490733703579933026
responderCookie            : 15460013388959380535
localUdpEncapsulationPort  : 0
remoteUdpEncapsulationPort : 0
encryption                 : AES256
integrity                  : SHA1
dhGroup                    : DHGroup2
lifeTimeSeconds            : 28800
isSaInitiator              : True
elapsedTimeInseconds       : 23092
quickModeSa                : {}
```

<span data-ttu-id="b3197-113">Restituisce le associazioni di sicurezza IKE per la connessione a Gateway di rete virtuale con il nome "myTunnel" all'interno del gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="b3197-113">Returns the IKE Security Associations for the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="b3197-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3197-114">PARAMETERS</span></span>

### <span data-ttu-id="b3197-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3197-115">-AsJob</span></span>
<span data-ttu-id="b3197-116">Eseguire il cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="b3197-116">Run cmdlet in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3197-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3197-117">-DefaultProfile</span></span>
<span data-ttu-id="b3197-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3197-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3197-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3197-119">-InputObject</span></span>
<span data-ttu-id="b3197-120">Oggetto di connessione al gateway di rete virtuale per cui è necessario recuperare gli oggetti IKE.</span><span class="sxs-lookup"><span data-stu-id="b3197-120">The virtual network gateway connection object for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3197-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b3197-121">-Name</span></span>
<span data-ttu-id="b3197-122">Nome della connessione del gateway di rete virtuale per cui è necessario recuperare gli SA IKE.</span><span class="sxs-lookup"><span data-stu-id="b3197-122">The virtual network gateway connection name for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, ConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3197-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3197-123">-ResourceGroupName</span></span>
<span data-ttu-id="b3197-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b3197-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3197-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3197-125">-ResourceId</span></span>
<span data-ttu-id="b3197-126">ID della risorsa Azure della connessione del Gateway di rete virtuale per cui recuperare gli ID IKE.</span><span class="sxs-lookup"><span data-stu-id="b3197-126">The Azure resource ID of the Virtual Network Gateway Connection for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3197-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3197-127">CommonParameters</span></span>
<span data-ttu-id="b3197-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3197-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3197-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b3197-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3197-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="b3197-130">INPUTS</span></span>

### <span data-ttu-id="b3197-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b3197-131">System.String</span></span>

## <span data-ttu-id="b3197-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3197-132">OUTPUTS</span></span>

### <span data-ttu-id="b3197-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="b3197-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="b3197-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="b3197-134">NOTES</span></span>

## <span data-ttu-id="b3197-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3197-135">RELATED LINKS</span></span>

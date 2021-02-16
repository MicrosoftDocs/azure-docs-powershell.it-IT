---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionikesa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
ms.openlocfilehash: 6b0eb456c2134e6ed64d8e6c441db041776fcf39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179806"
---
# <span data-ttu-id="647df-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="647df-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="647df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="647df-102">SYNOPSIS</span></span>
<span data-ttu-id="647df-103">Ottenere le associazioni di sicurezza IKE di una connessione a Gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="647df-103">Get IKE Security Associations of a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="647df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="647df-104">SYNTAX</span></span>

### <span data-ttu-id="647df-105">ByName</span><span class="sxs-lookup"><span data-stu-id="647df-105">ByName</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-Name <String>] -ResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="647df-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="647df-106">ByInputObject</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa -InputObject <PSVirtualNetworkGatewayConnection> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="647df-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="647df-107">ByResourceId</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-ResourceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="647df-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="647df-108">DESCRIPTION</span></span>
<span data-ttu-id="647df-109">Il cmdlet **Get-AzVirtualNetworkGatewayConnectionIkeSa** restituisce le associazioni di sicurezza IKE della connessione in base al nome della connessione e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="647df-109">The **Get-AzVirtualNetworkGatewayConnectionIkeSa** cmdlet returns the IKE Security Associations of your connection based on the Connection Name and Resource Group Name.</span></span>
<span data-ttu-id="647df-110">Se il cmdlet **Get-AzVirtualNetworkGatewayConnection** viene generato senza specificare il parametro -Name, l'output non mostrerà le associazioni di sicurezza IKE.</span><span class="sxs-lookup"><span data-stu-id="647df-110">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show the IKE Security Associations.</span></span>

## <span data-ttu-id="647df-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="647df-111">EXAMPLES</span></span>

### <span data-ttu-id="647df-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="647df-112">Example 1</span></span>
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

<span data-ttu-id="647df-113">Restituisce le associazioni di sicurezza IKE per la connessione a Gateway di rete virtuale con il nome "myTunnel" all'interno del gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="647df-113">Returns the IKE Security Associations for the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="647df-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="647df-114">PARAMETERS</span></span>

### <span data-ttu-id="647df-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="647df-115">-AsJob</span></span>
<span data-ttu-id="647df-116">Eseguire il cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="647df-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="647df-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="647df-117">-DefaultProfile</span></span>
<span data-ttu-id="647df-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="647df-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="647df-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="647df-119">-InputObject</span></span>
<span data-ttu-id="647df-120">Oggetto di connessione al gateway di rete virtuale per cui è necessario recuperare gli oggetti IKE.</span><span class="sxs-lookup"><span data-stu-id="647df-120">The virtual network gateway connection object for which IKE SAs needs to be fetched.</span></span>

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

### <span data-ttu-id="647df-121">-Name</span><span class="sxs-lookup"><span data-stu-id="647df-121">-Name</span></span>
<span data-ttu-id="647df-122">Nome della connessione del gateway di rete virtuale per cui è necessario recuperare gli SA IKE.</span><span class="sxs-lookup"><span data-stu-id="647df-122">The virtual network gateway connection name for which IKE SAs needs to be fetched.</span></span>

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

### <span data-ttu-id="647df-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="647df-123">-ResourceGroupName</span></span>
<span data-ttu-id="647df-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="647df-124">The resource group name.</span></span>

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

### <span data-ttu-id="647df-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="647df-125">-ResourceId</span></span>
<span data-ttu-id="647df-126">ID della risorsa Azure della connessione a Gateway di rete virtuale per cui recuperare gli ID IKE.</span><span class="sxs-lookup"><span data-stu-id="647df-126">The Azure resource ID of the Virtual Network Gateway Connection for which IKE SAs needs to be fetched.</span></span>

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

### <span data-ttu-id="647df-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="647df-127">CommonParameters</span></span>
<span data-ttu-id="647df-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="647df-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="647df-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="647df-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="647df-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="647df-130">INPUTS</span></span>

### <span data-ttu-id="647df-131">System.String</span><span class="sxs-lookup"><span data-stu-id="647df-131">System.String</span></span>

## <span data-ttu-id="647df-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="647df-132">OUTPUTS</span></span>

### <span data-ttu-id="647df-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="647df-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="647df-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="647df-134">NOTES</span></span>

## <span data-ttu-id="647df-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="647df-135">RELATED LINKS</span></span>

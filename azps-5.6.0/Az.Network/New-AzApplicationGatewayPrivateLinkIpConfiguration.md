---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayprivatelinkipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
ms.openlocfilehash: 4a34899a4e6c37ad3d4c84c173d07012110dcad7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986745"
---
# <span data-ttu-id="56f41-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="56f41-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="56f41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56f41-102">SYNOPSIS</span></span>
<span data-ttu-id="56f41-103">Crea una configurazione IP da associare alla configurazione PrivateLink</span><span class="sxs-lookup"><span data-stu-id="56f41-103">Creates an Ip Configuration to be associated with PrivateLink Configuration</span></span>

## <span data-ttu-id="56f41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56f41-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkIpConfiguration -Name <String> -Subnet <PSSubnet>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56f41-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="56f41-105">DESCRIPTION</span></span>
<span data-ttu-id="56f41-106">Il cmdlet **New-AzApplicationGatewayPrivateLinkIpConfiguration** crea una configurazione Ip da associare alla configurazione PrivateLink per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="56f41-106">The **New-AzApplicationGatewayPrivateLinkIpConfiguration** cmdlet creates an Ip Configuration to be associated with PrivateLink Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="56f41-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56f41-107">EXAMPLES</span></span>

### <span data-ttu-id="56f41-108">Esempio 1: Configurazione IP PrivateLink</span><span class="sxs-lookup"><span data-stu-id="56f41-108">Example 1: PrivateLink Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkIpConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
```

<span data-ttu-id="56f41-109">Questo comando crea una configurazione IP PrivateLink denominata 'ipConfig01' che archivia il risultato nella variabile $PrivateLinkIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="56f41-109">This command creates an PrivateLink IP Configuration named 'ipConfig01' stores the result in the variable named $PrivateLinkIpConfiguration.</span></span> 

## <span data-ttu-id="56f41-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56f41-110">PARAMETERS</span></span>

### <span data-ttu-id="56f41-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56f41-111">-DefaultProfile</span></span>
<span data-ttu-id="56f41-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56f41-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56f41-113">-Name</span><span class="sxs-lookup"><span data-stu-id="56f41-113">-Name</span></span>
<span data-ttu-id="56f41-114">Il nome di IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="56f41-114">The name of the IpConfiguration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f41-115">-Principale</span><span class="sxs-lookup"><span data-stu-id="56f41-115">-Primary</span></span>
<span data-ttu-id="56f41-116">Indicare che la configurazione IP è principale.</span><span class="sxs-lookup"><span data-stu-id="56f41-116">Indicate the ip configuration is primary.</span></span>

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

### <span data-ttu-id="56f41-117">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="56f41-117">-PrivateIpAddress</span></span>
<span data-ttu-id="56f41-118">Indirizzo IP privato della configurazione ip, se si desidera l'allocazione statica.</span><span class="sxs-lookup"><span data-stu-id="56f41-118">The private ip address of the ipConfiguration if static allocation is desired.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f41-119">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="56f41-119">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="56f41-120">Versione IP della configurazione IP</span><span class="sxs-lookup"><span data-stu-id="56f41-120">The ip version of the ip configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f41-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="56f41-121">-Subnet</span></span>
<span data-ttu-id="56f41-122">Subnet</span><span class="sxs-lookup"><span data-stu-id="56f41-122">Subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f41-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56f41-123">CommonParameters</span></span>
<span data-ttu-id="56f41-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56f41-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56f41-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="56f41-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56f41-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="56f41-126">INPUTS</span></span>

### <span data-ttu-id="56f41-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="56f41-127">None</span></span>

## <span data-ttu-id="56f41-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56f41-128">OUTPUTS</span></span>

### <span data-ttu-id="56f41-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="56f41-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="56f41-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="56f41-130">NOTES</span></span>

## <span data-ttu-id="56f41-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56f41-131">RELATED LINKS</span></span>

[<span data-ttu-id="56f41-132">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="56f41-132">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

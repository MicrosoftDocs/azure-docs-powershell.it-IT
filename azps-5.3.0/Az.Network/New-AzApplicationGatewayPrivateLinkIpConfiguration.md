---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkIpConfiguration.md
ms.openlocfilehash: 01da3615a43a5923d6017e759c1b04f039332c9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379413"
---
# <span data-ttu-id="59495-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="59495-101">New-AzApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="59495-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59495-102">SYNOPSIS</span></span>
<span data-ttu-id="59495-103">Crea una configurazione IP da associare alla configurazione di PrivateLink</span><span class="sxs-lookup"><span data-stu-id="59495-103">Creates an Ip Configuration to be associated with PrivateLink Configuration</span></span>

## <span data-ttu-id="59495-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59495-104">SYNTAX</span></span>

```
New-AzApplicationGatewayPrivateLinkIpConfiguration -Name <String> -Subnet <PSSubnet>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59495-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59495-105">DESCRIPTION</span></span>
<span data-ttu-id="59495-106">Il cmdlet **New-AzApplicationGatewayPrivateLinkIpConfiguration** crea una configurazione IP da associare alla configurazione di PrivateLink per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="59495-106">The **New-AzApplicationGatewayPrivateLinkIpConfiguration** cmdlet creates an Ip Configuration to be associated with PrivateLink Configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="59495-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59495-107">EXAMPLES</span></span>

### <span data-ttu-id="59495-108">Esempio 1: configurazione IP di PrivateLink</span><span class="sxs-lookup"><span data-stu-id="59495-108">Example 1: PrivateLink Ip Configuration</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkIpConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
```

<span data-ttu-id="59495-109">Questo comando crea una configurazione IP PrivateLink denominata "ipConfig01" archivia il risultato nella variabile denominata $PrivateLinkIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="59495-109">This command creates an PrivateLink IP Configuration named 'ipConfig01' stores the result in the variable named $PrivateLinkIpConfiguration.</span></span> 

## <span data-ttu-id="59495-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59495-110">PARAMETERS</span></span>

### <span data-ttu-id="59495-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59495-111">-DefaultProfile</span></span>
<span data-ttu-id="59495-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="59495-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59495-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="59495-113">-Name</span></span>
<span data-ttu-id="59495-114">Nome del IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="59495-114">The name of the IpConfiguration</span></span>

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

### <span data-ttu-id="59495-115">-Primaria</span><span class="sxs-lookup"><span data-stu-id="59495-115">-Primary</span></span>
<span data-ttu-id="59495-116">Indicare che la configurazione IP è primaria.</span><span class="sxs-lookup"><span data-stu-id="59495-116">Indicate the ip configuration is primary.</span></span>

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

### <span data-ttu-id="59495-117">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="59495-117">-PrivateIpAddress</span></span>
<span data-ttu-id="59495-118">Indirizzo IP privato di ipConfiguration se si vuole assegnare l'allocazione statica.</span><span class="sxs-lookup"><span data-stu-id="59495-118">The private ip address of the ipConfiguration if static allocation is desired.</span></span>

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

### <span data-ttu-id="59495-119">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="59495-119">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="59495-120">Versione IP della configurazione IP</span><span class="sxs-lookup"><span data-stu-id="59495-120">The ip version of the ip configuration</span></span>

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

### <span data-ttu-id="59495-121">-Subnet</span><span class="sxs-lookup"><span data-stu-id="59495-121">-Subnet</span></span>
<span data-ttu-id="59495-122">Subnet</span><span class="sxs-lookup"><span data-stu-id="59495-122">Subnet</span></span>

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

### <span data-ttu-id="59495-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59495-123">CommonParameters</span></span>
<span data-ttu-id="59495-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59495-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59495-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59495-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59495-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59495-126">INPUTS</span></span>

### <span data-ttu-id="59495-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="59495-127">None</span></span>

## <span data-ttu-id="59495-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59495-128">OUTPUTS</span></span>

### <span data-ttu-id="59495-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="59495-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration</span></span>

## <span data-ttu-id="59495-130">Note</span><span class="sxs-lookup"><span data-stu-id="59495-130">NOTES</span></span>

## <span data-ttu-id="59495-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59495-131">RELATED LINKS</span></span>

[<span data-ttu-id="59495-132">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="59495-132">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

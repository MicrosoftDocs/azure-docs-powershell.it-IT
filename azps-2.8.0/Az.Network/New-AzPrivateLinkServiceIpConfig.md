---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceIpConfig.md
ms.openlocfilehash: c7ea999af626206b741e86457d92627e4db196a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852905"
---
# <span data-ttu-id="2d787-101">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2d787-101">New-AzPrivateLinkServiceIpConfig</span></span>

## <span data-ttu-id="2d787-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2d787-102">SYNOPSIS</span></span>
<span data-ttu-id="2d787-103">Creare una configurazione IP di un servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="2d787-103">Create a private link service ip configuration.</span></span>

## <span data-ttu-id="2d787-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2d787-104">SYNTAX</span></span>

```
New-AzPrivateLinkServiceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-PublicIpAddress <PSPublicIpAddress>]
 [-Subnet <PSSubnet>] [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d787-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d787-105">DESCRIPTION</span></span>
<span data-ttu-id="2d787-106">Il cmdlet **New-AzPrivateLinkServiceIpConfig** crea una configurazione IP del servizio di collegamento privato.</span><span class="sxs-lookup"><span data-stu-id="2d787-106">The **New-AzPrivateLinkServiceIpConfig** cmdlet creates a private link service ip configuration.</span></span> <span data-ttu-id="2d787-107">Questa configurazione viene usata per l'origine NAT-ing il traffico in arrivo da endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="2d787-107">This configuration is used for source NAT-ing the incoming traffic from private endpoint.</span></span> 

## <span data-ttu-id="2d787-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2d787-108">EXAMPLES</span></span>

### <span data-ttu-id="2d787-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2d787-109">Example 1</span></span>
```
New-AzPrivateLinkServiceIpConfig -Name $IpConfigurationName -PrivateIpAddress "10.0.0.5" -Primary
```

<span data-ttu-id="2d787-110">Questo esempio crea una configurazione IP del servizio di collegamento privato in memoria.</span><span class="sxs-lookup"><span data-stu-id="2d787-110">This example create a private link service ip configuration in memory.</span></span>

## <span data-ttu-id="2d787-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2d787-111">PARAMETERS</span></span>

### <span data-ttu-id="2d787-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d787-112">-DefaultProfile</span></span>
<span data-ttu-id="2d787-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2d787-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d787-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d787-114">-Name</span></span>
<span data-ttu-id="2d787-115">Nome del IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d787-115">The name of the IpConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d787-116">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="2d787-116">-PrivateIpAddress</span></span>
<span data-ttu-id="2d787-117">Indirizzo IP privato di ipConfiguration se è specificato l'allocazione statica.</span><span class="sxs-lookup"><span data-stu-id="2d787-117">The private ip address of the ipConfiguration if static allocation is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d787-118">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="2d787-118">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="2d787-119">Versione IP della configurazione IP</span><span class="sxs-lookup"><span data-stu-id="2d787-119">The ip version of the ip configuration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d787-120">-Primaria</span><span class="sxs-lookup"><span data-stu-id="2d787-120">-Primary</span></span>
<span data-ttu-id="2d787-121">Indica che la configurazione IP corrente è primaria o meno.</span><span class="sxs-lookup"><span data-stu-id="2d787-121">Indicate current ip configuration is primary or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d787-122">-Subnet</span><span class="sxs-lookup"><span data-stu-id="2d787-122">-Subnet</span></span>
<span data-ttu-id="2d787-123">Subnet</span><span class="sxs-lookup"><span data-stu-id="2d787-123">Subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d787-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d787-124">CommonParameters</span></span>
<span data-ttu-id="2d787-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d787-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d787-126">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d787-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d787-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2d787-127">INPUTS</span></span>

### <span data-ttu-id="2d787-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2d787-128">None</span></span>

## <span data-ttu-id="2d787-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2d787-129">OUTPUTS</span></span>

### <span data-ttu-id="2d787-130">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkServiceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d787-130">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration</span></span>

## <span data-ttu-id="2d787-131">Note</span><span class="sxs-lookup"><span data-stu-id="2d787-131">NOTES</span></span>

## <span data-ttu-id="2d787-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2d787-132">RELATED LINKS</span></span>

[<span data-ttu-id="2d787-133">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2d787-133">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)
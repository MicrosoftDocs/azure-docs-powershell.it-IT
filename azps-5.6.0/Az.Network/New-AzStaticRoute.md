---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azstaticroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
ms.openlocfilehash: 2cf661ab2bcc531c0a88ae86934a53b212bb91d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953774"
---
# <span data-ttu-id="a7d0a-101">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="a7d0a-101">New-AzStaticRoute</span></span>

## <span data-ttu-id="a7d0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7d0a-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d0a-103">Crea un oggetto StaticRoute che può quindi essere aggiunto a un oggetto RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a7d0a-103">Creates a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="a7d0a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7d0a-104">SYNTAX</span></span>

```powershell
New-AzStaticRoute -Name <String> -AddressPrefix <String[]> -NextHopIpAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7d0a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a7d0a-105">DESCRIPTION</span></span>
<span data-ttu-id="a7d0a-106">Crea un oggetto StaticRoute.</span><span class="sxs-lookup"><span data-stu-id="a7d0a-106">Creates a StaticRoute object.</span></span>

## <span data-ttu-id="a7d0a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7d0a-107">EXAMPLES</span></span>

### <span data-ttu-id="a7d0a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a7d0a-108">Example 1</span></span>
```powershell
PS C:\> New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16") -NextHopIpAddress "10.90.0.5"

Name   AddressPrefixes              NextHopIpAddress
----   ---------------              ----------------
route1 {10.20.0.0/16, 10.30.0.0/16} 10.90.0.5
```

<span data-ttu-id="a7d0a-109">Il comando precedente creerà un oggetto StaticRoute che può quindi essere aggiunto a un oggetto RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a7d0a-109">The above command will create a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="a7d0a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7d0a-110">PARAMETERS</span></span>

### <span data-ttu-id="a7d0a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d0a-111">-DefaultProfile</span></span>
<span data-ttu-id="a7d0a-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7d0a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7d0a-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a7d0a-113">-AddressPrefix</span></span>
<span data-ttu-id="a7d0a-114">Elenco di prefissi di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="a7d0a-114">List of address prefixes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7d0a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a7d0a-115">-Name</span></span>
<span data-ttu-id="a7d0a-116">Nome della route.</span><span class="sxs-lookup"><span data-stu-id="a7d0a-116">The route name.</span></span>

```yaml
Type: String
Parameter Sets: (all)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7d0a-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="a7d0a-117">-NextHopIpAddress</span></span>
<span data-ttu-id="a7d0a-118">Indirizzo IP dell'hop successivo.</span><span class="sxs-lookup"><span data-stu-id="a7d0a-118">The next hop ip address.</span></span>

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

### <span data-ttu-id="a7d0a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d0a-119">CommonParameters</span></span>
<span data-ttu-id="a7d0a-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7d0a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d0a-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a7d0a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d0a-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="a7d0a-122">INPUTS</span></span>

### <span data-ttu-id="a7d0a-123">System.String</span><span class="sxs-lookup"><span data-stu-id="a7d0a-123">System.String</span></span>

## <span data-ttu-id="a7d0a-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7d0a-124">OUTPUTS</span></span>

### <span data-ttu-id="a7d0a-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="a7d0a-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="a7d0a-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="a7d0a-126">NOTES</span></span>

## <span data-ttu-id="a7d0a-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7d0a-127">RELATED LINKS</span></span>

[<span data-ttu-id="a7d0a-128">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7d0a-128">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azstaticroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzStaticRoute.md
ms.openlocfilehash: e4d9b8cd09aa1bf1528de1cd2179a76e7907e82b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187007"
---
# <span data-ttu-id="82093-101">New-AzStaticRoute</span><span class="sxs-lookup"><span data-stu-id="82093-101">New-AzStaticRoute</span></span>

## <span data-ttu-id="82093-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82093-102">SYNOPSIS</span></span>
<span data-ttu-id="82093-103">Crea un oggetto StaticRoute che può quindi essere aggiunto a un oggetto RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="82093-103">Creates a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="82093-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82093-104">SYNTAX</span></span>

```powershell
New-AzStaticRoute -Name <String> -AddressPrefix <String[]> -NextHopIpAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82093-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="82093-105">DESCRIPTION</span></span>
<span data-ttu-id="82093-106">Crea un oggetto StaticRoute.</span><span class="sxs-lookup"><span data-stu-id="82093-106">Creates a StaticRoute object.</span></span>

## <span data-ttu-id="82093-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82093-107">EXAMPLES</span></span>

### <span data-ttu-id="82093-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="82093-108">Example 1</span></span>
```powershell
PS C:\> New-AzStaticRoute -Name "route1" -AddressPrefix @("10.20.0.0/16", "10.30.0.0/16") -NextHopIpAddress "10.90.0.5"

Name   AddressPrefixes              NextHopIpAddress
----   ---------------              ----------------
route1 {10.20.0.0/16, 10.30.0.0/16} 10.90.0.5
```

<span data-ttu-id="82093-109">Il comando precedente creerà un oggetto StaticRoute che può quindi essere aggiunto a un oggetto RoutingConfiguration.</span><span class="sxs-lookup"><span data-stu-id="82093-109">The above command will create a StaticRoute object which can then be added to a RoutingConfiguration object.</span></span>

## <span data-ttu-id="82093-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82093-110">PARAMETERS</span></span>

### <span data-ttu-id="82093-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82093-111">-DefaultProfile</span></span>
<span data-ttu-id="82093-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="82093-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82093-113">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="82093-113">-AddressPrefix</span></span>
<span data-ttu-id="82093-114">Elenco di prefissi di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="82093-114">List of address prefixes.</span></span>

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

### <span data-ttu-id="82093-115">-Name</span><span class="sxs-lookup"><span data-stu-id="82093-115">-Name</span></span>
<span data-ttu-id="82093-116">Nome della route.</span><span class="sxs-lookup"><span data-stu-id="82093-116">The route name.</span></span>

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

### <span data-ttu-id="82093-117">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="82093-117">-NextHopIpAddress</span></span>
<span data-ttu-id="82093-118">Indirizzo IP dell'hop successivo.</span><span class="sxs-lookup"><span data-stu-id="82093-118">The next hop ip address.</span></span>

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

### <span data-ttu-id="82093-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82093-119">CommonParameters</span></span>
<span data-ttu-id="82093-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82093-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82093-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="82093-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82093-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="82093-122">INPUTS</span></span>

### <span data-ttu-id="82093-123">System.String</span><span class="sxs-lookup"><span data-stu-id="82093-123">System.String</span></span>

## <span data-ttu-id="82093-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82093-124">OUTPUTS</span></span>

### <span data-ttu-id="82093-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span><span class="sxs-lookup"><span data-stu-id="82093-125">Microsoft.Azure.Commands.Network.Models.PSStaticRoute</span></span>

## <span data-ttu-id="82093-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="82093-126">NOTES</span></span>

## <span data-ttu-id="82093-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82093-127">RELATED LINKS</span></span>

[<span data-ttu-id="82093-128">New-AzRoutingConfiguration</span><span class="sxs-lookup"><span data-stu-id="82093-128">New-AzRoutingConfiguration</span></span>](./New-AzRoutingConfiguration.md)

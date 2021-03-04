---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: d16b5d916f3a807de818c58de94f7f0841e04d17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956974"
---
# <span data-ttu-id="8af09-101">Get-AzExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="8af09-101">Get-AzExpressRoutePortsLocation</span></span>

## <span data-ttu-id="8af09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8af09-102">SYNOPSIS</span></span>
<span data-ttu-id="8af09-103">Ottiene le posizioni in cui sono disponibili le risorse ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="8af09-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

## <span data-ttu-id="8af09-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8af09-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8af09-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8af09-105">DESCRIPTION</span></span>
<span data-ttu-id="8af09-106">Il cmdlet **Get-AzExpressRoutePortsLocation** viene usato per recuperare le posizioni in cui sono disponibili le risorse di ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="8af09-106">The **Get-AzExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="8af09-107">Dato un percorso specifico come input, il cmdlet visualizza i dettagli della posizione, ad esempio l'elenco di larghezze di banda disponibili in tale posizione.</span><span class="sxs-lookup"><span data-stu-id="8af09-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>

## <span data-ttu-id="8af09-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8af09-108">EXAMPLES</span></span>

### <span data-ttu-id="8af09-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8af09-109">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

<span data-ttu-id="8af09-110">Elenca le posizioni in cui sono disponibili le risorse ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="8af09-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="8af09-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8af09-111">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="8af09-112">Elenca le larghezze di banda di ExpressRoutePort disponibili nella posizione $loc.</span><span class="sxs-lookup"><span data-stu-id="8af09-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="8af09-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8af09-113">PARAMETERS</span></span>

### <span data-ttu-id="8af09-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8af09-114">-DefaultProfile</span></span>
<span data-ttu-id="8af09-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8af09-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8af09-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="8af09-116">-LocationName</span></span>
<span data-ttu-id="8af09-117">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="8af09-117">The name of the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8af09-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8af09-118">CommonParameters</span></span>
<span data-ttu-id="8af09-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8af09-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8af09-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8af09-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8af09-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="8af09-121">INPUTS</span></span>

### <span data-ttu-id="8af09-122">System.String</span><span class="sxs-lookup"><span data-stu-id="8af09-122">System.String</span></span>

## <span data-ttu-id="8af09-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8af09-123">OUTPUTS</span></span>

### <span data-ttu-id="8af09-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="8af09-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="8af09-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="8af09-125">NOTES</span></span>

## <span data-ttu-id="8af09-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8af09-126">RELATED LINKS</span></span>

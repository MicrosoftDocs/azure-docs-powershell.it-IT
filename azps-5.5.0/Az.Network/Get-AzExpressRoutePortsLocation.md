---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 918ef18717cb09bad28ee10b91f635181dd5b3cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189783"
---
# <span data-ttu-id="b82cb-101">Get-AzExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="b82cb-101">Get-AzExpressRoutePortsLocation</span></span>

## <span data-ttu-id="b82cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b82cb-102">SYNOPSIS</span></span>
<span data-ttu-id="b82cb-103">Ottiene le posizioni in cui sono disponibili le risorse ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b82cb-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

## <span data-ttu-id="b82cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b82cb-104">SYNTAX</span></span>

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b82cb-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b82cb-105">DESCRIPTION</span></span>
<span data-ttu-id="b82cb-106">Il cmdlet **Get-AzExpressRoutePortsLocation** viene usato per recuperare le posizioni in cui sono disponibili le risorse di ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b82cb-106">The **Get-AzExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="b82cb-107">Dato un percorso specifico come input, il cmdlet visualizza i dettagli della posizione, ad esempio l'elenco di larghezze di banda disponibili in tale posizione.</span><span class="sxs-lookup"><span data-stu-id="b82cb-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>

## <span data-ttu-id="b82cb-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b82cb-108">EXAMPLES</span></span>

### <span data-ttu-id="b82cb-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b82cb-109">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

<span data-ttu-id="b82cb-110">Elenca le posizioni in cui sono disponibili le risorse ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b82cb-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="b82cb-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b82cb-111">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="b82cb-112">Elenca le larghezze di banda di ExpressRoutePort disponibili nella posizione $loc.</span><span class="sxs-lookup"><span data-stu-id="b82cb-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="b82cb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b82cb-113">PARAMETERS</span></span>

### <span data-ttu-id="b82cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b82cb-114">-DefaultProfile</span></span>
<span data-ttu-id="b82cb-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b82cb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b82cb-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="b82cb-116">-LocationName</span></span>
<span data-ttu-id="b82cb-117">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="b82cb-117">The name of the location.</span></span>

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

### <span data-ttu-id="b82cb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b82cb-118">CommonParameters</span></span>
<span data-ttu-id="b82cb-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b82cb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b82cb-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b82cb-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b82cb-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="b82cb-121">INPUTS</span></span>

### <span data-ttu-id="b82cb-122">System.String</span><span class="sxs-lookup"><span data-stu-id="b82cb-122">System.String</span></span>

## <span data-ttu-id="b82cb-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b82cb-123">OUTPUTS</span></span>

### <span data-ttu-id="b82cb-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="b82cb-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="b82cb-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="b82cb-125">NOTES</span></span>

## <span data-ttu-id="b82cb-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b82cb-126">RELATED LINKS</span></span>

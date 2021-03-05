---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 04da18bcd50fa547f1a59142682c93b4e3e5ab62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974782"
---
# <span data-ttu-id="aaa3f-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="aaa3f-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="aaa3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaa3f-102">SYNOPSIS</span></span>
<span data-ttu-id="aaa3f-103">Crea una corrispondenza della risposta di integrità risposta usata da Health Gateway per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="aaa3f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aaa3f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aaa3f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aaa3f-105">DESCRIPTION</span></span>
<span data-ttu-id="aaa3f-106">Il cmdlet **Add-AzApplicationGatewayProbeHealthResponseMatch crea** una corrispondenza health response usata da Health Gateway per un gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="aaa3f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aaa3f-107">EXAMPLES</span></span>

### <span data-ttu-id="aaa3f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aaa3f-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="aaa3f-109">Questo comando crea una corrispondenza della risposta all'integrità che può essere passata aConfig come parametro.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="aaa3f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aaa3f-110">PARAMETERS</span></span>

### <span data-ttu-id="aaa3f-111">-Body</span><span class="sxs-lookup"><span data-stu-id="aaa3f-111">-Body</span></span>
<span data-ttu-id="aaa3f-112">Corpo che deve essere contenuto nella risposta all'integrità.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="aaa3f-113">Il valore predefinito è vuoto</span><span class="sxs-lookup"><span data-stu-id="aaa3f-113">Default value is empty</span></span>

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

### <span data-ttu-id="aaa3f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaa3f-114">-DefaultProfile</span></span>
<span data-ttu-id="aaa3f-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aaa3f-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="aaa3f-116">-StatusCode</span></span>
<span data-ttu-id="aaa3f-117">Intervalli consentiti di codici di stato integri. L'intervallo predefinito di codici di stato integri è 200 - 399</span><span class="sxs-lookup"><span data-stu-id="aaa3f-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa3f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaa3f-118">CommonParameters</span></span>
<span data-ttu-id="aaa3f-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaa3f-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaa3f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaa3f-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="aaa3f-121">INPUTS</span></span>

### <span data-ttu-id="aaa3f-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="aaa3f-122">None</span></span>

## <span data-ttu-id="aaa3f-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aaa3f-123">OUTPUTS</span></span>

### <span data-ttu-id="aaa3f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthMatch</span><span class="sxs-lookup"><span data-stu-id="aaa3f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="aaa3f-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="aaa3f-125">NOTES</span></span>

## <span data-ttu-id="aaa3f-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aaa3f-126">RELATED LINKS</span></span>

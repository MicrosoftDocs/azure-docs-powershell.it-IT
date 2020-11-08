---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: edc0309b5e1a0c8b17d400e965074d38ca02bb80
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022748"
---
# <span data-ttu-id="68f48-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="68f48-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="68f48-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68f48-102">SYNOPSIS</span></span>
<span data-ttu-id="68f48-103">Crea una corrispondenza di risposta della sonda di integrità usata da Probe integrità per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="68f48-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="68f48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68f48-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>] [-StatusCode <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68f48-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68f48-105">DESCRIPTION</span></span>
<span data-ttu-id="68f48-106">**Il cmdlet Add-AzApplicationGatewayProbeHealthResponseMatch** crea una corrispondenza di risposta della sonda di integrità usata da Probe integrità per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="68f48-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="68f48-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68f48-107">EXAMPLES</span></span>

### <span data-ttu-id="68f48-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="68f48-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="68f48-109">Questo comando crea una corrispondenza di risposta sanitaria che può essere passata a ProbeConfig come parametro.</span><span class="sxs-lookup"><span data-stu-id="68f48-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="68f48-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68f48-110">PARAMETERS</span></span>

### <span data-ttu-id="68f48-111">-Body</span><span class="sxs-lookup"><span data-stu-id="68f48-111">-Body</span></span>
<span data-ttu-id="68f48-112">Corpo che deve essere contenuto nella risposta di integrità.</span><span class="sxs-lookup"><span data-stu-id="68f48-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="68f48-113">Il valore predefinito è Empty</span><span class="sxs-lookup"><span data-stu-id="68f48-113">Default value is empty</span></span>

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

### <span data-ttu-id="68f48-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68f48-114">-DefaultProfile</span></span>
<span data-ttu-id="68f48-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68f48-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68f48-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="68f48-116">-StatusCode</span></span>
<span data-ttu-id="68f48-117">Intervalli consentiti di codici di stato sani. L'intervallo predefinito di codici di stato sani è 200-399</span><span class="sxs-lookup"><span data-stu-id="68f48-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="68f48-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68f48-118">CommonParameters</span></span>
<span data-ttu-id="68f48-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68f48-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68f48-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68f48-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68f48-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68f48-121">INPUTS</span></span>

### <span data-ttu-id="68f48-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="68f48-122">None</span></span>

## <span data-ttu-id="68f48-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68f48-123">OUTPUTS</span></span>

### <span data-ttu-id="68f48-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="68f48-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="68f48-125">Note</span><span class="sxs-lookup"><span data-stu-id="68f48-125">NOTES</span></span>

## <span data-ttu-id="68f48-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68f48-126">RELATED LINKS</span></span>

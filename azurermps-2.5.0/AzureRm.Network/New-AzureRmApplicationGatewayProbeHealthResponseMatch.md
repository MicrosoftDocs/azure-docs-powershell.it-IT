---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobehealthresponsematch
schema: 2.0.0
ms.openlocfilehash: 8781b52c3ed50a2a533b90815f1637ebcfe6df52
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865751"
---
# <span data-ttu-id="2ecb1-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="2ecb1-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="2ecb1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ecb1-102">SYNOPSIS</span></span>
<span data-ttu-id="2ecb1-103">Crea una corrispondenza di risposta della sonda di integrità usata da Probe integrità per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2ecb1-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ecb1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ecb1-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeHealthResponseMatch [-Body <String>]
 [-StatusCode <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ecb1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ecb1-105">DESCRIPTION</span></span>
<span data-ttu-id="2ecb1-106">**Il cmdlet Add-AzureRmApplicationGatewayProbeHealthResponseMatch** crea una corrispondenza di risposta della sonda di integrità usata da Probe integrità per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2ecb1-106">**The Add-AzureRmApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="2ecb1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ecb1-107">EXAMPLES</span></span>

### <span data-ttu-id="2ecb1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2ecb1-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzureRmApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="2ecb1-109">Questo comando crea una corrispondenza di risposta sanitaria che può essere passata a ProbeConfig come parametro.</span><span class="sxs-lookup"><span data-stu-id="2ecb1-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="2ecb1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ecb1-110">PARAMETERS</span></span>

### <span data-ttu-id="2ecb1-111">-Body</span><span class="sxs-lookup"><span data-stu-id="2ecb1-111">-Body</span></span>
<span data-ttu-id="2ecb1-112">Corpo che deve essere contenuto nella risposta di integrità.</span><span class="sxs-lookup"><span data-stu-id="2ecb1-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="2ecb1-113">Il valore predefinito è Empty</span><span class="sxs-lookup"><span data-stu-id="2ecb1-113">Default value is empty</span></span>

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

### <span data-ttu-id="2ecb1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ecb1-114">-DefaultProfile</span></span>
<span data-ttu-id="2ecb1-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ecb1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ecb1-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="2ecb1-116">-StatusCode</span></span>
<span data-ttu-id="2ecb1-117">Intervalli consentiti di codici di stato sani. L'intervallo predefinito di codici di stato sani è 200-399</span><span class="sxs-lookup"><span data-stu-id="2ecb1-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ecb1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ecb1-118">CommonParameters</span></span>
<span data-ttu-id="2ecb1-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ecb1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ecb1-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ecb1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ecb1-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ecb1-121">INPUTS</span></span>

### <span data-ttu-id="2ecb1-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2ecb1-122">None</span></span>

## <span data-ttu-id="2ecb1-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ecb1-123">OUTPUTS</span></span>

### <span data-ttu-id="2ecb1-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="2ecb1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="2ecb1-125">Note</span><span class="sxs-lookup"><span data-stu-id="2ecb1-125">NOTES</span></span>

## <span data-ttu-id="2ecb1-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ecb1-126">RELATED LINKS</span></span>


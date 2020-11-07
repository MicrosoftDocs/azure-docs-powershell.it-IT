---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 6b54c300eb6e37544246b785fe30b2a3dcb67b9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687510"
---
# <span data-ttu-id="f6d34-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="f6d34-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="f6d34-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f6d34-102">SYNOPSIS</span></span>
<span data-ttu-id="f6d34-103">Crea una corrispondenza di risposta della sonda di integrità usata da Probe integrità per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f6d34-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6d34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6d34-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeHealthResponseMatch [-Body <String>]
 [-StatusCode <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6d34-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6d34-105">DESCRIPTION</span></span>
<span data-ttu-id="f6d34-106">**Il cmdlet Add-AzureRmApplicationGatewayProbeHealthResponseMatch** crea una corrispondenza di risposta della sonda di integrità usata da Probe integrità per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f6d34-106">**The Add-AzureRmApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="f6d34-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6d34-107">EXAMPLES</span></span>

### <span data-ttu-id="f6d34-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f6d34-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzureRmApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="f6d34-109">Questo comando crea una corrispondenza di risposta sanitaria che può essere passata a ProbeConfig come parametro.</span><span class="sxs-lookup"><span data-stu-id="f6d34-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="f6d34-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f6d34-110">PARAMETERS</span></span>

### <span data-ttu-id="f6d34-111">-Body</span><span class="sxs-lookup"><span data-stu-id="f6d34-111">-Body</span></span>
<span data-ttu-id="f6d34-112">Corpo che deve essere contenuto nella risposta di integrità.</span><span class="sxs-lookup"><span data-stu-id="f6d34-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="f6d34-113">Il valore predefinito è Empty</span><span class="sxs-lookup"><span data-stu-id="f6d34-113">Default value is empty</span></span>

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

### <span data-ttu-id="f6d34-114">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="f6d34-114">-StatusCode</span></span>
<span data-ttu-id="f6d34-115">Intervalli consentiti di codici di stato sani. L'intervallo predefinito di codici di stato sani è 200-399</span><span class="sxs-lookup"><span data-stu-id="f6d34-115">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="f6d34-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6d34-116">-DefaultProfile</span></span>
<span data-ttu-id="f6d34-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f6d34-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6d34-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6d34-118">CommonParameters</span></span>
<span data-ttu-id="f6d34-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6d34-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6d34-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6d34-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6d34-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f6d34-121">INPUTS</span></span>

### <span data-ttu-id="f6d34-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f6d34-122">None</span></span>

## <span data-ttu-id="f6d34-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6d34-123">OUTPUTS</span></span>

### <span data-ttu-id="f6d34-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="f6d34-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="f6d34-125">Note</span><span class="sxs-lookup"><span data-stu-id="f6d34-125">NOTES</span></span>

## <span data-ttu-id="f6d34-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6d34-126">RELATED LINKS</span></span>


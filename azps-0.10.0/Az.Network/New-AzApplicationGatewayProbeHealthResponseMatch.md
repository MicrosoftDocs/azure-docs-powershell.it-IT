---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 41693da553178bdd45d19da498a5774ef8d2fa60
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860558"
---
# <span data-ttu-id="71af1-101">New-AzApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="71af1-101">New-AzApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="71af1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71af1-102">SYNOPSIS</span></span>
<span data-ttu-id="71af1-103">Crea una corrispondenza di risposta della sonda di integrità usata da Probe integrità per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="71af1-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="71af1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71af1-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeHealthResponseMatch [-Body <String>]
 [-StatusCode <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="71af1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71af1-105">DESCRIPTION</span></span>
<span data-ttu-id="71af1-106">**Il cmdlet Add-AzApplicationGatewayProbeHealthResponseMatch** crea una corrispondenza di risposta della sonda di integrità usata da Probe integrità per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="71af1-106">**The Add-AzApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="71af1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71af1-107">EXAMPLES</span></span>

### <span data-ttu-id="71af1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="71af1-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="71af1-109">Questo comando crea una corrispondenza di risposta sanitaria che può essere passata a ProbeConfig come parametro.</span><span class="sxs-lookup"><span data-stu-id="71af1-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="71af1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71af1-110">PARAMETERS</span></span>

### <span data-ttu-id="71af1-111">-Body</span><span class="sxs-lookup"><span data-stu-id="71af1-111">-Body</span></span>
<span data-ttu-id="71af1-112">Corpo che deve essere contenuto nella risposta di integrità.</span><span class="sxs-lookup"><span data-stu-id="71af1-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="71af1-113">Il valore predefinito è Empty</span><span class="sxs-lookup"><span data-stu-id="71af1-113">Default value is empty</span></span>

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

### <span data-ttu-id="71af1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71af1-114">-DefaultProfile</span></span>
<span data-ttu-id="71af1-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71af1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71af1-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="71af1-116">-StatusCode</span></span>
<span data-ttu-id="71af1-117">Intervalli consentiti di codici di stato sani. L'intervallo predefinito di codici di stato sani è 200-399</span><span class="sxs-lookup"><span data-stu-id="71af1-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

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

### <span data-ttu-id="71af1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71af1-118">CommonParameters</span></span>
<span data-ttu-id="71af1-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71af1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71af1-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71af1-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71af1-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71af1-121">INPUTS</span></span>

### <span data-ttu-id="71af1-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="71af1-122">None</span></span>

## <span data-ttu-id="71af1-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71af1-123">OUTPUTS</span></span>

### <span data-ttu-id="71af1-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="71af1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="71af1-125">Note</span><span class="sxs-lookup"><span data-stu-id="71af1-125">NOTES</span></span>

## <span data-ttu-id="71af1-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71af1-126">RELATED LINKS</span></span>


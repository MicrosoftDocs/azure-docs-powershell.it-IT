---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: f2175583aaaf3af04120e22e32db79d7b20f1e30
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189879"
---
# <span data-ttu-id="1c73c-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="1c73c-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="1c73c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c73c-102">SYNOPSIS</span></span>
<span data-ttu-id="1c73c-103">Recupera tutte le opzioni SSL disponibili per i criteri SSL per Gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="1c73c-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="1c73c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c73c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c73c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1c73c-105">DESCRIPTION</span></span>
<span data-ttu-id="1c73c-106">Il cmdlet **Get-AzApplicationGatewayAvailableSslOption** ottiene tutte le opzioni SSL disponibili per i criteri SSL</span><span class="sxs-lookup"><span data-stu-id="1c73c-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="1c73c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c73c-107">EXAMPLES</span></span>

### <span data-ttu-id="1c73c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1c73c-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="1c73c-109">Questo comando restituisce tutte le opzioni SSL disponibili per i criteri SSL.</span><span class="sxs-lookup"><span data-stu-id="1c73c-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="1c73c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c73c-110">PARAMETERS</span></span>

### <span data-ttu-id="1c73c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c73c-111">-DefaultProfile</span></span>
<span data-ttu-id="1c73c-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c73c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c73c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c73c-113">CommonParameters</span></span>
<span data-ttu-id="1c73c-114">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c73c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c73c-115">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1c73c-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c73c-116">INPUT</span><span class="sxs-lookup"><span data-stu-id="1c73c-116">INPUTS</span></span>

### <span data-ttu-id="1c73c-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1c73c-117">None</span></span>

## <span data-ttu-id="1c73c-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c73c-118">OUTPUTS</span></span>

### <span data-ttu-id="1c73c-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="1c73c-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="1c73c-120">NOTE</span><span class="sxs-lookup"><span data-stu-id="1c73c-120">NOTES</span></span>

## <span data-ttu-id="1c73c-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c73c-121">RELATED LINKS</span></span>

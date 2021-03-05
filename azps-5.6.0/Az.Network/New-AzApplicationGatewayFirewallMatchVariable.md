---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: 824c1c4e98fca6b6f7d2ff3df9217cb000eeaf21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015069"
---
# <span data-ttu-id="b1b70-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="b1b70-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="b1b70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1b70-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b70-103">Crea una variabile di corrispondenza per la condizione del firewall.</span><span class="sxs-lookup"><span data-stu-id="b1b70-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="b1b70-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1b70-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1b70-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b1b70-105">DESCRIPTION</span></span>
<span data-ttu-id="b1b70-106">**New-AzApplicationGatewayFirewallMatchVariable** crea una variabile di corrispondenza per la condizione del firewall.</span><span class="sxs-lookup"><span data-stu-id="b1b70-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="b1b70-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1b70-107">EXAMPLES</span></span>

### <span data-ttu-id="b1b70-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b1b70-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="b1b70-109">Il comando crea una nuova variabile corrispondenza con il nome delle intestazioni delle richieste e il selettore è il campo Content-Length.</span><span class="sxs-lookup"><span data-stu-id="b1b70-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="b1b70-110">La nuova variabile di corrispondenza viene salvata in $variable.</span><span class="sxs-lookup"><span data-stu-id="b1b70-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="b1b70-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1b70-111">PARAMETERS</span></span>

### <span data-ttu-id="b1b70-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1b70-112">-DefaultProfile</span></span>
<span data-ttu-id="b1b70-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1b70-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1b70-114">-Selettore</span><span class="sxs-lookup"><span data-stu-id="b1b70-114">-Selector</span></span>
<span data-ttu-id="b1b70-115">Descrive il campo della raccolta matchVariable.</span><span class="sxs-lookup"><span data-stu-id="b1b70-115">Describes field of the matchVariable collection.</span></span>

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

### <span data-ttu-id="b1b70-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="b1b70-116">-VariableName</span></span>
<span data-ttu-id="b1b70-117">Variabile Match.</span><span class="sxs-lookup"><span data-stu-id="b1b70-117">Match Variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeaders, RequestBody, RequestCookies

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b70-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b70-118">CommonParameters</span></span>
<span data-ttu-id="b1b70-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1b70-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b70-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1b70-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b70-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="b1b70-121">INPUTS</span></span>

### <span data-ttu-id="b1b70-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b1b70-122">None</span></span>

## <span data-ttu-id="b1b70-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1b70-123">OUTPUTS</span></span>

### <span data-ttu-id="b1b70-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="b1b70-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="b1b70-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="b1b70-125">NOTES</span></span>

## <span data-ttu-id="b1b70-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1b70-126">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: c3ff96a2c1d06fdfba5879244b058ef1a7845f40
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202959"
---
# <span data-ttu-id="e1b94-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="e1b94-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="e1b94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1b94-102">SYNOPSIS</span></span>
<span data-ttu-id="e1b94-103">Crea una variabile di corrispondenza per la condizione del firewall.</span><span class="sxs-lookup"><span data-stu-id="e1b94-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="e1b94-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1b94-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1b94-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e1b94-105">DESCRIPTION</span></span>
<span data-ttu-id="e1b94-106">**New-AzApplicationGatewayFirewallMatchVariable** crea una variabile di corrispondenza per la condizione del firewall.</span><span class="sxs-lookup"><span data-stu-id="e1b94-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="e1b94-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1b94-107">EXAMPLES</span></span>

### <span data-ttu-id="e1b94-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e1b94-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="e1b94-109">Il comando crea una nuova variabile corrispondenza con il nome delle intestazioni delle richieste e il selettore è il campo Content-Length.</span><span class="sxs-lookup"><span data-stu-id="e1b94-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="e1b94-110">La nuova variabile di corrispondenza viene salvata in $variable.</span><span class="sxs-lookup"><span data-stu-id="e1b94-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="e1b94-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1b94-111">PARAMETERS</span></span>

### <span data-ttu-id="e1b94-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1b94-112">-DefaultProfile</span></span>
<span data-ttu-id="e1b94-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1b94-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1b94-114">-Selettore</span><span class="sxs-lookup"><span data-stu-id="e1b94-114">-Selector</span></span>
<span data-ttu-id="e1b94-115">Descrive il campo della raccolta matchVariable.</span><span class="sxs-lookup"><span data-stu-id="e1b94-115">Describes field of the matchVariable collection.</span></span>

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

### <span data-ttu-id="e1b94-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="e1b94-116">-VariableName</span></span>
<span data-ttu-id="e1b94-117">Variabile Match.</span><span class="sxs-lookup"><span data-stu-id="e1b94-117">Match Variable.</span></span>

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

### <span data-ttu-id="e1b94-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1b94-118">CommonParameters</span></span>
<span data-ttu-id="e1b94-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1b94-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1b94-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1b94-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1b94-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="e1b94-121">INPUTS</span></span>

### <span data-ttu-id="e1b94-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e1b94-122">None</span></span>

## <span data-ttu-id="e1b94-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1b94-123">OUTPUTS</span></span>

### <span data-ttu-id="e1b94-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="e1b94-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="e1b94-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="e1b94-125">NOTES</span></span>

## <span data-ttu-id="e1b94-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1b94-126">RELATED LINKS</span></span>

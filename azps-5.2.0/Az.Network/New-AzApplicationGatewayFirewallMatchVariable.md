---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: c3ff96a2c1d06fdfba5879244b058ef1a7845f40
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346636"
---
# <span data-ttu-id="bd441-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="bd441-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="bd441-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bd441-102">SYNOPSIS</span></span>
<span data-ttu-id="bd441-103">Crea una variabile di corrispondenza per la condizione del firewall.</span><span class="sxs-lookup"><span data-stu-id="bd441-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="bd441-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd441-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd441-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd441-105">DESCRIPTION</span></span>
<span data-ttu-id="bd441-106">La **nuova AzApplicationGatewayFirewallMatchVariable** crea una variabile di corrispondenza per la condizione del firewall.</span><span class="sxs-lookup"><span data-stu-id="bd441-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="bd441-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd441-107">EXAMPLES</span></span>

### <span data-ttu-id="bd441-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bd441-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="bd441-109">Il comando crea una nuova variabile di corrispondenza con il nome delle intestazioni della richiesta e il selettore è il campo Content-Length.</span><span class="sxs-lookup"><span data-stu-id="bd441-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="bd441-110">La nuova variabile di corrispondenza viene salvata in $variable.</span><span class="sxs-lookup"><span data-stu-id="bd441-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="bd441-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bd441-111">PARAMETERS</span></span>

### <span data-ttu-id="bd441-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd441-112">-DefaultProfile</span></span>
<span data-ttu-id="bd441-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bd441-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd441-114">-Selector</span><span class="sxs-lookup"><span data-stu-id="bd441-114">-Selector</span></span>
<span data-ttu-id="bd441-115">Descrive il campo della raccolta matchVariable.</span><span class="sxs-lookup"><span data-stu-id="bd441-115">Describes field of the matchVariable collection.</span></span>

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

### <span data-ttu-id="bd441-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="bd441-116">-VariableName</span></span>
<span data-ttu-id="bd441-117">Associa variabile.</span><span class="sxs-lookup"><span data-stu-id="bd441-117">Match Variable.</span></span>

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

### <span data-ttu-id="bd441-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd441-118">CommonParameters</span></span>
<span data-ttu-id="bd441-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd441-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd441-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd441-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd441-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bd441-121">INPUTS</span></span>

### <span data-ttu-id="bd441-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bd441-122">None</span></span>

## <span data-ttu-id="bd441-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd441-123">OUTPUTS</span></span>

### <span data-ttu-id="bd441-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="bd441-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="bd441-125">Note</span><span class="sxs-lookup"><span data-stu-id="bd441-125">NOTES</span></span>

## <span data-ttu-id="bd441-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd441-126">RELATED LINKS</span></span>

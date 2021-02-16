---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 68ab3fbd87e5fe28fffdd0f6d769fb21d0ce9e6e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398088"
---
# <span data-ttu-id="fc533-101">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc533-101">New-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="fc533-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc533-102">SYNOPSIS</span></span>
<span data-ttu-id="fc533-103">Crea una nuova configurazione di autenticazione client per il profilo SSL.</span><span class="sxs-lookup"><span data-stu-id="fc533-103">Creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="fc533-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc533-104">SYNTAX</span></span>

```
New-AzApplicationGatewayClientAuthConfiguration [-VerifyClientCertIssuerDN]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc533-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fc533-105">DESCRIPTION</span></span>
<span data-ttu-id="fc533-106">Il cmdlet **New-AzApplicationGatewayClientAuthConfiguration crea** una nuova configurazione di autenticazione client per il profilo SSL.</span><span class="sxs-lookup"><span data-stu-id="fc533-106">The **New-AzApplicationGatewayClientAuthConfiguration** cmdlet creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="fc533-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc533-107">EXAMPLES</span></span>

### <span data-ttu-id="fc533-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fc533-108">Example 1</span></span>
```powershell
PS C:\> $clientAuthConfig = New-AzApplicationGatewayClientAuthConfiguration -VerifyClientCertIssuerDN
```

<span data-ttu-id="fc533-109">Il comando crea una nuova configurazione di autenticazione client e la archivia in $clientAuthConfig variabile da usare in un profilo SSL.</span><span class="sxs-lookup"><span data-stu-id="fc533-109">The command create a new client auth configuration and stores it in $clientAuthConfig variable to be used in a SSL profile.</span></span> 

## <span data-ttu-id="fc533-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc533-110">PARAMETERS</span></span>

### <span data-ttu-id="fc533-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc533-111">-DefaultProfile</span></span>
<span data-ttu-id="fc533-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc533-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc533-113">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="fc533-113">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="fc533-114">Verificare il nome dell'autorità di certificazione client.</span><span class="sxs-lookup"><span data-stu-id="fc533-114">Verify client certificate issuer name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc533-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc533-115">CommonParameters</span></span>
<span data-ttu-id="fc533-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc533-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc533-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fc533-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc533-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="fc533-118">INPUTS</span></span>

### <span data-ttu-id="fc533-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fc533-119">None</span></span>

## <span data-ttu-id="fc533-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc533-120">OUTPUTS</span></span>

### <span data-ttu-id="fc533-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc533-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="fc533-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="fc533-122">NOTES</span></span>

## <span data-ttu-id="fc533-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc533-123">RELATED LINKS</span></span>


[<span data-ttu-id="fc533-124">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc533-124">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="fc533-125">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc533-125">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="fc533-126">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc533-126">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)

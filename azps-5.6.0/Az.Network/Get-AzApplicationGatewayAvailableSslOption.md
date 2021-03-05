---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: 8d2022f79dff5263f07737d525169dad3566fcda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003645"
---
# <span data-ttu-id="4ea66-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="4ea66-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="4ea66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ea66-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea66-103">Recupera tutte le opzioni SSL disponibili per i criteri SSL per Gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="4ea66-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="4ea66-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ea66-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ea66-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4ea66-105">DESCRIPTION</span></span>
<span data-ttu-id="4ea66-106">Il cmdlet **Get-AzApplicationGatewayAvailableSslOption** ottiene tutte le opzioni SSL disponibili per i criteri SSL</span><span class="sxs-lookup"><span data-stu-id="4ea66-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="4ea66-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ea66-107">EXAMPLES</span></span>

### <span data-ttu-id="4ea66-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4ea66-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="4ea66-109">Questo comando restituisce tutte le opzioni SSL disponibili per i criteri SSL.</span><span class="sxs-lookup"><span data-stu-id="4ea66-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="4ea66-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ea66-110">PARAMETERS</span></span>

### <span data-ttu-id="4ea66-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea66-111">-DefaultProfile</span></span>
<span data-ttu-id="4ea66-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea66-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ea66-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea66-113">CommonParameters</span></span>
<span data-ttu-id="4ea66-114">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ea66-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea66-115">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4ea66-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea66-116">INPUT</span><span class="sxs-lookup"><span data-stu-id="4ea66-116">INPUTS</span></span>

### <span data-ttu-id="4ea66-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4ea66-117">None</span></span>

## <span data-ttu-id="4ea66-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ea66-118">OUTPUTS</span></span>

### <span data-ttu-id="4ea66-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="4ea66-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="4ea66-120">NOTE</span><span class="sxs-lookup"><span data-stu-id="4ea66-120">NOTES</span></span>

## <span data-ttu-id="4ea66-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ea66-121">RELATED LINKS</span></span>

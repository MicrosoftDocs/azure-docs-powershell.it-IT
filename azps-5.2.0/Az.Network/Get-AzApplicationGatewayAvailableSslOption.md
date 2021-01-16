---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: f2175583aaaf3af04120e22e32db79d7b20f1e30
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354124"
---
# <span data-ttu-id="a44ff-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="a44ff-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="a44ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a44ff-102">SYNOPSIS</span></span>
<span data-ttu-id="a44ff-103">Ottiene tutte le opzioni SSL disponibili per i criteri SSL per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a44ff-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="a44ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a44ff-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a44ff-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a44ff-105">DESCRIPTION</span></span>
<span data-ttu-id="a44ff-106">Il cmdlet **Get-AzApplicationGatewayAvailableSslOption** ottiene tutte le opzioni SSL disponibili per i criteri SSL</span><span class="sxs-lookup"><span data-stu-id="a44ff-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="a44ff-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a44ff-107">EXAMPLES</span></span>

### <span data-ttu-id="a44ff-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a44ff-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="a44ff-109">Questi comandi restituiscono tutte le opzioni SSL disponibili per i criteri SSL.</span><span class="sxs-lookup"><span data-stu-id="a44ff-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="a44ff-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a44ff-110">PARAMETERS</span></span>

### <span data-ttu-id="a44ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a44ff-111">-DefaultProfile</span></span>
<span data-ttu-id="a44ff-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a44ff-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a44ff-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a44ff-113">CommonParameters</span></span>
<span data-ttu-id="a44ff-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a44ff-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a44ff-115">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a44ff-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a44ff-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a44ff-116">INPUTS</span></span>

### <span data-ttu-id="a44ff-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a44ff-117">None</span></span>

## <span data-ttu-id="a44ff-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a44ff-118">OUTPUTS</span></span>

### <span data-ttu-id="a44ff-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="a44ff-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="a44ff-120">Note</span><span class="sxs-lookup"><span data-stu-id="a44ff-120">NOTES</span></span>

## <span data-ttu-id="a44ff-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a44ff-121">RELATED LINKS</span></span>

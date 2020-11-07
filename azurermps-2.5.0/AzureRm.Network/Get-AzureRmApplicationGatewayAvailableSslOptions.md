---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablessloptions
schema: 2.0.0
ms.openlocfilehash: 023b2a43114fe47b50956e7f4626a75706e914f5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866311"
---
# <span data-ttu-id="c9d27-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="c9d27-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="c9d27-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9d27-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d27-103">Ottiene tutte le opzioni SSL disponibili per i criteri SSL per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9d27-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9d27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9d27-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableSslOptions [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9d27-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9d27-105">DESCRIPTION</span></span>
<span data-ttu-id="c9d27-106">Il cmdlet **Get-AzureRmApplicationGatewayAvailableSslOptions** ottiene tutte le opzioni SSL disponibili per i criteri SSL</span><span class="sxs-lookup"><span data-stu-id="c9d27-106">The **Get-AzureRmApplicationGatewayAvailableSslOptions** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="c9d27-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9d27-107">EXAMPLES</span></span>

### <span data-ttu-id="c9d27-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c9d27-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzureRmApplicationGatewayAvailableSslOptions
```

<span data-ttu-id="c9d27-109">Questi comandi restituiscono tutte le opzioni SSL disponibili per i criteri SSL.</span><span class="sxs-lookup"><span data-stu-id="c9d27-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="c9d27-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9d27-110">PARAMETERS</span></span>

### <span data-ttu-id="c9d27-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d27-111">-DefaultProfile</span></span>
<span data-ttu-id="c9d27-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9d27-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9d27-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d27-113">CommonParameters</span></span>
<span data-ttu-id="c9d27-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9d27-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d27-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9d27-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d27-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9d27-116">INPUTS</span></span>

### <span data-ttu-id="c9d27-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c9d27-117">None</span></span>

## <span data-ttu-id="c9d27-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9d27-118">OUTPUTS</span></span>

### <span data-ttu-id="c9d27-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="c9d27-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="c9d27-120">Note</span><span class="sxs-lookup"><span data-stu-id="c9d27-120">NOTES</span></span>

## <span data-ttu-id="c9d27-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9d27-121">RELATED LINKS</span></span>


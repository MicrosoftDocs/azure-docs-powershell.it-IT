---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
ms.openlocfilehash: 60e380ffd046c61abb218395a838c6e0d5d785f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510511"
---
# <span data-ttu-id="4e36c-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="4e36c-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="4e36c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e36c-102">SYNOPSIS</span></span>
<span data-ttu-id="4e36c-103">Ottiene tutte le opzioni SSL disponibili per i criteri SSL per il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4e36c-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e36c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e36c-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableSslOptions [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e36c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e36c-105">DESCRIPTION</span></span>
<span data-ttu-id="4e36c-106">Il cmdlet **Get-AzureRmApplicationGatewayAvailableSslOptions** ottiene tutte le opzioni SSL disponibili per i criteri SSL</span><span class="sxs-lookup"><span data-stu-id="4e36c-106">The **Get-AzureRmApplicationGatewayAvailableSslOptions** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="4e36c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e36c-107">EXAMPLES</span></span>

### <span data-ttu-id="4e36c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4e36c-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzureRmApplicationGatewayAvailableSslOptions
```

<span data-ttu-id="4e36c-109">Questi comandi restituiscono tutte le opzioni SSL disponibili per i criteri SSL.</span><span class="sxs-lookup"><span data-stu-id="4e36c-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="4e36c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e36c-110">PARAMETERS</span></span>

### <span data-ttu-id="4e36c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e36c-111">-DefaultProfile</span></span>
<span data-ttu-id="4e36c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e36c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e36c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e36c-113">CommonParameters</span></span>
<span data-ttu-id="4e36c-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e36c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e36c-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e36c-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e36c-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e36c-116">INPUTS</span></span>

### <span data-ttu-id="4e36c-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4e36c-117">None</span></span>

## <span data-ttu-id="4e36c-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e36c-118">OUTPUTS</span></span>

### <span data-ttu-id="4e36c-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="4e36c-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="4e36c-120">Note</span><span class="sxs-lookup"><span data-stu-id="4e36c-120">NOTES</span></span>

## <span data-ttu-id="4e36c-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e36c-121">RELATED LINKS</span></span>


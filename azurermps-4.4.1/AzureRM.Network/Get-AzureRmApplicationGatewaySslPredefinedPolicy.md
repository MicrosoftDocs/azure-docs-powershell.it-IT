---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 03d47278681cbba23895c00b124cc3a2fc2cc6e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688620"
---
# <span data-ttu-id="2b8cb-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="2b8cb-101">Get-AzureRmApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="2b8cb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b8cb-102">SYNOPSIS</span></span>
<span data-ttu-id="2b8cb-103">Ottiene i criteri SSL predefiniti forniti dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2b8cb-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b8cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b8cb-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b8cb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b8cb-105">DESCRIPTION</span></span>
<span data-ttu-id="2b8cb-106">Il cmdlet **Get-AzureRmApplicationGatewaySslPredefinedPolicy** ottiene i criteri SSL predefiniti forniti dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2b8cb-106">The **Get-AzureRmApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="2b8cb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b8cb-107">EXAMPLES</span></span>

### <span data-ttu-id="2b8cb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2b8cb-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzureRmApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="2b8cb-109">Questi comandi restituiscono tutti i criteri SSL predefiniti.</span><span class="sxs-lookup"><span data-stu-id="2b8cb-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="2b8cb-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2b8cb-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzureRmApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="2b8cb-111">Questo comando restituisce un criterio predefinito con il nome AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="2b8cb-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="2b8cb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b8cb-112">PARAMETERS</span></span>

### <span data-ttu-id="2b8cb-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b8cb-113">-Name</span></span>
<span data-ttu-id="2b8cb-114">Nome del criterio predefinito SSL</span><span class="sxs-lookup"><span data-stu-id="2b8cb-114">Name of the ssl predefined policy</span></span>

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

### <span data-ttu-id="2b8cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b8cb-115">-DefaultProfile</span></span>
<span data-ttu-id="2b8cb-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b8cb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b8cb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b8cb-117">CommonParameters</span></span>
<span data-ttu-id="2b8cb-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b8cb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b8cb-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b8cb-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b8cb-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b8cb-120">INPUTS</span></span>

### <span data-ttu-id="2b8cb-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2b8cb-121">None</span></span>

## <span data-ttu-id="2b8cb-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b8cb-122">OUTPUTS</span></span>

### <span data-ttu-id="2b8cb-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="2b8cb-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>
<span data-ttu-id="2b8cb-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy, Microsoft. Azure. Commands. Network, Version = 4.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2b8cb-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2b8cb-125">Note</span><span class="sxs-lookup"><span data-stu-id="2b8cb-125">NOTES</span></span>

## <span data-ttu-id="2b8cb-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b8cb-126">RELATED LINKS</span></span>


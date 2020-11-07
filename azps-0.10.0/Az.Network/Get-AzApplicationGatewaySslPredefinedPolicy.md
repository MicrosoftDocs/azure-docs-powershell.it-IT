---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 2c55da6b7193d02de51e273df4626152d6d088fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860842"
---
# <span data-ttu-id="58544-101">Get-AzApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="58544-101">Get-AzApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="58544-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58544-102">SYNOPSIS</span></span>
<span data-ttu-id="58544-103">Ottiene i criteri SSL predefiniti forniti dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="58544-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="58544-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58544-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58544-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58544-105">DESCRIPTION</span></span>
<span data-ttu-id="58544-106">Il cmdlet **Get-AzApplicationGatewaySslPredefinedPolicy** ottiene i criteri SSL predefiniti forniti dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="58544-106">The **Get-AzApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="58544-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58544-107">EXAMPLES</span></span>

### <span data-ttu-id="58544-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="58544-108">Example 1</span></span>
```
PS C:\>$policies = Get-AzApplicationGatewaySslPredefinedPolicy
```

<span data-ttu-id="58544-109">Questi comandi restituiscono tutti i criteri SSL predefiniti.</span><span class="sxs-lookup"><span data-stu-id="58544-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="58544-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="58544-110">Example 2</span></span>
```
PS C:\>$policy = Get-AzApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

<span data-ttu-id="58544-111">Questo comando restituisce un criterio predefinito con il nome AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="58544-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

## <span data-ttu-id="58544-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58544-112">PARAMETERS</span></span>

### <span data-ttu-id="58544-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58544-113">-DefaultProfile</span></span>
<span data-ttu-id="58544-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58544-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58544-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="58544-115">-Name</span></span>
<span data-ttu-id="58544-116">Nome del criterio predefinito SSL</span><span class="sxs-lookup"><span data-stu-id="58544-116">Name of the ssl predefined policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58544-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58544-117">CommonParameters</span></span>
<span data-ttu-id="58544-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58544-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58544-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58544-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58544-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58544-120">INPUTS</span></span>

### <span data-ttu-id="58544-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="58544-121">None</span></span>

## <span data-ttu-id="58544-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58544-122">OUTPUTS</span></span>

### <span data-ttu-id="58544-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="58544-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>
<span data-ttu-id="58544-124">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy, Microsoft. Azure. Commands. Network, Version = 4.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="58544-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="58544-125">Note</span><span class="sxs-lookup"><span data-stu-id="58544-125">NOTES</span></span>

## <span data-ttu-id="58544-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58544-126">RELATED LINKS</span></span>


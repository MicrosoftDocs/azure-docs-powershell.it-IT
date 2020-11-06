---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfirewallexclusionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallExclusionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFirewallExclusionConfig.md
ms.openlocfilehash: 570e2df066f9e56b7926bf2d0926c484a0654977
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517472"
---
# <span data-ttu-id="0d72b-101">New-AzureRmApplicationGatewayFirewallExclusionConfig</span><span class="sxs-lookup"><span data-stu-id="0d72b-101">New-AzureRmApplicationGatewayFirewallExclusionConfig</span></span>

## <span data-ttu-id="0d72b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d72b-102">SYNOPSIS</span></span>
<span data-ttu-id="0d72b-103">Crea un nuovo elenco di regole di esclusione per Application Gateway WAF</span><span class="sxs-lookup"><span data-stu-id="0d72b-103">Creates a new exclusion rule list for application gateway waf</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d72b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d72b-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFirewallExclusionConfig -Variable <String> -Operator <String> -Selector <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d72b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d72b-105">DESCRIPTION</span></span>
<span data-ttu-id="0d72b-106">Cmdlet **New-AzureRmApplicationGatewayFirewallExclusionConfig** un nuovo elenco di regole di esclusione per il gateway applicazione WAF.</span><span class="sxs-lookup"><span data-stu-id="0d72b-106">The **New-AzureRmApplicationGatewayFirewallExclusionConfig** cmdlet a new exclusion rule list for application gateway waf.</span></span>

## <span data-ttu-id="0d72b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d72b-107">EXAMPLES</span></span>

### <span data-ttu-id="0d72b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0d72b-108">Example 1</span></span>
```powershell
PS C:\> $exclusion1 = New-AzureRmApplicationGatewayFirewallExclusionConfig -Variable "RequestHeaderNames" -Operator "StartsWith" -Selector "xyz"
```

<span data-ttu-id="0d72b-109">Questo comando crea una nuova regola di esclusione elenca la configurazione per la variabile denominata RequestHeaderNames e operator denominata StartsWith e Selector denominata XYZ.</span><span class="sxs-lookup"><span data-stu-id="0d72b-109">This command creates a new exclusion rule lists configuration for the variable named RequestHeaderNames and operator named StartsWith and Selector named xyz.</span></span> <span data-ttu-id="0d72b-110">La configurazione dell'elenco di esclusione viene salvata in $exclusion 1.</span><span class="sxs-lookup"><span data-stu-id="0d72b-110">The exclusion list configuration is saved in $exclusion1.</span></span>

## <span data-ttu-id="0d72b-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d72b-111">PARAMETERS</span></span>

### <span data-ttu-id="0d72b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d72b-112">-DefaultProfile</span></span>
<span data-ttu-id="0d72b-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0d72b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d72b-114">-Operator</span><span class="sxs-lookup"><span data-stu-id="0d72b-114">-Operator</span></span>
<span data-ttu-id="0d72b-115">Quando la variabile è una raccolta, usare il selettore per specificare gli elementi della raccolta a cui si applica questa esclusione.</span><span class="sxs-lookup"><span data-stu-id="0d72b-115">When variable is a collection, operate on the selector to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d72b-116">-Selector</span><span class="sxs-lookup"><span data-stu-id="0d72b-116">-Selector</span></span>
<span data-ttu-id="0d72b-117">Quando la variabile è una raccolta, operator usato per specificare gli elementi della raccolta a cui si applica questa esclusione.</span><span class="sxs-lookup"><span data-stu-id="0d72b-117">When variable is a collection, operator used to specify which elements in the collection this exclusion applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d72b-118">-Variabile</span><span class="sxs-lookup"><span data-stu-id="0d72b-118">-Variable</span></span>
<span data-ttu-id="0d72b-119">Variabile da escludere.</span><span class="sxs-lookup"><span data-stu-id="0d72b-119">The variable to be excluded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d72b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d72b-120">CommonParameters</span></span>
<span data-ttu-id="0d72b-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d72b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d72b-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d72b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d72b-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d72b-123">INPUTS</span></span>

### <span data-ttu-id="0d72b-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0d72b-124">None</span></span>

## <span data-ttu-id="0d72b-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d72b-125">OUTPUTS</span></span>

### <span data-ttu-id="0d72b-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallExclusion</span><span class="sxs-lookup"><span data-stu-id="0d72b-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion</span></span>

## <span data-ttu-id="0d72b-127">Note</span><span class="sxs-lookup"><span data-stu-id="0d72b-127">NOTES</span></span>

## <span data-ttu-id="0d72b-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d72b-128">RELATED LINKS</span></span>

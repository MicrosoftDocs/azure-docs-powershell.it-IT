---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablewafrulesets
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
ms.openlocfilehash: d5e65b90c818102f2cb61997f0e5ff08640d6395
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510903"
---
# <span data-ttu-id="47c7c-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span><span class="sxs-lookup"><span data-stu-id="47c7c-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span></span>

## <span data-ttu-id="47c7c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47c7c-102">SYNOPSIS</span></span>
<span data-ttu-id="47c7c-103">Ottiene tutti i set di regole del firewall delle applicazioni Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="47c7c-103">Gets all available web application firewall rule sets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47c7c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47c7c-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="47c7c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47c7c-105">DESCRIPTION</span></span>
<span data-ttu-id="47c7c-106">Il cmdlet **Get-AzureRmApplicationGatewayAvailableWafRuleSets** ottiene tutti i set di regole del firewall delle applicazioni Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="47c7c-106">The **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="47c7c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47c7c-107">EXAMPLES</span></span>

### <span data-ttu-id="47c7c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="47c7c-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

<span data-ttu-id="47c7c-109">Questi comandi restituiscono tutti i set di regole del firewall delle applicazioni Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="47c7c-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="47c7c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47c7c-110">PARAMETERS</span></span>

### <span data-ttu-id="47c7c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47c7c-111">-DefaultProfile</span></span>
<span data-ttu-id="47c7c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47c7c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47c7c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47c7c-113">CommonParameters</span></span>
<span data-ttu-id="47c7c-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47c7c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47c7c-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47c7c-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47c7c-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47c7c-116">INPUTS</span></span>

### <span data-ttu-id="47c7c-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="47c7c-117">None</span></span>

## <span data-ttu-id="47c7c-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47c7c-118">OUTPUTS</span></span>

### <span data-ttu-id="47c7c-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="47c7c-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="47c7c-120">Note</span><span class="sxs-lookup"><span data-stu-id="47c7c-120">NOTES</span></span>
<span data-ttu-id="47c7c-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** è un alias per il cmdlet **Get-AzureRmApplicationGatewayAvailableWafRuleSets** .</span><span class="sxs-lookup"><span data-stu-id="47c7c-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet.</span></span>

## <span data-ttu-id="47c7c-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47c7c-122">RELATED LINKS</span></span>

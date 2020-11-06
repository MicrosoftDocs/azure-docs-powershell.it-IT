---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
ms.openlocfilehash: 27e5715f32b631fff3f185f0925d0b2a85967ac5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510507"
---
# <span data-ttu-id="34ad4-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span><span class="sxs-lookup"><span data-stu-id="34ad4-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span></span>

## <span data-ttu-id="34ad4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34ad4-102">SYNOPSIS</span></span>
<span data-ttu-id="34ad4-103">Ottiene tutti i set di regole del firewall delle applicazioni Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="34ad4-103">Gets all available web application firewall rule sets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34ad4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34ad4-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34ad4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34ad4-105">DESCRIPTION</span></span>
<span data-ttu-id="34ad4-106">Il cmdlet **Get-AzureRmApplicationGatewayAvailableWafRuleSets** ottiene tutti i set di regole del firewall delle applicazioni Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="34ad4-106">The **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="34ad4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34ad4-107">EXAMPLES</span></span>

### <span data-ttu-id="34ad4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="34ad4-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

<span data-ttu-id="34ad4-109">Questi comandi restituiscono tutti i set di regole del firewall delle applicazioni Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="34ad4-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="34ad4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34ad4-110">PARAMETERS</span></span>

### <span data-ttu-id="34ad4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34ad4-111">-DefaultProfile</span></span>
<span data-ttu-id="34ad4-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="34ad4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34ad4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34ad4-113">CommonParameters</span></span>
<span data-ttu-id="34ad4-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34ad4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34ad4-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34ad4-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34ad4-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34ad4-116">INPUTS</span></span>

### <span data-ttu-id="34ad4-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="34ad4-117">None</span></span>

## <span data-ttu-id="34ad4-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34ad4-118">OUTPUTS</span></span>

### <span data-ttu-id="34ad4-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="34ad4-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="34ad4-120">Note</span><span class="sxs-lookup"><span data-stu-id="34ad4-120">NOTES</span></span>
<span data-ttu-id="34ad4-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** è un alias per il cmdlet **Get-AzureRmApplicationGatewayAvailableWafRuleSets** .</span><span class="sxs-lookup"><span data-stu-id="34ad4-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet.</span></span>

## <span data-ttu-id="34ad4-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34ad4-122">RELATED LINKS</span></span>


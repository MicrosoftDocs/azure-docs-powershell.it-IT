---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablewafrulesets
schema: 2.0.0
ms.openlocfilehash: 83ee8e673271079690c24691f22badfe5193ba50
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866310"
---
# <span data-ttu-id="5ea94-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span><span class="sxs-lookup"><span data-stu-id="5ea94-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span></span>

## <span data-ttu-id="5ea94-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ea94-102">SYNOPSIS</span></span>
<span data-ttu-id="5ea94-103">Ottiene tutti i set di regole del firewall delle applicazioni Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="5ea94-103">Gets all available web application firewall rule sets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ea94-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ea94-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ea94-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ea94-105">DESCRIPTION</span></span>
<span data-ttu-id="5ea94-106">Il cmdlet **Get-AzureRmApplicationGatewayAvailableWafRuleSets** ottiene tutti i set di regole del firewall delle applicazioni Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="5ea94-106">The **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="5ea94-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ea94-107">EXAMPLES</span></span>

### <span data-ttu-id="5ea94-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5ea94-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

<span data-ttu-id="5ea94-109">Questi comandi restituiscono tutti i set di regole del firewall delle applicazioni Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="5ea94-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="5ea94-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ea94-110">PARAMETERS</span></span>

### <span data-ttu-id="5ea94-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ea94-111">-DefaultProfile</span></span>
<span data-ttu-id="5ea94-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ea94-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ea94-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ea94-113">CommonParameters</span></span>
<span data-ttu-id="5ea94-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ea94-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ea94-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ea94-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ea94-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ea94-116">INPUTS</span></span>

### <span data-ttu-id="5ea94-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5ea94-117">None</span></span>

## <span data-ttu-id="5ea94-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ea94-118">OUTPUTS</span></span>

### <span data-ttu-id="5ea94-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="5ea94-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="5ea94-120">Note</span><span class="sxs-lookup"><span data-stu-id="5ea94-120">NOTES</span></span>
<span data-ttu-id="5ea94-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** è un alias per il cmdlet **Get-AzureRmApplicationGatewayAvailableWafRuleSets** .</span><span class="sxs-lookup"><span data-stu-id="5ea94-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet.</span></span>

## <span data-ttu-id="5ea94-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ea94-122">RELATED LINKS</span></span>


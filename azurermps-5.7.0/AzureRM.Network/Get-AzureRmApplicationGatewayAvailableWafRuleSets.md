---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablewafrulesets
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableWafRuleSets.md
ms.openlocfilehash: fb16474d8a23f528aaaeb498ced4fa5a3e952236
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "93522170"
---
# <span data-ttu-id="ea3de-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span><span class="sxs-lookup"><span data-stu-id="ea3de-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span></span>

## <span data-ttu-id="ea3de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ea3de-102">SYNOPSIS</span></span>
<span data-ttu-id="ea3de-103">Ottiene tutti i set di regole del firewall delle applicazioni Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="ea3de-103">Gets all available web application firewall rule sets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea3de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea3de-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea3de-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea3de-105">DESCRIPTION</span></span>
<span data-ttu-id="ea3de-106">Il cmdlet **Get-AzureRmApplicationGatewayAvailableWafRuleSets** ottiene tutti i set di regole del firewall delle applicazioni Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="ea3de-106">The **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="ea3de-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea3de-107">EXAMPLES</span></span>

### <span data-ttu-id="ea3de-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ea3de-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

<span data-ttu-id="ea3de-109">Questi comandi restituiscono tutti i set di regole del firewall delle applicazioni Web disponibili.</span><span class="sxs-lookup"><span data-stu-id="ea3de-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="ea3de-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ea3de-110">PARAMETERS</span></span>

### <span data-ttu-id="ea3de-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea3de-111">-DefaultProfile</span></span>
<span data-ttu-id="ea3de-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea3de-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea3de-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea3de-113">CommonParameters</span></span>
<span data-ttu-id="ea3de-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea3de-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea3de-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea3de-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea3de-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ea3de-116">INPUTS</span></span>

### <span data-ttu-id="ea3de-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ea3de-117">None</span></span>

## <span data-ttu-id="ea3de-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea3de-118">OUTPUTS</span></span>

### <span data-ttu-id="ea3de-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="ea3de-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="ea3de-120">Note</span><span class="sxs-lookup"><span data-stu-id="ea3de-120">NOTES</span></span>
<span data-ttu-id="ea3de-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** è un alias per il cmdlet **Get-AzureRmApplicationGatewayAvailableWafRuleSets** .</span><span class="sxs-lookup"><span data-stu-id="ea3de-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet.</span></span>

## <span data-ttu-id="ea3de-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea3de-122">RELATED LINKS</span></span>


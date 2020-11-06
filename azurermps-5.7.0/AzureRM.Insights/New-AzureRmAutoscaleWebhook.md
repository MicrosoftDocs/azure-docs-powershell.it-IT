---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
ms.openlocfilehash: 8b94ad5728e7852bb3cd834e7479a29cc11c1698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519458"
---
# <span data-ttu-id="7c5b2-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="7c5b2-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="7c5b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c5b2-102">SYNOPSIS</span></span>
<span data-ttu-id="7c5b2-103">Crea un webhook di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="7c5b2-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c5b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c5b2-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c5b2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c5b2-105">DESCRIPTION</span></span>
<span data-ttu-id="7c5b2-106">Il cmdlet **New-AzureRmAutoscaleWebhook** crea un webhook di scala.</span><span class="sxs-lookup"><span data-stu-id="7c5b2-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="7c5b2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c5b2-107">EXAMPLES</span></span>

## <span data-ttu-id="7c5b2-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c5b2-108">PARAMETERS</span></span>

### <span data-ttu-id="7c5b2-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c5b2-109">-DefaultProfile</span></span>
<span data-ttu-id="7c5b2-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7c5b2-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c5b2-111">-Property</span><span class="sxs-lookup"><span data-stu-id="7c5b2-111">-Property</span></span>
<span data-ttu-id="7c5b2-112">Specifica l'elenco di proprietà nel formato @ (Property1 =' value1',....).</span><span class="sxs-lookup"><span data-stu-id="7c5b2-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Properties

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c5b2-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="7c5b2-113">-ServiceUri</span></span>
<span data-ttu-id="7c5b2-114">Specifica l'URI del servizio.</span><span class="sxs-lookup"><span data-stu-id="7c5b2-114">Specifies the service URI.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c5b2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c5b2-115">CommonParameters</span></span>
<span data-ttu-id="7c5b2-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c5b2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c5b2-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c5b2-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c5b2-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c5b2-118">INPUTS</span></span>

### <span data-ttu-id="7c5b2-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7c5b2-119">None</span></span>
<span data-ttu-id="7c5b2-120">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7c5b2-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7c5b2-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c5b2-121">OUTPUTS</span></span>

### <span data-ttu-id="7c5b2-122">Microsoft. Azure. Management. monitor. Management. Models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="7c5b2-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="7c5b2-123">Note</span><span class="sxs-lookup"><span data-stu-id="7c5b2-123">NOTES</span></span>

## <span data-ttu-id="7c5b2-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c5b2-124">RELATED LINKS</span></span>

[<span data-ttu-id="7c5b2-125">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="7c5b2-125">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)



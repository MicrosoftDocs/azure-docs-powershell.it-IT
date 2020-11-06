---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
ms.openlocfilehash: 2fc67e4f50d3c0a045ed6f0e6d82d5bf46d10c25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519584"
---
# <span data-ttu-id="b4a98-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="b4a98-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="b4a98-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b4a98-102">SYNOPSIS</span></span>
<span data-ttu-id="b4a98-103">Crea un webhook di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="b4a98-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4a98-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4a98-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Properties] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4a98-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4a98-105">DESCRIPTION</span></span>
<span data-ttu-id="b4a98-106">Il cmdlet **New-AzureRmAutoscaleWebhook** crea un webhook di scala.</span><span class="sxs-lookup"><span data-stu-id="b4a98-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="b4a98-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4a98-107">EXAMPLES</span></span>

## <span data-ttu-id="b4a98-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b4a98-108">PARAMETERS</span></span>

### <span data-ttu-id="b4a98-109">-Proprietà</span><span class="sxs-lookup"><span data-stu-id="b4a98-109">-Properties</span></span>
<span data-ttu-id="b4a98-110">Specifica l'elenco di proprietà nel formato @ (Property1 =' value1',....).</span><span class="sxs-lookup"><span data-stu-id="b4a98-110">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4a98-111">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="b4a98-111">-ServiceUri</span></span>
<span data-ttu-id="b4a98-112">Specifica l'URI del servizio.</span><span class="sxs-lookup"><span data-stu-id="b4a98-112">Specifies the service URI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4a98-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4a98-113">-DefaultProfile</span></span>
<span data-ttu-id="b4a98-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b4a98-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4a98-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4a98-115">CommonParameters</span></span>
<span data-ttu-id="b4a98-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4a98-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4a98-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4a98-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4a98-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b4a98-118">INPUTS</span></span>

## <span data-ttu-id="b4a98-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4a98-119">OUTPUTS</span></span>

### <span data-ttu-id="b4a98-120">Microsoft. Azure. Management. monitor. Management. Models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="b4a98-120">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="b4a98-121">Note</span><span class="sxs-lookup"><span data-stu-id="b4a98-121">NOTES</span></span>

## <span data-ttu-id="b4a98-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4a98-122">RELATED LINKS</span></span>

[<span data-ttu-id="b4a98-123">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="b4a98-123">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)



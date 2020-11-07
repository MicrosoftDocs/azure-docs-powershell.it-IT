---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalewebhook
schema: 2.0.0
ms.openlocfilehash: fe6170842bcacf4d7fb0c8e442dc988c03c67e35
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866348"
---
# <span data-ttu-id="0e143-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="0e143-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="0e143-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0e143-102">SYNOPSIS</span></span>
<span data-ttu-id="0e143-103">Crea un webhook di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="0e143-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e143-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0e143-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e143-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e143-105">DESCRIPTION</span></span>
<span data-ttu-id="0e143-106">Il cmdlet **New-AzureRmAutoscaleWebhook** crea un webhook di scala.</span><span class="sxs-lookup"><span data-stu-id="0e143-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="0e143-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0e143-107">EXAMPLES</span></span>

## <span data-ttu-id="0e143-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0e143-108">PARAMETERS</span></span>

### <span data-ttu-id="0e143-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e143-109">-DefaultProfile</span></span>
<span data-ttu-id="0e143-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0e143-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e143-111">-Property</span><span class="sxs-lookup"><span data-stu-id="0e143-111">-Property</span></span>
<span data-ttu-id="0e143-112">Specifica l'elenco di proprietà nel formato @ (Property1 =' value1',....).</span><span class="sxs-lookup"><span data-stu-id="0e143-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="0e143-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="0e143-113">-ServiceUri</span></span>
<span data-ttu-id="0e143-114">Specifica l'URI del servizio.</span><span class="sxs-lookup"><span data-stu-id="0e143-114">Specifies the service URI.</span></span>

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

### <span data-ttu-id="0e143-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e143-115">CommonParameters</span></span>
<span data-ttu-id="0e143-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e143-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e143-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e143-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e143-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0e143-118">INPUTS</span></span>

### <span data-ttu-id="0e143-119">System. String</span><span class="sxs-lookup"><span data-stu-id="0e143-119">System.String</span></span>

### <span data-ttu-id="0e143-120">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0e143-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0e143-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0e143-121">OUTPUTS</span></span>

### <span data-ttu-id="0e143-122">Microsoft. Azure. Management. monitor. Management. Models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="0e143-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="0e143-123">Note</span><span class="sxs-lookup"><span data-stu-id="0e143-123">NOTES</span></span>

## <span data-ttu-id="0e143-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0e143-124">RELATED LINKS</span></span>

[<span data-ttu-id="0e143-125">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="0e143-125">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)



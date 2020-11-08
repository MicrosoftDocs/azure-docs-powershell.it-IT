---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
ms.openlocfilehash: f9e9d9bea69944fdd6eae6c81a4472dee1816e4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018779"
---
# <span data-ttu-id="26dfd-101">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="26dfd-101">New-AzAutoscaleWebhook</span></span>

## <span data-ttu-id="26dfd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="26dfd-103">Crea un webhook di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="26dfd-103">Creates an Autoscale webhook.</span></span>

## <span data-ttu-id="26dfd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26dfd-104">SYNTAX</span></span>

```
New-AzAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26dfd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26dfd-105">DESCRIPTION</span></span>
<span data-ttu-id="26dfd-106">Il cmdlet **New-AzAutoscaleWebhook** crea un webhook di scala.</span><span class="sxs-lookup"><span data-stu-id="26dfd-106">The **New-AzAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="26dfd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26dfd-107">EXAMPLES</span></span>

## <span data-ttu-id="26dfd-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26dfd-108">PARAMETERS</span></span>

### <span data-ttu-id="26dfd-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26dfd-109">-DefaultProfile</span></span>
<span data-ttu-id="26dfd-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="26dfd-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26dfd-111">-Property</span><span class="sxs-lookup"><span data-stu-id="26dfd-111">-Property</span></span>
<span data-ttu-id="26dfd-112">Specifica l'elenco di proprietà nel formato @ (Property1 =' value1',....).</span><span class="sxs-lookup"><span data-stu-id="26dfd-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="26dfd-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="26dfd-113">-ServiceUri</span></span>
<span data-ttu-id="26dfd-114">Specifica l'URI del servizio.</span><span class="sxs-lookup"><span data-stu-id="26dfd-114">Specifies the service URI.</span></span>

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

### <span data-ttu-id="26dfd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26dfd-115">CommonParameters</span></span>
<span data-ttu-id="26dfd-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26dfd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26dfd-117">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26dfd-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26dfd-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26dfd-118">INPUTS</span></span>

### <span data-ttu-id="26dfd-119">System. String</span><span class="sxs-lookup"><span data-stu-id="26dfd-119">System.String</span></span>

### <span data-ttu-id="26dfd-120">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="26dfd-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="26dfd-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26dfd-121">OUTPUTS</span></span>

### <span data-ttu-id="26dfd-122">Microsoft. Azure. Management. monitor. Management. Models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="26dfd-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="26dfd-123">Note</span><span class="sxs-lookup"><span data-stu-id="26dfd-123">NOTES</span></span>

## <span data-ttu-id="26dfd-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26dfd-124">RELATED LINKS</span></span>

[<span data-ttu-id="26dfd-125">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="26dfd-125">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)



---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
ms.openlocfilehash: f6791d2cc962f0bb0db038ad8c5391425c09bfbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521239"
---
# <span data-ttu-id="d5aeb-101">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="d5aeb-101">New-AzureRmAutoscaleNotification</span></span>

## <span data-ttu-id="d5aeb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d5aeb-102">SYNOPSIS</span></span>
<span data-ttu-id="d5aeb-103">Crea una notifica tramite posta elettronica di scala.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-103">Creates an Autoscale email notification.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5aeb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5aeb-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleNotification [[-Webhooks] <WebhookNotification[]>] [[-CustomEmails] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5aeb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5aeb-105">DESCRIPTION</span></span>
<span data-ttu-id="d5aeb-106">Il cmdlet **New-AzureRmAutoscaleNotification** crea una notifica tramite posta elettronica per la scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-106">The **New-AzureRmAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="d5aeb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5aeb-107">EXAMPLES</span></span>

### <span data-ttu-id="d5aeb-108">Esempio 1: creare una notifica di posta elettronica in scala ridotta</span><span class="sxs-lookup"><span data-stu-id="d5aeb-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="d5aeb-109">Questo comando crea una notifica di posta elettronica di Autosacale per due indirizzi specificati.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="d5aeb-110">Esempio 2: creare una notifica di posta elettronica di scalabilità per l'amministratore della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="d5aeb-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="d5aeb-111">Questo comando crea una notifica di posta elettronica di Autosacale per l'amministratore della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="d5aeb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d5aeb-112">PARAMETERS</span></span>

### <span data-ttu-id="d5aeb-113">-CustomEmails</span><span class="sxs-lookup"><span data-stu-id="d5aeb-113">-CustomEmails</span></span>
<span data-ttu-id="d5aeb-114">Specifica un elenco delimitato da virgole di indirizzi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-114">Specifies a comma-separated list of email addresses.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5aeb-115">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="d5aeb-115">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="d5aeb-116">Indica che questa operazione invia una notifica tramite posta elettronica all'amministratore della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-116">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5aeb-117">-SendEmailToSubscriptionCoAdministrators</span><span class="sxs-lookup"><span data-stu-id="d5aeb-117">-SendEmailToSubscriptionCoAdministrators</span></span>
<span data-ttu-id="d5aeb-118">Indica che questa operazione invia una notifica tramite posta elettronica ai coordinatori dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-118">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5aeb-119">-Webhook</span><span class="sxs-lookup"><span data-stu-id="d5aeb-119">-Webhooks</span></span>
<span data-ttu-id="d5aeb-120">Specifica un elenco delimitato da virgole di Webhook di scala.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-120">Specifies a comma-separated list of Autoscale webhooks.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5aeb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5aeb-121">-DefaultProfile</span></span>
<span data-ttu-id="d5aeb-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5aeb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5aeb-123">CommonParameters</span></span>
<span data-ttu-id="d5aeb-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5aeb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5aeb-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5aeb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5aeb-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d5aeb-126">INPUTS</span></span>

## <span data-ttu-id="d5aeb-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5aeb-127">OUTPUTS</span></span>

### <span data-ttu-id="d5aeb-128">Microsoft. Azure. Management. monitor. Management. Models. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="d5aeb-128">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="d5aeb-129">Note</span><span class="sxs-lookup"><span data-stu-id="d5aeb-129">NOTES</span></span>

## <span data-ttu-id="d5aeb-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5aeb-130">RELATED LINKS</span></span>

[<span data-ttu-id="d5aeb-131">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="d5aeb-131">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)



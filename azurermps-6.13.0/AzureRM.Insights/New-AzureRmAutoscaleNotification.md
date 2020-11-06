---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
ms.openlocfilehash: e550341d0bd5a5d2f4e26e4ac736fab9831b67c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513811"
---
# <span data-ttu-id="f0e26-101">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="f0e26-101">New-AzureRmAutoscaleNotification</span></span>

## <span data-ttu-id="f0e26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f0e26-102">SYNOPSIS</span></span>
<span data-ttu-id="f0e26-103">Crea una notifica tramite posta elettronica di scala.</span><span class="sxs-lookup"><span data-stu-id="f0e26-103">Creates an Autoscale email notification.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0e26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0e26-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0e26-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0e26-105">DESCRIPTION</span></span>
<span data-ttu-id="f0e26-106">Il cmdlet **New-AzureRmAutoscaleNotification** crea una notifica tramite posta elettronica per la scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="f0e26-106">The **New-AzureRmAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="f0e26-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0e26-107">EXAMPLES</span></span>

### <span data-ttu-id="f0e26-108">Esempio 1: creare una notifica di posta elettronica in scala ridotta</span><span class="sxs-lookup"><span data-stu-id="f0e26-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="f0e26-109">Questo comando crea una notifica di posta elettronica di Autosacale per due indirizzi specificati.</span><span class="sxs-lookup"><span data-stu-id="f0e26-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="f0e26-110">Esempio 2: creare una notifica di posta elettronica di scalabilità per l'amministratore della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="f0e26-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="f0e26-111">Questo comando crea una notifica di posta elettronica di Autosacale per l'amministratore della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="f0e26-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="f0e26-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f0e26-112">PARAMETERS</span></span>

### <span data-ttu-id="f0e26-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="f0e26-113">-CustomEmail</span></span>
<span data-ttu-id="f0e26-114">Specifica un elenco delimitato da virgole di indirizzi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="f0e26-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="f0e26-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0e26-115">-DefaultProfile</span></span>
<span data-ttu-id="f0e26-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f0e26-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0e26-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="f0e26-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="f0e26-118">Indica che questa operazione invia una notifica tramite posta elettronica all'amministratore della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="f0e26-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="f0e26-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="f0e26-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="f0e26-120">Indica che questa operazione invia una notifica tramite posta elettronica ai coordinatori dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f0e26-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="f0e26-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="f0e26-121">-Webhook</span></span>
<span data-ttu-id="f0e26-122">Specifica un elenco delimitato da virgole di Webhook di scala.</span><span class="sxs-lookup"><span data-stu-id="f0e26-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="f0e26-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0e26-123">CommonParameters</span></span>
<span data-ttu-id="f0e26-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0e26-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0e26-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0e26-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0e26-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f0e26-126">INPUTS</span></span>

### <span data-ttu-id="f0e26-127">Microsoft. Azure. Management. monitor. Management. Models. WebhookNotification []</span><span class="sxs-lookup"><span data-stu-id="f0e26-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="f0e26-128">System. String []</span><span class="sxs-lookup"><span data-stu-id="f0e26-128">System.String[]</span></span>

### <span data-ttu-id="f0e26-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f0e26-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f0e26-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0e26-130">OUTPUTS</span></span>

### <span data-ttu-id="f0e26-131">Microsoft. Azure. Management. monitor. Management. Models. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="f0e26-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="f0e26-132">Note</span><span class="sxs-lookup"><span data-stu-id="f0e26-132">NOTES</span></span>

## <span data-ttu-id="f0e26-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0e26-133">RELATED LINKS</span></span>

[<span data-ttu-id="f0e26-134">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="f0e26-134">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)



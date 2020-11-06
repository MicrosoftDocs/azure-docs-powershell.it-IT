---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
ms.openlocfilehash: ee95455b5081105ec4e28a4811e46ca92bfbc240
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515700"
---
# <span data-ttu-id="a340d-101">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="a340d-101">New-AzureRmAutoscaleNotification</span></span>

## <span data-ttu-id="a340d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a340d-102">SYNOPSIS</span></span>
<span data-ttu-id="a340d-103">Crea una notifica tramite posta elettronica di scala.</span><span class="sxs-lookup"><span data-stu-id="a340d-103">Creates an Autoscale email notification.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a340d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a340d-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator] 
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a340d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a340d-105">DESCRIPTION</span></span>
<span data-ttu-id="a340d-106">Il cmdlet **New-AzureRmAutoscaleNotification** crea una notifica tramite posta elettronica per la scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="a340d-106">The **New-AzureRmAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="a340d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a340d-107">EXAMPLES</span></span>

### <span data-ttu-id="a340d-108">Esempio 1: creare una notifica di posta elettronica in scala ridotta</span><span class="sxs-lookup"><span data-stu-id="a340d-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="a340d-109">Questo comando crea una notifica di posta elettronica di Autosacale per due indirizzi specificati.</span><span class="sxs-lookup"><span data-stu-id="a340d-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="a340d-110">Esempio 2: creare una notifica di posta elettronica di scalabilità per l'amministratore della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="a340d-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="a340d-111">Questo comando crea una notifica di posta elettronica di Autosacale per l'amministratore della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a340d-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="a340d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a340d-112">PARAMETERS</span></span>

### <span data-ttu-id="a340d-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="a340d-113">-CustomEmail</span></span>
<span data-ttu-id="a340d-114">Specifica un elenco delimitato da virgole di indirizzi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="a340d-114">Specifies a comma-separated list of email addresses.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: CustomEmails

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a340d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a340d-115">-DefaultProfile</span></span>
<span data-ttu-id="a340d-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a340d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a340d-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="a340d-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="a340d-118">Indica che questa operazione invia una notifica tramite posta elettronica all'amministratore della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a340d-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a340d-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="a340d-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="a340d-120">Indica che questa operazione invia una notifica tramite posta elettronica ai coordinatori dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a340d-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: SendEmailToSubscriptionCoAdministrators

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a340d-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="a340d-121">-Webhook</span></span>
<span data-ttu-id="a340d-122">Specifica un elenco delimitato da virgole di Webhook di scala.</span><span class="sxs-lookup"><span data-stu-id="a340d-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

```yaml
Type: WebhookNotification[]
Parameter Sets: (All)
Aliases: Webhooks

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a340d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a340d-123">CommonParameters</span></span>
<span data-ttu-id="a340d-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a340d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a340d-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a340d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a340d-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a340d-126">INPUTS</span></span>

### <span data-ttu-id="a340d-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a340d-127">None</span></span>
<span data-ttu-id="a340d-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="a340d-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a340d-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a340d-129">OUTPUTS</span></span>

### <span data-ttu-id="a340d-130">Microsoft. Azure. Management. monitor. Management. Models. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="a340d-130">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="a340d-131">Note</span><span class="sxs-lookup"><span data-stu-id="a340d-131">NOTES</span></span>

## <span data-ttu-id="a340d-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a340d-132">RELATED LINKS</span></span>

[<span data-ttu-id="a340d-133">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="a340d-133">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)



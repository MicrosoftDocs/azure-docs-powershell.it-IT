---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: 010698183dec206002c0966fb8f37d629d24794a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296809"
---
# <span data-ttu-id="69c95-101">New-AzAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="69c95-101">New-AzAutoscaleNotification</span></span>

## <span data-ttu-id="69c95-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69c95-102">SYNOPSIS</span></span>
<span data-ttu-id="69c95-103">Crea una notifica tramite posta elettronica di scala.</span><span class="sxs-lookup"><span data-stu-id="69c95-103">Creates an Autoscale email notification.</span></span>

## <span data-ttu-id="69c95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69c95-104">SYNTAX</span></span>

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69c95-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69c95-105">DESCRIPTION</span></span>
<span data-ttu-id="69c95-106">Il cmdlet **New-AzAutoscaleNotification** crea una notifica tramite posta elettronica per la scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="69c95-106">The **New-AzAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="69c95-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69c95-107">EXAMPLES</span></span>

### <span data-ttu-id="69c95-108">Esempio 1: creare una notifica di posta elettronica in scala ridotta</span><span class="sxs-lookup"><span data-stu-id="69c95-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="69c95-109">Questo comando crea una notifica di posta elettronica di Autosacale per due indirizzi specificati.</span><span class="sxs-lookup"><span data-stu-id="69c95-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="69c95-110">Esempio 2: creare una notifica di posta elettronica di scalabilità per l'amministratore della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="69c95-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="69c95-111">Questo comando crea una notifica di posta elettronica di Autosacale per l'amministratore della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="69c95-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="69c95-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69c95-112">PARAMETERS</span></span>

### <span data-ttu-id="69c95-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="69c95-113">-CustomEmail</span></span>
<span data-ttu-id="69c95-114">Specifica un elenco delimitato da virgole di indirizzi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="69c95-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="69c95-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69c95-115">-DefaultProfile</span></span>
<span data-ttu-id="69c95-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="69c95-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69c95-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="69c95-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="69c95-118">Indica che questa operazione invia una notifica tramite posta elettronica all'amministratore della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="69c95-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="69c95-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="69c95-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="69c95-120">Indica che questa operazione invia una notifica tramite posta elettronica ai coordinatori dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="69c95-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="69c95-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="69c95-121">-Webhook</span></span>
<span data-ttu-id="69c95-122">Specifica un elenco delimitato da virgole di Webhook di scala.</span><span class="sxs-lookup"><span data-stu-id="69c95-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="69c95-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c95-123">CommonParameters</span></span>
<span data-ttu-id="69c95-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69c95-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c95-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69c95-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c95-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69c95-126">INPUTS</span></span>

### <span data-ttu-id="69c95-127">Microsoft. Azure. Management. monitor. Management. Models. WebhookNotification []</span><span class="sxs-lookup"><span data-stu-id="69c95-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="69c95-128">System. String []</span><span class="sxs-lookup"><span data-stu-id="69c95-128">System.String[]</span></span>

### <span data-ttu-id="69c95-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="69c95-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="69c95-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69c95-130">OUTPUTS</span></span>

### <span data-ttu-id="69c95-131">Microsoft. Azure. Management. monitor. Management. Models. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="69c95-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="69c95-132">Note</span><span class="sxs-lookup"><span data-stu-id="69c95-132">NOTES</span></span>

## <span data-ttu-id="69c95-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69c95-133">RELATED LINKS</span></span>

[<span data-ttu-id="69c95-134">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="69c95-134">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)



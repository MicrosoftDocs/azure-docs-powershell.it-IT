---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: c537908d2249ca5ec8a33adffa4e655b0a9ec6e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982669"
---
# <span data-ttu-id="3e6ea-101">New-AzAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="3e6ea-101">New-AzAutoscaleNotification</span></span>

## <span data-ttu-id="3e6ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e6ea-102">SYNOPSIS</span></span>
<span data-ttu-id="3e6ea-103">Crea una notifica di posta elettronica con scala automatica.</span><span class="sxs-lookup"><span data-stu-id="3e6ea-103">Creates an Autoscale email notification.</span></span>

## <span data-ttu-id="3e6ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e6ea-104">SYNTAX</span></span>

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e6ea-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3e6ea-105">DESCRIPTION</span></span>
<span data-ttu-id="3e6ea-106">Il cmdlet **New-AzAutoscaleNotification** crea una notifica di posta elettronica per la scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="3e6ea-106">The **New-AzAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="3e6ea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e6ea-107">EXAMPLES</span></span>

### <span data-ttu-id="3e6ea-108">Esempio 1: Creare una notifica di ridimensionamento automatico tramite posta elettronica</span><span class="sxs-lookup"><span data-stu-id="3e6ea-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="3e6ea-109">Questo comando crea una notifica di posta elettronica autosacale per due indirizzi specificati.</span><span class="sxs-lookup"><span data-stu-id="3e6ea-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="3e6ea-110">Esempio 2: Creare una notifica di ridimensionamento automatico tramite posta elettronica per l'amministratore dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="3e6ea-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="3e6ea-111">Questo comando crea una notifica di autosacale tramite posta elettronica per l'amministratore della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="3e6ea-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="3e6ea-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e6ea-112">PARAMETERS</span></span>

### <span data-ttu-id="3e6ea-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="3e6ea-113">-CustomEmail</span></span>
<span data-ttu-id="3e6ea-114">Specifica un elenco di indirizzi di posta elettronica separati da virgola.</span><span class="sxs-lookup"><span data-stu-id="3e6ea-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="3e6ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e6ea-115">-DefaultProfile</span></span>
<span data-ttu-id="3e6ea-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3e6ea-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e6ea-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="3e6ea-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="3e6ea-118">Indica che questa operazione invia una notifica tramite posta elettronica all'amministratore della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="3e6ea-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="3e6ea-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="3e6ea-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="3e6ea-120">Indica che questa operazione invia una notifica tramite posta elettronica ai co-amministratori della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="3e6ea-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="3e6ea-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="3e6ea-121">-Webhook</span></span>
<span data-ttu-id="3e6ea-122">Specifica un elenco di webhook con valori delimitati da virgole.</span><span class="sxs-lookup"><span data-stu-id="3e6ea-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="3e6ea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e6ea-123">CommonParameters</span></span>
<span data-ttu-id="3e6ea-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e6ea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e6ea-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3e6ea-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e6ea-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="3e6ea-126">INPUTS</span></span>

### <span data-ttu-id="3e6ea-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span><span class="sxs-lookup"><span data-stu-id="3e6ea-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="3e6ea-128">System.String[]</span><span class="sxs-lookup"><span data-stu-id="3e6ea-128">System.String[]</span></span>

### <span data-ttu-id="3e6ea-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3e6ea-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3e6ea-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e6ea-130">OUTPUTS</span></span>

### <span data-ttu-id="3e6ea-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="3e6ea-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="3e6ea-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="3e6ea-132">NOTES</span></span>

## <span data-ttu-id="3e6ea-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e6ea-133">RELATED LINKS</span></span>

[<span data-ttu-id="3e6ea-134">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="3e6ea-134">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)



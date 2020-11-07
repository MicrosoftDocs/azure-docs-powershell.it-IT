---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: 35f540d26464b7cdc4b08916f1397b71ee7cca18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835064"
---
# <span data-ttu-id="d2438-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="d2438-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="d2438-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2438-102">SYNOPSIS</span></span>
<span data-ttu-id="d2438-103">Crea un nuovo destinatario del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="d2438-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="d2438-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2438-104">SYNTAX</span></span>

### <span data-ttu-id="d2438-105">NewEmailReceiver (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d2438-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2438-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="d2438-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2438-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="d2438-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2438-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2438-108">DESCRIPTION</span></span>
<span data-ttu-id="d2438-109">Il cmdlet **New-AzActionGroupReceiver** crea il nuovo ricevitore del gruppo di azioni in memoria.</span><span class="sxs-lookup"><span data-stu-id="d2438-109">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="d2438-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2438-110">EXAMPLES</span></span>

### <span data-ttu-id="d2438-111">Esempio 1: creare un nuovo ricevitore di posta elettronica in memoria.</span><span class="sxs-lookup"><span data-stu-id="d2438-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="d2438-112">Questo comando crea un nuovo ricevitore di posta elettronica in memoria.</span><span class="sxs-lookup"><span data-stu-id="d2438-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="d2438-113">Esempio 2: creare un nuovo ricevitore SMS in memoria.</span><span class="sxs-lookup"><span data-stu-id="d2438-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="d2438-114">Questo comando crea un nuovo ricevitore SMS in memoria.</span><span class="sxs-lookup"><span data-stu-id="d2438-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="d2438-115">Esempio 3: creare un nuovo ricevitore webhook in memoria.</span><span class="sxs-lookup"><span data-stu-id="d2438-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="d2438-116">Questo comando crea un nuovo ricevitore webhook in memoria.</span><span class="sxs-lookup"><span data-stu-id="d2438-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="d2438-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2438-117">PARAMETERS</span></span>

### <span data-ttu-id="d2438-118">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="d2438-118">-CountryCode</span></span>
<span data-ttu-id="d2438-119">Specifica il codice paese per il destinatario SMS.</span><span class="sxs-lookup"><span data-stu-id="d2438-119">Specifies the country code for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2438-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2438-120">-DefaultProfile</span></span>
<span data-ttu-id="d2438-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d2438-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2438-122">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="d2438-122">-EmailAddress</span></span>
<span data-ttu-id="d2438-123">Specifica l'indirizzo per il destinatario della posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="d2438-123">Specifies the address for the Email receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewEmailReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2438-124">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="d2438-124">-EmailReceiver</span></span>
<span data-ttu-id="d2438-125">Specifica la creazione di un ricevitore di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="d2438-125">Specifies to create an Email receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewEmailReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2438-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2438-126">-Name</span></span>
<span data-ttu-id="d2438-127">Specifica il nome del destinatario.</span><span class="sxs-lookup"><span data-stu-id="d2438-127">Specifies the name for the receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2438-128">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="d2438-128">-PhoneNumber</span></span>
<span data-ttu-id="d2438-129">Specifica il numero di telefono per il ricevitore SMS.</span><span class="sxs-lookup"><span data-stu-id="d2438-129">Specifies the phone number for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2438-130">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="d2438-130">-ServiceUri</span></span>
<span data-ttu-id="d2438-131">Specifica l'URI per il ricevitore webhook.</span><span class="sxs-lookup"><span data-stu-id="d2438-131">Specifies the URI for the webhook receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2438-132">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="d2438-132">-SmsReceiver</span></span>
<span data-ttu-id="d2438-133">Specifica la creazione di un ricevitore SMS</span><span class="sxs-lookup"><span data-stu-id="d2438-133">Specifies to create a SMS receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2438-134">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="d2438-134">-WebhookReceiver</span></span>
<span data-ttu-id="d2438-135">Specifica la creazione di un ricevitore webhook</span><span class="sxs-lookup"><span data-stu-id="d2438-135">Specifies to create a webhook receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2438-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2438-136">CommonParameters</span></span>
<span data-ttu-id="d2438-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2438-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2438-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2438-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2438-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2438-139">INPUTS</span></span>

### <span data-ttu-id="d2438-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d2438-140">System.String</span></span>

### <span data-ttu-id="d2438-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d2438-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d2438-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2438-142">OUTPUTS</span></span>

### <span data-ttu-id="d2438-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="d2438-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="d2438-144">Note</span><span class="sxs-lookup"><span data-stu-id="d2438-144">NOTES</span></span>

## <span data-ttu-id="d2438-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2438-145">RELATED LINKS</span></span>

<span data-ttu-id="d2438-146">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="d2438-146">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>

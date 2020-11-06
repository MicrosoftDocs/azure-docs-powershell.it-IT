---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroupReceiver.md
ms.openlocfilehash: 82102d8e1c3e726f7932b52fdfcbf2d99084c679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513823"
---
# <span data-ttu-id="9c133-101">New-AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="9c133-101">New-AzureRmActionGroupReceiver</span></span>

## <span data-ttu-id="9c133-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9c133-102">SYNOPSIS</span></span>
<span data-ttu-id="9c133-103">Crea un nuovo destinatario del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="9c133-103">Creates an new action group receiver.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c133-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c133-104">SYNTAX</span></span>

### <span data-ttu-id="9c133-105">NewEmailReceiver (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9c133-105">NewEmailReceiver (Default)</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c133-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="9c133-106">NewSmsReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c133-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="9c133-107">NewWebhookReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c133-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c133-108">DESCRIPTION</span></span>
<span data-ttu-id="9c133-109">Il cmdlet **New-AzureRmActionGroupReceiver** crea il nuovo ricevitore del gruppo di azioni in memoria.</span><span class="sxs-lookup"><span data-stu-id="9c133-109">The **New-AzureRmActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="9c133-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c133-110">EXAMPLES</span></span>

### <span data-ttu-id="9c133-111">Esempio 1: creare un nuovo ricevitore di posta elettronica in memoria.</span><span class="sxs-lookup"><span data-stu-id="9c133-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzureRmActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="9c133-112">Questo comando crea un nuovo ricevitore di posta elettronica in memoria.</span><span class="sxs-lookup"><span data-stu-id="9c133-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="9c133-113">Esempio 2: creare un nuovo ricevitore SMS in memoria.</span><span class="sxs-lookup"><span data-stu-id="9c133-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzureRmActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="9c133-114">Questo comando crea un nuovo ricevitore SMS in memoria.</span><span class="sxs-lookup"><span data-stu-id="9c133-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="9c133-115">Esempio 3: creare un nuovo ricevitore webhook in memoria.</span><span class="sxs-lookup"><span data-stu-id="9c133-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzureRmActionGroupReceiver -Name 'webhookReceiver1' -SMSReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="9c133-116">Questo comando crea un nuovo ricevitore webhook in memoria.</span><span class="sxs-lookup"><span data-stu-id="9c133-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="9c133-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9c133-117">PARAMETERS</span></span>

### <span data-ttu-id="9c133-118">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="9c133-118">-CountryCode</span></span>
<span data-ttu-id="9c133-119">Specifica il codice paese per il destinatario SMS.</span><span class="sxs-lookup"><span data-stu-id="9c133-119">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="9c133-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c133-120">-DefaultProfile</span></span>
<span data-ttu-id="9c133-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9c133-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c133-122">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="9c133-122">-EmailAddress</span></span>
<span data-ttu-id="9c133-123">Specifica l'indirizzo per il destinatario della posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="9c133-123">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="9c133-124">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="9c133-124">-EmailReceiver</span></span>
<span data-ttu-id="9c133-125">Specifica la creazione di un ricevitore di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="9c133-125">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="9c133-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c133-126">-Name</span></span>
<span data-ttu-id="9c133-127">Specifica il nome del destinatario.</span><span class="sxs-lookup"><span data-stu-id="9c133-127">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="9c133-128">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="9c133-128">-PhoneNumber</span></span>
<span data-ttu-id="9c133-129">Specifica il numero di telefono per il ricevitore SMS.</span><span class="sxs-lookup"><span data-stu-id="9c133-129">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="9c133-130">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="9c133-130">-ServiceUri</span></span>
<span data-ttu-id="9c133-131">Specifica l'URI per il ricevitore webhook.</span><span class="sxs-lookup"><span data-stu-id="9c133-131">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="9c133-132">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="9c133-132">-SmsReceiver</span></span>
<span data-ttu-id="9c133-133">Specifica la creazione di un ricevitore SMS</span><span class="sxs-lookup"><span data-stu-id="9c133-133">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="9c133-134">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="9c133-134">-WebhookReceiver</span></span>
<span data-ttu-id="9c133-135">Specifica la creazione di un ricevitore webhook</span><span class="sxs-lookup"><span data-stu-id="9c133-135">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="9c133-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c133-136">CommonParameters</span></span>
<span data-ttu-id="9c133-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c133-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c133-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c133-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c133-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9c133-139">INPUTS</span></span>

### <span data-ttu-id="9c133-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9c133-140">System.String</span></span>

### <span data-ttu-id="9c133-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9c133-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9c133-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c133-142">OUTPUTS</span></span>

### <span data-ttu-id="9c133-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="9c133-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="9c133-144">Note</span><span class="sxs-lookup"><span data-stu-id="9c133-144">NOTES</span></span>

## <span data-ttu-id="9c133-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c133-145">RELATED LINKS</span></span>

<span data-ttu-id="9c133-146">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="9c133-146">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span></span>

---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroupReceiver.md
ms.openlocfilehash: 1c35572191ccf66bd7fd4e88e0996a8efdd1b82b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515715"
---
# <span data-ttu-id="b1a99-101">New-AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="b1a99-101">New-AzureRmActionGroupReceiver</span></span>

## <span data-ttu-id="b1a99-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1a99-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a99-103">Crea un nuovo destinatario del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="b1a99-103">Creates an new action group receiver.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1a99-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1a99-104">SYNTAX</span></span>

### <span data-ttu-id="b1a99-105">NewEmailReceiver (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b1a99-105">NewEmailReceiver (Default)</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1a99-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="b1a99-106">NewSmsReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1a99-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="b1a99-107">NewWebhookReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1a99-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1a99-108">DESCRIPTION</span></span>
<span data-ttu-id="b1a99-109">Il cmdlet **New-AzureRmActionGroupReceiver** crea il nuovo ricevitore del gruppo di azioni in memoria.</span><span class="sxs-lookup"><span data-stu-id="b1a99-109">The **New-AzureRmActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="b1a99-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1a99-110">EXAMPLES</span></span>

### <span data-ttu-id="b1a99-111">Esempio 1: creare un nuovo ricevitore di posta elettronica in memoria.</span><span class="sxs-lookup"><span data-stu-id="b1a99-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzureRmActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="b1a99-112">Questo comando crea un nuovo ricevitore di posta elettronica in memoria.</span><span class="sxs-lookup"><span data-stu-id="b1a99-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="b1a99-113">Esempio 2: creare un nuovo ricevitore SMS in memoria.</span><span class="sxs-lookup"><span data-stu-id="b1a99-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzureRmActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="b1a99-114">Questo comando crea un nuovo ricevitore SMS in memoria.</span><span class="sxs-lookup"><span data-stu-id="b1a99-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="b1a99-115">Esempio 3: creare un nuovo ricevitore webhook in memoria.</span><span class="sxs-lookup"><span data-stu-id="b1a99-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzureRmActionGroupReceiver -Name 'webhookReceiver1' -SMSReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="b1a99-116">Questo comando crea un nuovo ricevitore webhook in memoria.</span><span class="sxs-lookup"><span data-stu-id="b1a99-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="b1a99-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1a99-117">PARAMETERS</span></span>

### <span data-ttu-id="b1a99-118">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="b1a99-118">-CountryCode</span></span>
<span data-ttu-id="b1a99-119">Specifica il codice paese per il destinatario SMS.</span><span class="sxs-lookup"><span data-stu-id="b1a99-119">Specifies the country code for the SMS receiver.</span></span>

```yaml
Type: String
Parameter Sets: NewSmsReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1a99-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1a99-120">-DefaultProfile</span></span>
<span data-ttu-id="b1a99-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b1a99-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1a99-122">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="b1a99-122">-EmailAddress</span></span>
<span data-ttu-id="b1a99-123">Specifica l'indirizzo per il destinatario della posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="b1a99-123">Specifies the address for the Email receiver.</span></span>

```yaml
Type: String
Parameter Sets: NewEmailReceiver
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1a99-124">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="b1a99-124">-EmailReceiver</span></span>
<span data-ttu-id="b1a99-125">Specifica la creazione di un ricevitore di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="b1a99-125">Specifies to create an Email receiver</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NewEmailReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1a99-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1a99-126">-Name</span></span>
<span data-ttu-id="b1a99-127">Specifica il nome del destinatario.</span><span class="sxs-lookup"><span data-stu-id="b1a99-127">Specifies the name for the receiver.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1a99-128">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="b1a99-128">-PhoneNumber</span></span>
<span data-ttu-id="b1a99-129">Specifica il numero di telefono per il ricevitore SMS.</span><span class="sxs-lookup"><span data-stu-id="b1a99-129">Specifies the phone number for the SMS receiver.</span></span>

```yaml
Type: String
Parameter Sets: NewSmsReceiver
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1a99-130">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="b1a99-130">-ServiceUri</span></span>
<span data-ttu-id="b1a99-131">Specifica l'URI per il ricevitore webhook.</span><span class="sxs-lookup"><span data-stu-id="b1a99-131">Specifies the URI for the webhook receiver.</span></span>

```yaml
Type: String
Parameter Sets: NewWebhookReceiver
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1a99-132">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="b1a99-132">-SmsReceiver</span></span>
<span data-ttu-id="b1a99-133">Specifica la creazione di un ricevitore SMS</span><span class="sxs-lookup"><span data-stu-id="b1a99-133">Specifies to create a SMS receiver</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NewSmsReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1a99-134">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="b1a99-134">-WebhookReceiver</span></span>
<span data-ttu-id="b1a99-135">Specifica la creazione di un ricevitore webhook</span><span class="sxs-lookup"><span data-stu-id="b1a99-135">Specifies to create a webhook receiver</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1a99-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a99-136">CommonParameters</span></span>
<span data-ttu-id="b1a99-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1a99-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a99-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1a99-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a99-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1a99-139">INPUTS</span></span>

### <span data-ttu-id="b1a99-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b1a99-140">None</span></span>
<span data-ttu-id="b1a99-141">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b1a99-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b1a99-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1a99-142">OUTPUTS</span></span>

### <span data-ttu-id="b1a99-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="b1a99-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="b1a99-144">Note</span><span class="sxs-lookup"><span data-stu-id="b1a99-144">NOTES</span></span>

## <span data-ttu-id="b1a99-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1a99-145">RELATED LINKS</span></span>

<span data-ttu-id="b1a99-146">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="b1a99-146">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span></span>

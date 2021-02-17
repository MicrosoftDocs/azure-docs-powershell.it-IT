---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: f2862c08212f5e41de10cb600edb22c38eac68d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192207"
---
# <span data-ttu-id="663f6-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="663f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="663f6-102">SYNOPSIS</span></span>
<span data-ttu-id="663f6-103">Crea un nuovo ricevitore di gruppi di azioni.</span><span class="sxs-lookup"><span data-stu-id="663f6-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="663f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="663f6-104">SYNTAX</span></span>

### <span data-ttu-id="663f6-105">NewEmailReceiver (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="663f6-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="663f6-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="663f6-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="663f6-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="663f6-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="663f6-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="663f6-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="663f6-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="663f6-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="663f6-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="663f6-115">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="663f6-115">DESCRIPTION</span></span>
<span data-ttu-id="663f6-116">Il cmdlet **New-AzActionGroupReceiver** crea un nuovo ricevitore di gruppi di azioni in memoria.</span><span class="sxs-lookup"><span data-stu-id="663f6-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="663f6-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="663f6-117">EXAMPLES</span></span>

### <span data-ttu-id="663f6-118">Esempio 1: Creare un nuovo ricevitore di posta elettronica in memoria.</span><span class="sxs-lookup"><span data-stu-id="663f6-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="663f6-119">Questo comando crea un nuovo destinatario di posta elettronica in memoria.</span><span class="sxs-lookup"><span data-stu-id="663f6-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="663f6-120">Esempio 2: Creare un nuovo ricevitore SMS in memoria.</span><span class="sxs-lookup"><span data-stu-id="663f6-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="663f6-121">Questo comando crea un nuovo ricevitore SMS in memoria.</span><span class="sxs-lookup"><span data-stu-id="663f6-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="663f6-122">Esempio 3: Creare un nuovo ricevitore Webhook in memoria.</span><span class="sxs-lookup"><span data-stu-id="663f6-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="663f6-123">Questo comando crea un nuovo ricevitore Webhook in memoria.</span><span class="sxs-lookup"><span data-stu-id="663f6-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="663f6-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="663f6-124">PARAMETERS</span></span>

### <span data-ttu-id="663f6-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="663f6-126">Creare un armRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-126">Create a ArmRoleReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewArmRoleReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="663f6-127">-AutomationAccountId</span></span>
<span data-ttu-id="663f6-128">AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="663f6-128">the AutomationAccountId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="663f6-130">Creare un automationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-130">Create a AutomationRunbookReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="663f6-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="663f6-132">l'URI in cui devono essere inviati gli webhook</span><span class="sxs-lookup"><span data-stu-id="663f6-132">the URI where webhooks should be sent</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="663f6-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="663f6-134">AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="663f6-134">the AzureAppPushEmailAddress</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureAppPushReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="663f6-136">Creare un azureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-136">Create a AzureAppPushReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAzureAppPushReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="663f6-138">Creare un armRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-138">Create a ArmRoleReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-139">-Tutto Url</span><span class="sxs-lookup"><span data-stu-id="663f6-139">-CallbackUrl</span></span>
<span data-ttu-id="663f6-140">UrlUrl</span><span class="sxs-lookup"><span data-stu-id="663f6-140">the CallbackUrl</span></span>

```yaml
Type: System.String
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="663f6-141">-ConnectionId</span></span>
<span data-ttu-id="663f6-142">l'ID di connessione itsm di questo ricevitore</span><span class="sxs-lookup"><span data-stu-id="663f6-142">the itsm connection id of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="663f6-143">-CountryCode</span></span>
<span data-ttu-id="663f6-144">Specifica il codice paese per il ricevente SMS.</span><span class="sxs-lookup"><span data-stu-id="663f6-144">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="663f6-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="663f6-145">-DefaultProfile</span></span>
<span data-ttu-id="663f6-146">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="663f6-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="663f6-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="663f6-147">-EmailAddress</span></span>
<span data-ttu-id="663f6-148">Specifica l'indirizzo del destinatario della posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="663f6-148">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="663f6-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-149">-EmailReceiver</span></span>
<span data-ttu-id="663f6-150">Specifica di creare un destinatario di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="663f6-150">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="663f6-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="663f6-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="663f6-152">ResourceId dell'app per le funzioni</span><span class="sxs-lookup"><span data-stu-id="663f6-152">the function app resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-153">-FunctionName</span><span class="sxs-lookup"><span data-stu-id="663f6-153">-FunctionName</span></span>
<span data-ttu-id="663f6-154">nome functionName</span><span class="sxs-lookup"><span data-stu-id="663f6-154">the functionName</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="663f6-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="663f6-156">httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="663f6-156">the httpTriggerUrl</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="663f6-157">-IdentifierUri</span></span>
<span data-ttu-id="663f6-158">URI identificatore per l'autenticazione aad</span><span class="sxs-lookup"><span data-stu-id="663f6-158">the Identifier uri for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-159">-IsGlobalRunbook</span><span class="sxs-lookup"><span data-stu-id="663f6-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="663f6-160">che indica se questa istanza è un runbook globale</span><span class="sxs-lookup"><span data-stu-id="663f6-160">indicating whether this instance is global runbook</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-161">-ItsmReceiver</span></span>
<span data-ttu-id="663f6-162">Creare un itsmReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-162">Create a ItsmReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewItsmReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-163">-LogicAppReceiver</span></span>
<span data-ttu-id="663f6-164">Creare un logicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-164">Create a LogicAppReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-165">-Name</span><span class="sxs-lookup"><span data-stu-id="663f6-165">-Name</span></span>
<span data-ttu-id="663f6-166">Specifica il nome del destinatario.</span><span class="sxs-lookup"><span data-stu-id="663f6-166">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="663f6-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="663f6-167">-ObjectId</span></span>
<span data-ttu-id="663f6-168">ID oggetto app webhook per l'autenticazione aad</span><span class="sxs-lookup"><span data-stu-id="663f6-168">the webhook app object Id for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-169">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="663f6-169">-PhoneNumber</span></span>
<span data-ttu-id="663f6-170">Specifica il numero di telefono per il ricevitore SMS.</span><span class="sxs-lookup"><span data-stu-id="663f6-170">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="663f6-171">-Area geografica</span><span class="sxs-lookup"><span data-stu-id="663f6-171">-Region</span></span>
<span data-ttu-id="663f6-172">l'area geografica di questo ricevitore</span><span class="sxs-lookup"><span data-stu-id="663f6-172">the itsm Region of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="663f6-173">-ResourceId</span></span>
<span data-ttu-id="663f6-174">Il valore di ResourceId</span><span class="sxs-lookup"><span data-stu-id="663f6-174">the ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="663f6-175">-RoleId</span></span>
<span data-ttu-id="663f6-176">ID ruolo arm del ricevitore</span><span class="sxs-lookup"><span data-stu-id="663f6-176">The arm role id of the receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewArmRoleReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="663f6-177">-RunbookName</span></span>
<span data-ttu-id="663f6-178">Nome Runbook</span><span class="sxs-lookup"><span data-stu-id="663f6-178">the RunbookName</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="663f6-179">-ServiceUri</span></span>
<span data-ttu-id="663f6-180">Specifica l'URI per il ricevitore Webhook.</span><span class="sxs-lookup"><span data-stu-id="663f6-180">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="663f6-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-181">-SmsReceiver</span></span>
<span data-ttu-id="663f6-182">Specifica di creare un ricevitore SMS</span><span class="sxs-lookup"><span data-stu-id="663f6-182">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="663f6-183">-TenantId</span><span class="sxs-lookup"><span data-stu-id="663f6-183">-TenantId</span></span>
<span data-ttu-id="663f6-184">l'ID tenant per l'autenticazione aad</span><span class="sxs-lookup"><span data-stu-id="663f6-184">the tenant id for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="663f6-185">-TicketConfiguration</span></span>
<span data-ttu-id="663f6-186">itsm TicketConfiguration di questo ricevitore</span><span class="sxs-lookup"><span data-stu-id="663f6-186">the itsm TicketConfiguration of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="663f6-187">-UseAadAuth</span></span>
<span data-ttu-id="663f6-188">il contrassegno da usare per aggiungere l'autenticazione</span><span class="sxs-lookup"><span data-stu-id="663f6-188">the flag to use add auth</span></span>

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

### <span data-ttu-id="663f6-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="663f6-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="663f6-190">Il contrassegno indica se usare lo schema di avviso comune.</span><span class="sxs-lookup"><span data-stu-id="663f6-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="663f6-191">Questo valore sarà trascurato per i recimi SMS, Azure App push, ITSM e Voice.</span><span class="sxs-lookup"><span data-stu-id="663f6-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

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

### <span data-ttu-id="663f6-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="663f6-192">-VoiceCountryCode</span></span>
<span data-ttu-id="663f6-193">Il codice paese del ricevitore vocale</span><span class="sxs-lookup"><span data-stu-id="663f6-193">The country code of the voice receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewVoiceReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="663f6-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="663f6-195">Il numero di telefono del ricevitore vocale</span><span class="sxs-lookup"><span data-stu-id="663f6-195">The phone number of the voice receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewVoiceReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-196">-VoiceReceiver</span></span>
<span data-ttu-id="663f6-197">Creare un ricevitore vocale</span><span class="sxs-lookup"><span data-stu-id="663f6-197">Create a voice receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewVoiceReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="663f6-198">-WebhookReceiver</span></span>
<span data-ttu-id="663f6-199">Specifica di creare un ricevitore webhook</span><span class="sxs-lookup"><span data-stu-id="663f6-199">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="663f6-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="663f6-200">-WebhookResourceId</span></span>
<span data-ttu-id="663f6-201">the WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="663f6-201">the WebhookResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="663f6-202">-WorkspaceId</span></span>
<span data-ttu-id="663f6-203">ID area di lavoro itsm di questo ricevitore</span><span class="sxs-lookup"><span data-stu-id="663f6-203">the itsm workspace id of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663f6-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="663f6-204">CommonParameters</span></span>
<span data-ttu-id="663f6-205">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="663f6-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="663f6-206">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="663f6-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="663f6-207">INPUT</span><span class="sxs-lookup"><span data-stu-id="663f6-207">INPUTS</span></span>

### <span data-ttu-id="663f6-208">System.String</span><span class="sxs-lookup"><span data-stu-id="663f6-208">System.String</span></span>

### <span data-ttu-id="663f6-209">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="663f6-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="663f6-210">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="663f6-210">OUTPUTS</span></span>

### <span data-ttu-id="663f6-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="663f6-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="663f6-212">NOTE</span><span class="sxs-lookup"><span data-stu-id="663f6-212">NOTES</span></span>

## <span data-ttu-id="663f6-213">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="663f6-213">RELATED LINKS</span></span>

<span data-ttu-id="663f6-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="663f6-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>

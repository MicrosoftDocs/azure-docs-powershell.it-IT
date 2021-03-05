---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: 917f6287c40d4c26123217cccbf1dfc11866a488
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979902"
---
# <span data-ttu-id="770db-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="770db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="770db-102">SYNOPSIS</span></span>
<span data-ttu-id="770db-103">Crea un nuovo ricevitore di gruppi di azioni.</span><span class="sxs-lookup"><span data-stu-id="770db-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="770db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="770db-104">SYNTAX</span></span>

### <span data-ttu-id="770db-105">NewEmailReceiver (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="770db-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="770db-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="770db-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="770db-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="770db-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="770db-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="770db-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="770db-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="770db-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="770db-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="770db-115">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="770db-115">DESCRIPTION</span></span>
<span data-ttu-id="770db-116">Il cmdlet **New-AzActionGroupReceiver** crea un nuovo ricevitore di gruppi di azioni in memoria.</span><span class="sxs-lookup"><span data-stu-id="770db-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="770db-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="770db-117">EXAMPLES</span></span>

### <span data-ttu-id="770db-118">Esempio 1: Creare un nuovo ricevitore di posta elettronica in memoria.</span><span class="sxs-lookup"><span data-stu-id="770db-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="770db-119">Questo comando crea un nuovo destinatario di posta elettronica in memoria.</span><span class="sxs-lookup"><span data-stu-id="770db-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="770db-120">Esempio 2: Creare un nuovo ricevitore SMS in memoria.</span><span class="sxs-lookup"><span data-stu-id="770db-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="770db-121">Questo comando crea un nuovo ricevitore SMS in memoria.</span><span class="sxs-lookup"><span data-stu-id="770db-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="770db-122">Esempio 3: Creare un nuovo ricevitore Webhook in memoria.</span><span class="sxs-lookup"><span data-stu-id="770db-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="770db-123">Questo comando crea un nuovo ricevitore Webhook in memoria.</span><span class="sxs-lookup"><span data-stu-id="770db-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="770db-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="770db-124">PARAMETERS</span></span>

### <span data-ttu-id="770db-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="770db-126">Creare un armRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-126">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="770db-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="770db-127">-AutomationAccountId</span></span>
<span data-ttu-id="770db-128">AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="770db-128">the AutomationAccountId</span></span>

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

### <span data-ttu-id="770db-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="770db-130">Creare un automationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-130">Create a AutomationRunbookReceiver</span></span>

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

### <span data-ttu-id="770db-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="770db-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="770db-132">l'URI in cui devono essere inviati gli webhook</span><span class="sxs-lookup"><span data-stu-id="770db-132">the URI where webhooks should be sent</span></span>

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

### <span data-ttu-id="770db-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="770db-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="770db-134">AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="770db-134">the AzureAppPushEmailAddress</span></span>

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

### <span data-ttu-id="770db-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="770db-136">Creare un azureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-136">Create a AzureAppPushReceiver</span></span>

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

### <span data-ttu-id="770db-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="770db-138">Creare un armRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-138">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="770db-139">-Tutto Url</span><span class="sxs-lookup"><span data-stu-id="770db-139">-CallbackUrl</span></span>
<span data-ttu-id="770db-140">UrlUrl</span><span class="sxs-lookup"><span data-stu-id="770db-140">the CallbackUrl</span></span>

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

### <span data-ttu-id="770db-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="770db-141">-ConnectionId</span></span>
<span data-ttu-id="770db-142">l'ID di connessione itsm di questo ricevitore</span><span class="sxs-lookup"><span data-stu-id="770db-142">the itsm connection id of this receiver</span></span>

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

### <span data-ttu-id="770db-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="770db-143">-CountryCode</span></span>
<span data-ttu-id="770db-144">Specifica il codice paese per il ricevente SMS.</span><span class="sxs-lookup"><span data-stu-id="770db-144">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="770db-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770db-145">-DefaultProfile</span></span>
<span data-ttu-id="770db-146">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="770db-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="770db-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="770db-147">-EmailAddress</span></span>
<span data-ttu-id="770db-148">Specifica l'indirizzo del destinatario della posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="770db-148">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="770db-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-149">-EmailReceiver</span></span>
<span data-ttu-id="770db-150">Specifica di creare un destinatario di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="770db-150">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="770db-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="770db-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="770db-152">the function app resourceId</span><span class="sxs-lookup"><span data-stu-id="770db-152">the function app resourceId</span></span>

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

### <span data-ttu-id="770db-153">-FunctionName</span><span class="sxs-lookup"><span data-stu-id="770db-153">-FunctionName</span></span>
<span data-ttu-id="770db-154">nome functionName</span><span class="sxs-lookup"><span data-stu-id="770db-154">the functionName</span></span>

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

### <span data-ttu-id="770db-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="770db-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="770db-156">httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="770db-156">the httpTriggerUrl</span></span>

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

### <span data-ttu-id="770db-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="770db-157">-IdentifierUri</span></span>
<span data-ttu-id="770db-158">URI identificatore per l'autenticazione aad</span><span class="sxs-lookup"><span data-stu-id="770db-158">the Identifier uri for aad auth</span></span>

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

### <span data-ttu-id="770db-159">-IsGlobalRunbook</span><span class="sxs-lookup"><span data-stu-id="770db-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="770db-160">che indica se questa istanza è un runbook globale</span><span class="sxs-lookup"><span data-stu-id="770db-160">indicating whether this instance is global runbook</span></span>

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

### <span data-ttu-id="770db-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-161">-ItsmReceiver</span></span>
<span data-ttu-id="770db-162">Creare un itsmReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-162">Create a ItsmReceiver</span></span>

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

### <span data-ttu-id="770db-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-163">-LogicAppReceiver</span></span>
<span data-ttu-id="770db-164">Creare un logicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-164">Create a LogicAppReceiver</span></span>

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

### <span data-ttu-id="770db-165">-Name</span><span class="sxs-lookup"><span data-stu-id="770db-165">-Name</span></span>
<span data-ttu-id="770db-166">Specifica il nome del destinatario.</span><span class="sxs-lookup"><span data-stu-id="770db-166">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="770db-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="770db-167">-ObjectId</span></span>
<span data-ttu-id="770db-168">ID oggetto app webhook per l'autenticazione aad</span><span class="sxs-lookup"><span data-stu-id="770db-168">the webhook app object Id for aad auth</span></span>

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

### <span data-ttu-id="770db-169">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="770db-169">-PhoneNumber</span></span>
<span data-ttu-id="770db-170">Specifica il numero di telefono per il ricevitore SMS.</span><span class="sxs-lookup"><span data-stu-id="770db-170">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="770db-171">-Region</span><span class="sxs-lookup"><span data-stu-id="770db-171">-Region</span></span>
<span data-ttu-id="770db-172">l'area geografica di questo ricevitore</span><span class="sxs-lookup"><span data-stu-id="770db-172">the itsm Region of this receiver</span></span>

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

### <span data-ttu-id="770db-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="770db-173">-ResourceId</span></span>
<span data-ttu-id="770db-174">Il valore di ResourceId</span><span class="sxs-lookup"><span data-stu-id="770db-174">the ResourceId</span></span>

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

### <span data-ttu-id="770db-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="770db-175">-RoleId</span></span>
<span data-ttu-id="770db-176">ID ruolo arm del ricevitore</span><span class="sxs-lookup"><span data-stu-id="770db-176">The arm role id of the receiver</span></span>

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

### <span data-ttu-id="770db-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="770db-177">-RunbookName</span></span>
<span data-ttu-id="770db-178">Nome Runbook</span><span class="sxs-lookup"><span data-stu-id="770db-178">the RunbookName</span></span>

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

### <span data-ttu-id="770db-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="770db-179">-ServiceUri</span></span>
<span data-ttu-id="770db-180">Specifica l'URI per il ricevitore Webhook.</span><span class="sxs-lookup"><span data-stu-id="770db-180">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="770db-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-181">-SmsReceiver</span></span>
<span data-ttu-id="770db-182">Specifica di creare un ricevitore SMS</span><span class="sxs-lookup"><span data-stu-id="770db-182">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="770db-183">-TenantId</span><span class="sxs-lookup"><span data-stu-id="770db-183">-TenantId</span></span>
<span data-ttu-id="770db-184">l'ID tenant per l'autenticazione aad</span><span class="sxs-lookup"><span data-stu-id="770db-184">the tenant id for aad auth</span></span>

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

### <span data-ttu-id="770db-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="770db-185">-TicketConfiguration</span></span>
<span data-ttu-id="770db-186">itsm TicketConfiguration di questo ricevitore</span><span class="sxs-lookup"><span data-stu-id="770db-186">the itsm TicketConfiguration of this receiver</span></span>

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

### <span data-ttu-id="770db-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="770db-187">-UseAadAuth</span></span>
<span data-ttu-id="770db-188">il contrassegno da usare per aggiungere l'autenticazione</span><span class="sxs-lookup"><span data-stu-id="770db-188">the flag to use add auth</span></span>

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

### <span data-ttu-id="770db-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="770db-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="770db-190">Il contrassegno indica se usare lo schema di avviso comune.</span><span class="sxs-lookup"><span data-stu-id="770db-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="770db-191">Questo valore sarà trascurato per i recimi SMS, Azure App push, ITSM e Voice.</span><span class="sxs-lookup"><span data-stu-id="770db-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

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

### <span data-ttu-id="770db-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="770db-192">-VoiceCountryCode</span></span>
<span data-ttu-id="770db-193">Il codice paese del ricevitore vocale</span><span class="sxs-lookup"><span data-stu-id="770db-193">The country code of the voice receiver</span></span>

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

### <span data-ttu-id="770db-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="770db-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="770db-195">Il numero di telefono del ricevitore vocale</span><span class="sxs-lookup"><span data-stu-id="770db-195">The phone number of the voice receiver</span></span>

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

### <span data-ttu-id="770db-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-196">-VoiceReceiver</span></span>
<span data-ttu-id="770db-197">Creare un ricevitore vocale</span><span class="sxs-lookup"><span data-stu-id="770db-197">Create a voice receiver</span></span>

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

### <span data-ttu-id="770db-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="770db-198">-WebhookReceiver</span></span>
<span data-ttu-id="770db-199">Specifica di creare un ricevitore webhook</span><span class="sxs-lookup"><span data-stu-id="770db-199">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="770db-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="770db-200">-WebhookResourceId</span></span>
<span data-ttu-id="770db-201">the WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="770db-201">the WebhookResourceId</span></span>

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

### <span data-ttu-id="770db-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="770db-202">-WorkspaceId</span></span>
<span data-ttu-id="770db-203">ID area di lavoro itsm di questo ricevitore</span><span class="sxs-lookup"><span data-stu-id="770db-203">the itsm workspace id of this receiver</span></span>

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

### <span data-ttu-id="770db-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770db-204">CommonParameters</span></span>
<span data-ttu-id="770db-205">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="770db-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770db-206">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="770db-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770db-207">INPUT</span><span class="sxs-lookup"><span data-stu-id="770db-207">INPUTS</span></span>

### <span data-ttu-id="770db-208">System.String</span><span class="sxs-lookup"><span data-stu-id="770db-208">System.String</span></span>

### <span data-ttu-id="770db-209">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="770db-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="770db-210">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="770db-210">OUTPUTS</span></span>

### <span data-ttu-id="770db-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="770db-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="770db-212">NOTE</span><span class="sxs-lookup"><span data-stu-id="770db-212">NOTES</span></span>

## <span data-ttu-id="770db-213">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="770db-213">RELATED LINKS</span></span>

<span data-ttu-id="770db-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="770db-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>

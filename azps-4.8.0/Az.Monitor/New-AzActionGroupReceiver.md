---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: f2862c08212f5e41de10cb600edb22c38eac68d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189768"
---
# <span data-ttu-id="68352-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="68352-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68352-102">SYNOPSIS</span></span>
<span data-ttu-id="68352-103">Crea un nuovo destinatario del gruppo di azioni.</span><span class="sxs-lookup"><span data-stu-id="68352-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="68352-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68352-104">SYNTAX</span></span>

### <span data-ttu-id="68352-105">NewEmailReceiver (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="68352-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68352-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68352-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68352-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68352-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68352-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68352-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68352-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68352-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68352-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68352-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68352-115">DESCRIPTION</span></span>
<span data-ttu-id="68352-116">Il cmdlet **New-AzActionGroupReceiver** crea il nuovo ricevitore del gruppo di azioni in memoria.</span><span class="sxs-lookup"><span data-stu-id="68352-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="68352-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68352-117">EXAMPLES</span></span>

### <span data-ttu-id="68352-118">Esempio 1: creare un nuovo ricevitore di posta elettronica in memoria.</span><span class="sxs-lookup"><span data-stu-id="68352-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="68352-119">Questo comando crea un nuovo ricevitore di posta elettronica in memoria.</span><span class="sxs-lookup"><span data-stu-id="68352-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="68352-120">Esempio 2: creare un nuovo ricevitore SMS in memoria.</span><span class="sxs-lookup"><span data-stu-id="68352-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="68352-121">Questo comando crea un nuovo ricevitore SMS in memoria.</span><span class="sxs-lookup"><span data-stu-id="68352-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="68352-122">Esempio 3: creare un nuovo ricevitore webhook in memoria.</span><span class="sxs-lookup"><span data-stu-id="68352-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="68352-123">Questo comando crea un nuovo ricevitore webhook in memoria.</span><span class="sxs-lookup"><span data-stu-id="68352-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="68352-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68352-124">PARAMETERS</span></span>

### <span data-ttu-id="68352-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="68352-126">Creare un ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-126">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="68352-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="68352-127">-AutomationAccountId</span></span>
<span data-ttu-id="68352-128">AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="68352-128">the AutomationAccountId</span></span>

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

### <span data-ttu-id="68352-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="68352-130">Creare un AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-130">Create a AutomationRunbookReceiver</span></span>

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

### <span data-ttu-id="68352-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="68352-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="68352-132">URI in cui devono essere inviati i webhook</span><span class="sxs-lookup"><span data-stu-id="68352-132">the URI where webhooks should be sent</span></span>

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

### <span data-ttu-id="68352-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="68352-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="68352-134">AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="68352-134">the AzureAppPushEmailAddress</span></span>

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

### <span data-ttu-id="68352-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="68352-136">Creare un AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-136">Create a AzureAppPushReceiver</span></span>

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

### <span data-ttu-id="68352-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="68352-138">Creare un ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-138">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="68352-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="68352-139">-CallbackUrl</span></span>
<span data-ttu-id="68352-140">CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="68352-140">the CallbackUrl</span></span>

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

### <span data-ttu-id="68352-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="68352-141">-ConnectionId</span></span>
<span data-ttu-id="68352-142">ID connessione ITSM di questo ricevitore</span><span class="sxs-lookup"><span data-stu-id="68352-142">the itsm connection id of this receiver</span></span>

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

### <span data-ttu-id="68352-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="68352-143">-CountryCode</span></span>
<span data-ttu-id="68352-144">Specifica il codice paese per il destinatario SMS.</span><span class="sxs-lookup"><span data-stu-id="68352-144">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="68352-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68352-145">-DefaultProfile</span></span>
<span data-ttu-id="68352-146">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="68352-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68352-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="68352-147">-EmailAddress</span></span>
<span data-ttu-id="68352-148">Specifica l'indirizzo per il destinatario della posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="68352-148">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="68352-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-149">-EmailReceiver</span></span>
<span data-ttu-id="68352-150">Specifica la creazione di un ricevitore di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="68352-150">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="68352-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="68352-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="68352-152">la funzione app resourceId</span><span class="sxs-lookup"><span data-stu-id="68352-152">the function app resourceId</span></span>

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

### <span data-ttu-id="68352-153">-Funzionename</span><span class="sxs-lookup"><span data-stu-id="68352-153">-FunctionName</span></span>
<span data-ttu-id="68352-154">funzionename</span><span class="sxs-lookup"><span data-stu-id="68352-154">the functionName</span></span>

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

### <span data-ttu-id="68352-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="68352-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="68352-156">httpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="68352-156">the httpTriggerUrl</span></span>

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

### <span data-ttu-id="68352-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="68352-157">-IdentifierUri</span></span>
<span data-ttu-id="68352-158">URI identificatore per AAD auth</span><span class="sxs-lookup"><span data-stu-id="68352-158">the Identifier uri for aad auth</span></span>

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

### <span data-ttu-id="68352-159">-IsGlobalRunbook</span><span class="sxs-lookup"><span data-stu-id="68352-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="68352-160">che indica se l'istanza è globale Runbook</span><span class="sxs-lookup"><span data-stu-id="68352-160">indicating whether this instance is global runbook</span></span>

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

### <span data-ttu-id="68352-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-161">-ItsmReceiver</span></span>
<span data-ttu-id="68352-162">Creare un ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-162">Create a ItsmReceiver</span></span>

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

### <span data-ttu-id="68352-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-163">-LogicAppReceiver</span></span>
<span data-ttu-id="68352-164">Creare un LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-164">Create a LogicAppReceiver</span></span>

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

### <span data-ttu-id="68352-165">-Nome</span><span class="sxs-lookup"><span data-stu-id="68352-165">-Name</span></span>
<span data-ttu-id="68352-166">Specifica il nome del destinatario.</span><span class="sxs-lookup"><span data-stu-id="68352-166">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="68352-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="68352-167">-ObjectId</span></span>
<span data-ttu-id="68352-168">ID oggetto app webhook per AAD auth</span><span class="sxs-lookup"><span data-stu-id="68352-168">the webhook app object Id for aad auth</span></span>

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

### <span data-ttu-id="68352-169">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="68352-169">-PhoneNumber</span></span>
<span data-ttu-id="68352-170">Specifica il numero di telefono per il ricevitore SMS.</span><span class="sxs-lookup"><span data-stu-id="68352-170">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="68352-171">-Area geografica</span><span class="sxs-lookup"><span data-stu-id="68352-171">-Region</span></span>
<span data-ttu-id="68352-172">Area ITSM di questo ricevitore</span><span class="sxs-lookup"><span data-stu-id="68352-172">the itsm Region of this receiver</span></span>

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

### <span data-ttu-id="68352-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68352-173">-ResourceId</span></span>
<span data-ttu-id="68352-174">ResourceId</span><span class="sxs-lookup"><span data-stu-id="68352-174">the ResourceId</span></span>

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

### <span data-ttu-id="68352-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="68352-175">-RoleId</span></span>
<span data-ttu-id="68352-176">ID ruolo ARM del destinatario</span><span class="sxs-lookup"><span data-stu-id="68352-176">The arm role id of the receiver</span></span>

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

### <span data-ttu-id="68352-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="68352-177">-RunbookName</span></span>
<span data-ttu-id="68352-178">RunbookName</span><span class="sxs-lookup"><span data-stu-id="68352-178">the RunbookName</span></span>

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

### <span data-ttu-id="68352-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="68352-179">-ServiceUri</span></span>
<span data-ttu-id="68352-180">Specifica l'URI per il ricevitore webhook.</span><span class="sxs-lookup"><span data-stu-id="68352-180">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="68352-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-181">-SmsReceiver</span></span>
<span data-ttu-id="68352-182">Specifica la creazione di un ricevitore SMS</span><span class="sxs-lookup"><span data-stu-id="68352-182">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="68352-183">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="68352-183">-TenantId</span></span>
<span data-ttu-id="68352-184">ID tenant per AAD auth</span><span class="sxs-lookup"><span data-stu-id="68352-184">the tenant id for aad auth</span></span>

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

### <span data-ttu-id="68352-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="68352-185">-TicketConfiguration</span></span>
<span data-ttu-id="68352-186">ITSM TicketConfiguration di questo ricevitore</span><span class="sxs-lookup"><span data-stu-id="68352-186">the itsm TicketConfiguration of this receiver</span></span>

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

### <span data-ttu-id="68352-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="68352-187">-UseAadAuth</span></span>
<span data-ttu-id="68352-188">contrassegno per l'uso di Add auth</span><span class="sxs-lookup"><span data-stu-id="68352-188">the flag to use add auth</span></span>

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

### <span data-ttu-id="68352-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="68352-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="68352-190">Il contrassegno se usare lo schema di avviso comune.</span><span class="sxs-lookup"><span data-stu-id="68352-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="68352-191">Questo valore sarà neglectedfor SMS, Azure app push, ITSM e Voice recievers.</span><span class="sxs-lookup"><span data-stu-id="68352-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

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

### <span data-ttu-id="68352-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="68352-192">-VoiceCountryCode</span></span>
<span data-ttu-id="68352-193">Codice paese del ricevitore vocale</span><span class="sxs-lookup"><span data-stu-id="68352-193">The country code of the voice receiver</span></span>

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

### <span data-ttu-id="68352-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="68352-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="68352-195">Numero di telefono del ricevitore vocale</span><span class="sxs-lookup"><span data-stu-id="68352-195">The phone number of the voice receiver</span></span>

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

### <span data-ttu-id="68352-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-196">-VoiceReceiver</span></span>
<span data-ttu-id="68352-197">Creare un ricevitore vocale</span><span class="sxs-lookup"><span data-stu-id="68352-197">Create a voice receiver</span></span>

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

### <span data-ttu-id="68352-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="68352-198">-WebhookReceiver</span></span>
<span data-ttu-id="68352-199">Specifica la creazione di un ricevitore webhook</span><span class="sxs-lookup"><span data-stu-id="68352-199">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="68352-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="68352-200">-WebhookResourceId</span></span>
<span data-ttu-id="68352-201">WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="68352-201">the WebhookResourceId</span></span>

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

### <span data-ttu-id="68352-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="68352-202">-WorkspaceId</span></span>
<span data-ttu-id="68352-203">ID area di lavoro di ITSM di questo ricevitore</span><span class="sxs-lookup"><span data-stu-id="68352-203">the itsm workspace id of this receiver</span></span>

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

### <span data-ttu-id="68352-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68352-204">CommonParameters</span></span>
<span data-ttu-id="68352-205">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68352-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68352-206">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68352-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68352-207">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68352-207">INPUTS</span></span>

### <span data-ttu-id="68352-208">System. String</span><span class="sxs-lookup"><span data-stu-id="68352-208">System.String</span></span>

### <span data-ttu-id="68352-209">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="68352-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="68352-210">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68352-210">OUTPUTS</span></span>

### <span data-ttu-id="68352-211">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="68352-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="68352-212">Note</span><span class="sxs-lookup"><span data-stu-id="68352-212">NOTES</span></span>

## <span data-ttu-id="68352-213">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68352-213">RELATED LINKS</span></span>

<span data-ttu-id="68352-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="68352-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>

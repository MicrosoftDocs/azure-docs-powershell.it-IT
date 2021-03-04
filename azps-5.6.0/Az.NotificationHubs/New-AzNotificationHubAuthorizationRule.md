---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7E9CBEE9-DD5F-4552-9187-ECBBEF6174B0
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 74ad4f80a25250129d050ed3a2769dca6f776376
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951277"
---
# <span data-ttu-id="3a8e2-101">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3a8e2-101">New-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="3a8e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a8e2-102">SYNOPSIS</span></span>
<span data-ttu-id="3a8e2-103">Crea una regola di autorizzazione e la assegna a un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="3a8e2-103">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

## <span data-ttu-id="3a8e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a8e2-104">SYNTAX</span></span>

### <span data-ttu-id="3a8e2-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a8e2-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a8e2-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a8e2-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a8e2-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3a8e2-107">DESCRIPTION</span></span>
<span data-ttu-id="3a8e2-108">Il cmdlet **New-AzNotificationHubAuthorizationRule** crea una regola di autorizzazione firma di accesso condiviso dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="3a8e2-108">The **New-AzNotificationHubAuthorizationRule** cmdlet creates a notification hub Shared Access Signature (SAS) authorization rule.</span></span>
<span data-ttu-id="3a8e2-109">Le regole di autorizzazione vengono usate per gestire l'accesso agli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="3a8e2-109">Authorization rules are used to manage access to your notification hubs.</span></span>
<span data-ttu-id="3a8e2-110">Questa operazione viene eseguita con la creazione di collegamenti, come URI, in base a diversi livelli di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="3a8e2-110">This is done by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="3a8e2-111">I client vengono indirizzati a uno di questi URI in base al livello di autorizzazione appropriato.</span><span class="sxs-lookup"><span data-stu-id="3a8e2-111">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="3a8e2-112">Ad esempio, un client con l'autorizzazione di ascolto verrà indirizzato all'URI per tale autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="3a8e2-112">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

## <span data-ttu-id="3a8e2-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a8e2-113">EXAMPLES</span></span>

### <span data-ttu-id="3a8e2-114">Esempio 1: Creare una regola di autorizzazione dell'hub di notifica</span><span class="sxs-lookup"><span data-stu-id="3a8e2-114">Example 1: Create a notification hub authorization rule</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\ExternalAccessRule.json"
```

<span data-ttu-id="3a8e2-115">Questo comando crea una nuova regola di autorizzazione e la assegna all'hub di notifica denominato ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="3a8e2-115">This command creates a new authorization rule and assigns it to the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="3a8e2-116">Questo hub si trova nello spazio dei nomi ContosoCliente ed è assegnato al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="3a8e2-116">This hub is located in the ContosoNamespace namespace and is assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="3a8e2-117">Si noti che tutte le informazioni di configurazione per la regola, incluso il nome della regola, verranno prese dal file di input C:\Configuration\ExternalAccessRule.jsattiva.</span><span class="sxs-lookup"><span data-stu-id="3a8e2-117">Note that all the configuration information for the rule, including the rule name, will be taken from the input file C:\Configuration\ExternalAccessRule.json.</span></span>

## <span data-ttu-id="3a8e2-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a8e2-118">PARAMETERS</span></span>

### <span data-ttu-id="3a8e2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a8e2-119">-DefaultProfile</span></span>
<span data-ttu-id="3a8e2-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="3a8e2-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a8e2-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="3a8e2-121">-InputFile</span></span>
<span data-ttu-id="3a8e2-122">Specifica il file di input per la regola di autorizzazione creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a8e2-122">Specifies the input file for the authorization rule that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a8e2-123">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3a8e2-123">-Namespace</span></span>
<span data-ttu-id="3a8e2-124">Specifica lo spazio dei nomi a cui vengono assegnate le regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="3a8e2-124">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="3a8e2-125">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="3a8e2-125">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a8e2-126">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="3a8e2-126">-NotificationHub</span></span>
<span data-ttu-id="3a8e2-127">Specifica l'hub di notifica a cui verranno assegnate le regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="3a8e2-127">Specifies the notification hub that the authorization rules will be assigned to.</span></span>
<span data-ttu-id="3a8e2-128">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma usata da tali client.</span><span class="sxs-lookup"><span data-stu-id="3a8e2-128">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="3a8e2-129">Tenere presente che è necessario specificare il nome di un hub di notifica esistente.</span><span class="sxs-lookup"><span data-stu-id="3a8e2-129">Note that you must specify the name of an existing notification hub.</span></span>
<span data-ttu-id="3a8e2-130">Il cmdlet **New-AzNotificationHubAuthorizationRule** non può creare nuovi hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="3a8e2-130">The **New-AzNotificationHubAuthorizationRule** cmdlet cannot create new notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a8e2-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3a8e2-131">-ResourceGroup</span></span>
<span data-ttu-id="3a8e2-132">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="3a8e2-132">Specifies the resource group that the notification hub is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a8e2-133">-SASRule</span><span class="sxs-lookup"><span data-stu-id="3a8e2-133">-SASRule</span></span>
<span data-ttu-id="3a8e2-134">Specifica **l'oggetto SharedAccessAuthorizationRuleAttributes** contenente informazioni di configurazione per le nuove regole.</span><span class="sxs-lookup"><span data-stu-id="3a8e2-134">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a8e2-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a8e2-135">-Confirm</span></span>
<span data-ttu-id="3a8e2-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a8e2-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a8e2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a8e2-137">-WhatIf</span></span>
<span data-ttu-id="3a8e2-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a8e2-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a8e2-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a8e2-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a8e2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a8e2-140">CommonParameters</span></span>
<span data-ttu-id="3a8e2-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a8e2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a8e2-142">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a8e2-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a8e2-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="3a8e2-143">INPUTS</span></span>

### <span data-ttu-id="3a8e2-144">System.String</span><span class="sxs-lookup"><span data-stu-id="3a8e2-144">System.String</span></span>

## <span data-ttu-id="3a8e2-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a8e2-145">OUTPUTS</span></span>

### <span data-ttu-id="3a8e2-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="3a8e2-146">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="3a8e2-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="3a8e2-147">NOTES</span></span>

## <span data-ttu-id="3a8e2-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a8e2-148">RELATED LINKS</span></span>

[<span data-ttu-id="3a8e2-149">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3a8e2-149">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="3a8e2-150">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3a8e2-150">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="3a8e2-151">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3a8e2-151">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)



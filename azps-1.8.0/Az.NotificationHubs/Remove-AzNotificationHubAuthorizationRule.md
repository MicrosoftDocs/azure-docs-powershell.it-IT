---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 6ad682ad80400fa84034b35804c9756775d05eeb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677843"
---
# <span data-ttu-id="ae39b-101">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ae39b-101">Remove-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="ae39b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae39b-102">SYNOPSIS</span></span>
<span data-ttu-id="ae39b-103">Rimuove una regola di autorizzazione da un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ae39b-103">Removes an authorization rule from a notification hub.</span></span>

## <span data-ttu-id="ae39b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae39b-104">SYNTAX</span></span>

```
Remove-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae39b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae39b-105">DESCRIPTION</span></span>
<span data-ttu-id="ae39b-106">Il cmdlet **Remove-AzNotificationHubAuthorizationRule** rimuove una regola di autorizzazione della firma di accesso condiviso (SAS) da un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ae39b-106">The **Remove-AzNotificationHubAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>
<span data-ttu-id="ae39b-107">Le regole di autorizzazione gestiscono l'accesso agli hub di notifica tramite la creazione di collegamenti, come URI, in base a livelli di autorizzazione diversi.</span><span class="sxs-lookup"><span data-stu-id="ae39b-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="ae39b-108">I livelli di autorizzazione possono essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="ae39b-108">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="ae39b-109">Ascoltare</span><span class="sxs-lookup"><span data-stu-id="ae39b-109">Listen</span></span>
- <span data-ttu-id="ae39b-110">Invia</span><span class="sxs-lookup"><span data-stu-id="ae39b-110">Send</span></span>
- <span data-ttu-id="ae39b-111">I client di gestione vengono indirizzati a uno di questi URI in base al livello di autorizzazione appropriato.</span><span class="sxs-lookup"><span data-stu-id="ae39b-111">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="ae39b-112">Ad esempio, un client assegnato l'autorizzazione Listen verrà indirizzato all'URI per l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="ae39b-112">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="ae39b-113">La rimozione di una regola di autorizzazione consente inoltre di rimuovere l'autorizzazione utente corrispondente.</span><span class="sxs-lookup"><span data-stu-id="ae39b-113">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="ae39b-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae39b-114">EXAMPLES</span></span>

### <span data-ttu-id="ae39b-115">Esempio 1: rimuovere una regola di autorizzazione da un hub di notifica</span><span class="sxs-lookup"><span data-stu-id="ae39b-115">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="ae39b-116">Questo comando rimuove la regola di autorizzazione denominata ListenRule dall'hub di notifica denominato ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="ae39b-116">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="ae39b-117">Quando si esegue questo comando, è necessario specificare sia lo spazio dei nomi che il gruppo di risorse a cui è assegnato l'hub.</span><span class="sxs-lookup"><span data-stu-id="ae39b-117">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="ae39b-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae39b-118">PARAMETERS</span></span>

### <span data-ttu-id="ae39b-119">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ae39b-119">-AuthorizationRule</span></span>
<span data-ttu-id="ae39b-120">Specifica il nome della regola di autenticazione SAS rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae39b-120">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae39b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae39b-121">-DefaultProfile</span></span>
<span data-ttu-id="ae39b-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ae39b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae39b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ae39b-123">-Force</span></span>
<span data-ttu-id="ae39b-124">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ae39b-124">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae39b-125">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ae39b-125">-Namespace</span></span>
<span data-ttu-id="ae39b-126">Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ae39b-126">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="ae39b-127">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ae39b-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="ae39b-128">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="ae39b-128">-NotificationHub</span></span>
<span data-ttu-id="ae39b-129">Specifica l'hub di notifica a cui sono assegnate le regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="ae39b-129">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="ae39b-130">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma.</span><span class="sxs-lookup"><span data-stu-id="ae39b-130">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="ae39b-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ae39b-131">-ResourceGroup</span></span>
<span data-ttu-id="ae39b-132">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ae39b-132">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="ae39b-133">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ae39b-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="ae39b-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ae39b-134">-Confirm</span></span>
<span data-ttu-id="ae39b-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae39b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae39b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae39b-136">-WhatIf</span></span>
<span data-ttu-id="ae39b-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae39b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae39b-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae39b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae39b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae39b-139">CommonParameters</span></span>
<span data-ttu-id="ae39b-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae39b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae39b-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae39b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae39b-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae39b-142">INPUTS</span></span>

### <span data-ttu-id="ae39b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ae39b-143">System.String</span></span>

## <span data-ttu-id="ae39b-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae39b-144">OUTPUTS</span></span>

### <span data-ttu-id="ae39b-145">System. void</span><span class="sxs-lookup"><span data-stu-id="ae39b-145">System.Void</span></span>

## <span data-ttu-id="ae39b-146">Note</span><span class="sxs-lookup"><span data-stu-id="ae39b-146">NOTES</span></span>

## <span data-ttu-id="ae39b-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae39b-147">RELATED LINKS</span></span>

[<span data-ttu-id="ae39b-148">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ae39b-148">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="ae39b-149">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ae39b-149">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="ae39b-150">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ae39b-150">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


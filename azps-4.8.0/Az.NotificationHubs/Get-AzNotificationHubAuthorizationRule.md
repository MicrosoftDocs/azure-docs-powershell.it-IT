---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 7c85bafabede1c905efaf000721e5f8d6bee1572
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032279"
---
# <span data-ttu-id="5b2e6-101">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5b2e6-101">Get-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="5b2e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b2e6-102">SYNOPSIS</span></span>
<span data-ttu-id="5b2e6-103">Ottiene informazioni sulle regole di autorizzazione associate a un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5b2e6-103">Gets information about the authorization rules associated with a notification hub.</span></span>

## <span data-ttu-id="5b2e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b2e6-104">SYNTAX</span></span>

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b2e6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b2e6-105">DESCRIPTION</span></span>
<span data-ttu-id="5b2e6-106">Il cmdlet **Get-AzNotificationHubAuthorizationRule** ottiene informazioni sulle regole di autorizzazione della firma di accesso condiviso (SAS) associate a un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5b2e6-106">The **Get-AzNotificationHubAuthorizationRule** cmdlet gets information about the Shared Access Signature (SAS) authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="5b2e6-107">Il cmdlet restituisce informazioni su tutte le regole associate a un hub o, includendo il parametro *AuthorizationRule* , ottiene informazioni su una regola specifica.</span><span class="sxs-lookup"><span data-stu-id="5b2e6-107">The cmdlet returns information about all the rules associated with a hub or, by including the *AuthorizationRule* parameter, gets information about a specific rule.</span></span>
<span data-ttu-id="5b2e6-108">Le regole di autorizzazione gestiscono l'accesso agli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5b2e6-108">Authorization rules manage access to your notification hubs.</span></span>
<span data-ttu-id="5b2e6-109">Una regola di autorizzazione creerà collegamenti, come URI, in base a livelli di autorizzazione diversi.</span><span class="sxs-lookup"><span data-stu-id="5b2e6-109">An authorization rule will create links, as a URI, based on different permission levels.</span></span>
<span data-ttu-id="5b2e6-110">I client vengono indirizzati a uno di questi URI in base al livello di autorizzazione appropriato.</span><span class="sxs-lookup"><span data-stu-id="5b2e6-110">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="5b2e6-111">Ad esempio, un client con l'autorizzazione Listen verrà indirizzato all'URI per l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="5b2e6-111">For instance, a client with the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="5b2e6-112">Il cmdlet **Get-AzNotificationHubAuthorizationRule** ottiene solo le informazioni sulle regole di autorizzazione associate a un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5b2e6-112">The **Get-AzNotificationHubAuthorizationRule** cmdlet only gets information about the authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="5b2e6-113">Per ottenere informazioni sull'hub stesso, USA Get-AzNotificationHub.</span><span class="sxs-lookup"><span data-stu-id="5b2e6-113">To get information about the hub itself, use Get-AzNotificationHub.</span></span>

## <span data-ttu-id="5b2e6-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b2e6-114">EXAMPLES</span></span>

### <span data-ttu-id="5b2e6-115">Esempio 1: ottenere informazioni per tutte le regole di autorizzazione assegnate a un hub di notifica</span><span class="sxs-lookup"><span data-stu-id="5b2e6-115">Example 1: Get information for all authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="5b2e6-116">Questo comando ottiene le informazioni per tutte le regole di autorizzazione assegnate all'hub di notifica denominato ContosoInternalHub nello spazio dei nomi ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="5b2e6-116">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="5b2e6-117">Devi specificare lo spazio dei nomi in cui si trova l'hub e il gruppo di risorse a cui è stato assegnato l'hub.</span><span class="sxs-lookup"><span data-stu-id="5b2e6-117">You must specify the namespace where the hub is located as well as the resource group that the hub has been assigned to.</span></span>

### <span data-ttu-id="5b2e6-118">Esempio 2: ottenere informazioni per le regole di autorizzazione assegnate a un hub di notifica</span><span class="sxs-lookup"><span data-stu-id="5b2e6-118">Example 2: Get information for an authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="5b2e6-119">Questo comando ottiene le informazioni per tutte le regole di autorizzazione assegnate all'hub di notifica denominato ContosoInternalHub nello spazio dei nomi ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="5b2e6-119">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="5b2e6-120">Il comando usa il parametro *AuthorizationRule* per limitare i dati restituiti a una singola regola di autorizzazione denominata ListenRule.</span><span class="sxs-lookup"><span data-stu-id="5b2e6-120">The command uses the *AuthorizationRule* parameter to limit the returned data to a single authorization rule named ListenRule.</span></span>

## <span data-ttu-id="5b2e6-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b2e6-121">PARAMETERS</span></span>

### <span data-ttu-id="5b2e6-122">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5b2e6-122">-AuthorizationRule</span></span>
<span data-ttu-id="5b2e6-123">Specifica il nome di una regola di autenticazione SAS.</span><span class="sxs-lookup"><span data-stu-id="5b2e6-123">Specifies the name of an SAS authentication rule.</span></span>
<span data-ttu-id="5b2e6-124">Queste regole determinano il tipo di accesso che gli utenti hanno all'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5b2e6-124">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b2e6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b2e6-125">-DefaultProfile</span></span>
<span data-ttu-id="5b2e6-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5b2e6-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b2e6-127">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5b2e6-127">-Namespace</span></span>
<span data-ttu-id="5b2e6-128">Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5b2e6-128">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="5b2e6-129">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5b2e6-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="5b2e6-130">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="5b2e6-130">-NotificationHub</span></span>
<span data-ttu-id="5b2e6-131">Specifica l'hub di notifica che questo cmdlet assegna le regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="5b2e6-131">Specifies the notification hub that this cmdlet assigns authorization rules.</span></span>
<span data-ttu-id="5b2e6-132">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma utilizzata da tali client.</span><span class="sxs-lookup"><span data-stu-id="5b2e6-132">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="5b2e6-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5b2e6-133">-ResourceGroup</span></span>
<span data-ttu-id="5b2e6-134">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5b2e6-134">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="5b2e6-135">I gruppi di risorse organizzano elementi come spazi dei nomi, hub di notifica e regole di autorizzazione in modi che semplificano la gestione delle scorte e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5b2e6-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simplify inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="5b2e6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b2e6-136">CommonParameters</span></span>
<span data-ttu-id="5b2e6-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b2e6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b2e6-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b2e6-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b2e6-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b2e6-139">INPUTS</span></span>

### <span data-ttu-id="5b2e6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5b2e6-140">System.String</span></span>

## <span data-ttu-id="5b2e6-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b2e6-141">OUTPUTS</span></span>

### <span data-ttu-id="5b2e6-142">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="5b2e6-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="5b2e6-143">Note</span><span class="sxs-lookup"><span data-stu-id="5b2e6-143">NOTES</span></span>

## <span data-ttu-id="5b2e6-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b2e6-144">RELATED LINKS</span></span>

[<span data-ttu-id="5b2e6-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5b2e6-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="5b2e6-146">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5b2e6-146">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="5b2e6-147">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5b2e6-147">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="5b2e6-148">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5b2e6-148">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)



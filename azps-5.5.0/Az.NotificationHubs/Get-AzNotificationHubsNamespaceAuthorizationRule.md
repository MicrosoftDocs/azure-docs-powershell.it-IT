---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206426"
---
# <span data-ttu-id="5749d-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5749d-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="5749d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5749d-102">SYNOPSIS</span></span>
<span data-ttu-id="5749d-103">Ottiene informazioni sulle regole di autorizzazione associate a uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5749d-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

## <span data-ttu-id="5749d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5749d-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5749d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5749d-105">DESCRIPTION</span></span>
<span data-ttu-id="5749d-106">Il cmdlet **Get-AzNotificationHubsAuthorizationRule** restituisce informazioni sulle regole di autorizzazione della firma di accesso condiviso associate a uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5749d-106">The **Get-AzNotificationHubsNamespaceAuthorizationRule** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="5749d-107">È possibile restituire informazioni su tutte le regole associate allo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="5749d-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="5749d-108">In alternativa, includendo il *parametro AuthorizationRule,* è possibile restituire informazioni per una regola specifica.</span><span class="sxs-lookup"><span data-stu-id="5749d-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>
<span data-ttu-id="5749d-109">Le regole di autorizzazione gestiscono l'accesso agli spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="5749d-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="5749d-110">Questa operazione viene eseguita mediante la creazione di collegamenti, come URI, in base a diversi livelli di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="5749d-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="5749d-111">I livelli della piattaforma possono essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="5749d-111">Platform levels can be one of the following:</span></span> 
- <span data-ttu-id="5749d-112">Ascoltare</span><span class="sxs-lookup"><span data-stu-id="5749d-112">Listen</span></span>
- <span data-ttu-id="5749d-113">Invia</span><span class="sxs-lookup"><span data-stu-id="5749d-113">Send</span></span>
- <span data-ttu-id="5749d-114">La gestione dei client viene indirizzata a uno di questi URL in base al livello di autorizzazione appropriato.</span><span class="sxs-lookup"><span data-stu-id="5749d-114">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="5749d-115">Ad esempio, un client con l'autorizzazione di ascolto verrà indirizzato all'URI per tale autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="5749d-115">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="5749d-116">Questo cmdlet ottiene solo le regole di autorizzazione associate a uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="5749d-116">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="5749d-117">Per ottenere informazioni sullo spazio dei nomi stesso, usare Get-AzNotificationHubsHubsHubs.</span><span class="sxs-lookup"><span data-stu-id="5749d-117">To get information about the namespace itself, use Get-AzNotificationHubsNamespace.</span></span>

## <span data-ttu-id="5749d-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5749d-118">EXAMPLES</span></span>

### <span data-ttu-id="5749d-119">Esempio 1: Ottenere informazioni su tutte le regole di autorizzazione assegnate agli spazi dei nomi</span><span class="sxs-lookup"><span data-stu-id="5749d-119">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="5749d-120">Questo comando ottiene informazioni su tutte le regole di autorizzazione assegnate sia allo spazio dei nomi ContosoCliente che al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="5749d-120">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="5749d-121">Esempio 2: Ottenere informazioni su una regola di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="5749d-121">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="5749d-122">Questo comando ottiene informazioni su una singola regola di autorizzazione dello spazio dei nomi denominata ListenRule.</span><span class="sxs-lookup"><span data-stu-id="5749d-122">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="5749d-123">Quando si ottengono informazioni per una regola di autorizzazione specifica, è necessario includere lo spazio dei nomi e il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5749d-123">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="5749d-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5749d-124">PARAMETERS</span></span>

### <span data-ttu-id="5749d-125">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5749d-125">-AuthorizationRule</span></span>
<span data-ttu-id="5749d-126">Specifica il nome di una regola di autenticazione della firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="5749d-126">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="5749d-127">Queste regole determinano il tipo di accesso che gli utenti hanno allo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="5749d-127">These rules determine the type of access that users have to the namespace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5749d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5749d-128">-DefaultProfile</span></span>
<span data-ttu-id="5749d-129">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="5749d-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5749d-130">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5749d-130">-Namespace</span></span>
<span data-ttu-id="5749d-131">Specifica lo spazio dei nomi a cui vengono assegnate le regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="5749d-131">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="5749d-132">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5749d-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="5749d-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5749d-133">-ResourceGroup</span></span>
<span data-ttu-id="5749d-134">Specifica il gruppo di risorse a cui sono assegnate le regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="5749d-134">Specifies the resource group to which the authorization rules are assigned.</span></span>
<span data-ttu-id="5749d-135">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che consentono semplicemente la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5749d-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="5749d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5749d-136">CommonParameters</span></span>
<span data-ttu-id="5749d-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5749d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5749d-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5749d-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5749d-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="5749d-139">INPUTS</span></span>

### <span data-ttu-id="5749d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5749d-140">System.String</span></span>

## <span data-ttu-id="5749d-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5749d-141">OUTPUTS</span></span>

### <span data-ttu-id="5749d-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="5749d-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="5749d-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="5749d-143">NOTES</span></span>

## <span data-ttu-id="5749d-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5749d-144">RELATED LINKS</span></span>

[<span data-ttu-id="5749d-145">Get-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="5749d-145">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="5749d-146">New-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="5749d-146">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="5749d-147">Remove-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="5749d-147">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="5749d-148">Set-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="5749d-148">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)



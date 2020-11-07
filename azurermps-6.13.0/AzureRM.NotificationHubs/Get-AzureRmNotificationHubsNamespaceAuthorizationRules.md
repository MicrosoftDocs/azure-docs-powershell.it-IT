---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: 9546039459792d5ef72807d8466f728f2060a346
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685928"
---
# <span data-ttu-id="dc528-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="dc528-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="dc528-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dc528-102">SYNOPSIS</span></span>
<span data-ttu-id="dc528-103">Ottiene informazioni sulle regole di autorizzazione associate a uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="dc528-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc528-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dc528-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc528-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc528-105">DESCRIPTION</span></span>
<span data-ttu-id="dc528-106">Il cmdlet **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** restituisce informazioni sulle regole di autorizzazione della firma di accesso condiviso (SAS) associate a uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="dc528-106">The **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="dc528-107">Puoi restituire informazioni su tutte le regole associate allo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="dc528-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="dc528-108">In alternativa, e includendo il parametro *AuthorizationRule* , puoi restituire informazioni per una regola specifica.</span><span class="sxs-lookup"><span data-stu-id="dc528-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>
<span data-ttu-id="dc528-109">Le regole di autorizzazione gestiscono l'accesso agli spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="dc528-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="dc528-110">Questa operazione viene eseguita tramite la creazione di collegamenti, come URI, in base a livelli di autorizzazione diversi.</span><span class="sxs-lookup"><span data-stu-id="dc528-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="dc528-111">I livelli della piattaforma possono essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="dc528-111">Platform levels can be one of the following:</span></span> 
- <span data-ttu-id="dc528-112">Ascoltare</span><span class="sxs-lookup"><span data-stu-id="dc528-112">Listen</span></span>
- <span data-ttu-id="dc528-113">Invia</span><span class="sxs-lookup"><span data-stu-id="dc528-113">Send</span></span>
- <span data-ttu-id="dc528-114">I client di gestione vengono indirizzati a uno di questi URI in base al livello di autorizzazione appropriato.</span><span class="sxs-lookup"><span data-stu-id="dc528-114">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="dc528-115">Ad esempio, un client assegnato l'autorizzazione Listen verrà indirizzato all'URI per l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="dc528-115">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="dc528-116">Questo cmdlet ottiene solo le regole di autorizzazione associate a uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="dc528-116">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="dc528-117">Per ottenere informazioni sullo spazio dei nomi stesso, USA Get-AzureRmNotificationHubsNamespace.</span><span class="sxs-lookup"><span data-stu-id="dc528-117">To get information about the namespace itself, use Get-AzureRmNotificationHubsNamespace.</span></span>

## <span data-ttu-id="dc528-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dc528-118">EXAMPLES</span></span>

### <span data-ttu-id="dc528-119">Esempio 1: ottenere informazioni su tutte le regole di autorizzazione assegnate agli spazi dei nomi</span><span class="sxs-lookup"><span data-stu-id="dc528-119">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="dc528-120">Questo comando consente di ottenere informazioni su tutte le regole di autorizzazione assegnate sia allo spazio dei nomi ContosoNamespace che al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="dc528-120">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="dc528-121">Esempio 2: ottenere informazioni su una regola di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="dc528-121">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="dc528-122">Questo comando consente di ottenere informazioni su una singola regola di autorizzazione dello spazio dei nomi denominata ListenRule.</span><span class="sxs-lookup"><span data-stu-id="dc528-122">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="dc528-123">È necessario includere lo spazio dei nomi e il gruppo di risorse quando si ottengono informazioni per una specifica regola di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="dc528-123">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="dc528-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dc528-124">PARAMETERS</span></span>

### <span data-ttu-id="dc528-125">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="dc528-125">-AuthorizationRule</span></span>
<span data-ttu-id="dc528-126">Specifica il nome di una regola di autenticazione SAS.</span><span class="sxs-lookup"><span data-stu-id="dc528-126">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="dc528-127">Queste regole determinano il tipo di accesso che gli utenti hanno allo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="dc528-127">These rules determine the type of access that users have to the namespace.</span></span>

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

### <span data-ttu-id="dc528-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc528-128">-DefaultProfile</span></span>
<span data-ttu-id="dc528-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="dc528-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc528-130">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dc528-130">-Namespace</span></span>
<span data-ttu-id="dc528-131">Specifica lo spazio dei nomi a cui vengono assegnate le regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="dc528-131">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="dc528-132">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="dc528-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="dc528-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dc528-133">-ResourceGroup</span></span>
<span data-ttu-id="dc528-134">Specifica il gruppo di risorse a cui sono assegnate le regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="dc528-134">Specifies the resource group to which the authorization rules are assigned.</span></span>
<span data-ttu-id="dc528-135">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dc528-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="dc528-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc528-136">CommonParameters</span></span>
<span data-ttu-id="dc528-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc528-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc528-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc528-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc528-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dc528-139">INPUTS</span></span>

### <span data-ttu-id="dc528-140">System. String</span><span class="sxs-lookup"><span data-stu-id="dc528-140">System.String</span></span>

## <span data-ttu-id="dc528-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dc528-141">OUTPUTS</span></span>

### <span data-ttu-id="dc528-142">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="dc528-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="dc528-143">Note</span><span class="sxs-lookup"><span data-stu-id="dc528-143">NOTES</span></span>

## <span data-ttu-id="dc528-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dc528-144">RELATED LINKS</span></span>

[<span data-ttu-id="dc528-145">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="dc528-145">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="dc528-146">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="dc528-146">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="dc528-147">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="dc528-147">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="dc528-148">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="dc528-148">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)



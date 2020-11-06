---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: bb92344616c79db26b37bd9b18bdff7973946c24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513167"
---
# <span data-ttu-id="8cba5-101">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="8cba5-101">Remove-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="8cba5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8cba5-102">SYNOPSIS</span></span>
<span data-ttu-id="8cba5-103">Rimuove una regola di autorizzazione da un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="8cba5-103">Removes an authorization rule from a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cba5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cba5-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cba5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cba5-105">DESCRIPTION</span></span>
<span data-ttu-id="8cba5-106">Il cmdlet **Remove-AzureRmNotificationHubAuthorizationRules** rimuove una regola di autorizzazione della firma di accesso condiviso (SAS) da un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="8cba5-106">The **Remove-AzureRmNotificationHubAuthorizationRules** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>

<span data-ttu-id="8cba5-107">Le regole di autorizzazione gestiscono l'accesso agli hub di notifica tramite la creazione di collegamenti, come URI, in base a livelli di autorizzazione diversi.</span><span class="sxs-lookup"><span data-stu-id="8cba5-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="8cba5-108">I livelli di autorizzazione possono essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="8cba5-108">Permission levels can be one of the following:</span></span> 

- <span data-ttu-id="8cba5-109">Ascoltare</span><span class="sxs-lookup"><span data-stu-id="8cba5-109">Listen</span></span>
- <span data-ttu-id="8cba5-110">Invia</span><span class="sxs-lookup"><span data-stu-id="8cba5-110">Send</span></span>
- <span data-ttu-id="8cba5-111">Gestire</span><span class="sxs-lookup"><span data-stu-id="8cba5-111">Manage</span></span>

<span data-ttu-id="8cba5-112">I client vengono indirizzati a uno di questi URI in base al livello di autorizzazione appropriato.</span><span class="sxs-lookup"><span data-stu-id="8cba5-112">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="8cba5-113">Ad esempio, un client assegnato l'autorizzazione Listen verrà indirizzato all'URI per l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="8cba5-113">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="8cba5-114">La rimozione di una regola di autorizzazione consente inoltre di rimuovere l'autorizzazione utente corrispondente.</span><span class="sxs-lookup"><span data-stu-id="8cba5-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="8cba5-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cba5-115">EXAMPLES</span></span>

### <span data-ttu-id="8cba5-116">Esempio 1: rimuovere una regola di autorizzazione da un hub di notifica</span><span class="sxs-lookup"><span data-stu-id="8cba5-116">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="8cba5-117">Questo comando rimuove la regola di autorizzazione denominata ListenRule dall'hub di notifica denominato ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="8cba5-117">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="8cba5-118">Quando si esegue questo comando, è necessario specificare sia lo spazio dei nomi che il gruppo di risorse a cui è assegnato l'hub.</span><span class="sxs-lookup"><span data-stu-id="8cba5-118">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="8cba5-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8cba5-119">PARAMETERS</span></span>

### <span data-ttu-id="8cba5-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8cba5-120">-AuthorizationRule</span></span>
<span data-ttu-id="8cba5-121">Specifica il nome della regola di autenticazione SAS rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cba5-121">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8cba5-122">-Force</span><span class="sxs-lookup"><span data-stu-id="8cba5-122">-Force</span></span>
<span data-ttu-id="8cba5-123">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="8cba5-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8cba5-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8cba5-124">-Namespace</span></span>
<span data-ttu-id="8cba5-125">Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="8cba5-125">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="8cba5-126">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="8cba5-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="8cba5-127">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="8cba5-127">-NotificationHub</span></span>
<span data-ttu-id="8cba5-128">Specifica l'hub di notifica a cui sono assegnate le regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="8cba5-128">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="8cba5-129">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma.</span><span class="sxs-lookup"><span data-stu-id="8cba5-129">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="8cba5-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8cba5-130">-ResourceGroup</span></span>
<span data-ttu-id="8cba5-131">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="8cba5-131">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="8cba5-132">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cba5-132">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="8cba5-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8cba5-133">-Confirm</span></span>
<span data-ttu-id="8cba5-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cba5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cba5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cba5-135">-WhatIf</span></span>
<span data-ttu-id="8cba5-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cba5-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8cba5-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cba5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cba5-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cba5-138">-DefaultProfile</span></span>
<span data-ttu-id="8cba5-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8cba5-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cba5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cba5-140">CommonParameters</span></span>
<span data-ttu-id="8cba5-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cba5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cba5-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cba5-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cba5-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8cba5-143">INPUTS</span></span>

## <span data-ttu-id="8cba5-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cba5-144">OUTPUTS</span></span>

## <span data-ttu-id="8cba5-145">Note</span><span class="sxs-lookup"><span data-stu-id="8cba5-145">NOTES</span></span>

## <span data-ttu-id="8cba5-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cba5-146">RELATED LINKS</span></span>

[<span data-ttu-id="8cba5-147">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="8cba5-147">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="8cba5-148">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="8cba5-148">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="8cba5-149">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="8cba5-149">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)



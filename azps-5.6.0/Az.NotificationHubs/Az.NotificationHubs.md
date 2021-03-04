---
Module Name: Az.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link: https://docs.microsoft.com/powershell/module/az.notificationhubs
Help Version: 4.1.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
ms.openlocfilehash: f82f5ec814159bd71a83594a501df3561b747aee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951422"
---
# <span data-ttu-id="10e6b-101">Modulo Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="10e6b-101">Az.NotificationHubs Module</span></span>
## <span data-ttu-id="10e6b-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10e6b-102">Description</span></span>
<span data-ttu-id="10e6b-103">Questo argomento visualizza gli argomenti della Guida per i cmdlet dell'Hub di notifica di Azure.</span><span class="sxs-lookup"><span data-stu-id="10e6b-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="10e6b-104">Gli hub di notifica vengono usati per inviare notifiche push a più client, indipendentemente dalla piattaforma (iOS, Android, Windows Phone 8, Windows Store e così via) usata da tali client.</span><span class="sxs-lookup"><span data-stu-id="10e6b-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="10e6b-105">Questi hub sono approssimativamente equivalenti alle singole app: ogni app in genere avrà un proprio hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10e6b-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="10e6b-106">Gli hub di notifica sono organizzati in contenitori logici noti come spazi dei nomi e le regole di autorizzazione della firma di accesso condiviso vengono usate per gestire l'accesso agli hub e agli spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="10e6b-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="10e6b-107">Tutti questi elementi possono essere amministrati usando i cmdlet dell'Hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10e6b-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="10e6b-108">Cmdlet di Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="10e6b-108">Az.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="10e6b-109">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="10e6b-109">Get-AzNotificationHub</span></span>](Get-AzNotificationHub.md)
<span data-ttu-id="10e6b-110">Recupera informazioni sugli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10e6b-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="10e6b-111">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="10e6b-111">Get-AzNotificationHubAuthorizationRule</span></span>](Get-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="10e6b-112">Ottiene informazioni sulle regole di autorizzazione associate a un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10e6b-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="10e6b-113">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="10e6b-113">Get-AzNotificationHubListKey</span></span>](Get-AzNotificationHubListKey.md)
<span data-ttu-id="10e6b-114">Ottiene le stringhe di connessione primaria e secondaria associate a una regola di autorizzazione dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10e6b-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="10e6b-115">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="10e6b-115">Get-AzNotificationHubPNSCredential</span></span>](Get-AzNotificationHubPNSCredential.md)
<span data-ttu-id="10e6b-116">Ottiene le credenziali PNS per un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10e6b-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="10e6b-117">Get-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="10e6b-117">Get-AzNotificationHubsNamespace</span></span>](Get-AzNotificationHubsNamespace.md)
<span data-ttu-id="10e6b-118">Ottiene informazioni su uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10e6b-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="10e6b-119">Get-AzNotificationHubsAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="10e6b-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Get-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="10e6b-120">Ottiene informazioni sulle regole di autorizzazione associate a uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10e6b-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="10e6b-121">Get-AzNotificationHubsNotificationListKey</span><span class="sxs-lookup"><span data-stu-id="10e6b-121">Get-AzNotificationHubsNamespaceListKey</span></span>](Get-AzNotificationHubsNamespaceListKey.md)
<span data-ttu-id="10e6b-122">Ottiene le stringhe di connessione primaria e secondaria associate a una regola di autorizzazione dello spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10e6b-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="10e6b-123">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="10e6b-123">New-AzNotificationHub</span></span>](New-AzNotificationHub.md)
<span data-ttu-id="10e6b-124">Crea un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10e6b-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="10e6b-125">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="10e6b-125">New-AzNotificationHubAuthorizationRule</span></span>](New-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="10e6b-126">Crea una regola di autorizzazione e la assegna a un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10e6b-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="10e6b-127">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="10e6b-127">New-AzNotificationHubKey</span></span>](New-AzNotificationHubKey.md)
<span data-ttu-id="10e6b-128">Rigenerare la chiave della regola di autorizzazione per un elemento NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="10e6b-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="10e6b-129">New-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="10e6b-129">New-AzNotificationHubsNamespace</span></span>](New-AzNotificationHubsNamespace.md)
<span data-ttu-id="10e6b-130">Crea uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10e6b-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="10e6b-131">New-AzNotificationHubsAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="10e6b-131">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](New-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="10e6b-132">Crea una regola di autorizzazione e la assegna a uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10e6b-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="10e6b-133">New-AzNotificationHubs Una chiave di registro</span><span class="sxs-lookup"><span data-stu-id="10e6b-133">New-AzNotificationHubsNamespaceKey</span></span>](New-AzNotificationHubsNamespaceKey.md)
<span data-ttu-id="10e6b-134">Rigenerare la chiave della regola di autorizzazione per uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="10e6b-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="10e6b-135">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="10e6b-135">Remove-AzNotificationHub</span></span>](Remove-AzNotificationHub.md)
<span data-ttu-id="10e6b-136">Rimuove un hub di notifica esistente.</span><span class="sxs-lookup"><span data-stu-id="10e6b-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="10e6b-137">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="10e6b-137">Remove-AzNotificationHubAuthorizationRule</span></span>](Remove-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="10e6b-138">Rimuove una regola di autorizzazione da un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10e6b-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="10e6b-139">Remove-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="10e6b-139">Remove-AzNotificationHubsNamespace</span></span>](Remove-AzNotificationHubsNamespace.md)
<span data-ttu-id="10e6b-140">Rimuove uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10e6b-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="10e6b-141">Remove-AzNotificationHubsAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="10e6b-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Remove-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="10e6b-142">Rimuove una regola di autorizzazione da uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10e6b-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="10e6b-143">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="10e6b-143">Set-AzNotificationHub</span></span>](Set-AzNotificationHub.md)
<span data-ttu-id="10e6b-144">Imposta i valori delle proprietà per un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10e6b-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="10e6b-145">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="10e6b-145">Set-AzNotificationHubAuthorizationRule</span></span>](Set-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="10e6b-146">Imposta le regole di autorizzazione per un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10e6b-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="10e6b-147">Set-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="10e6b-147">Set-AzNotificationHubsNamespace</span></span>](Set-AzNotificationHubsNamespace.md)
<span data-ttu-id="10e6b-148">Imposta i valori delle proprietà per uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10e6b-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="10e6b-149">Set-AzNotificationHubsAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="10e6b-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Set-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="10e6b-150">Imposta le regole di autorizzazione per uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10e6b-150">Sets authorization rules for a notification hub namespace.</span></span>


---
Module Name: Az.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs
Help Version: 4.1.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
ms.openlocfilehash: dd39a8f87120ea7aaddb4570276e1e3060873e2f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336319"
---
# <span data-ttu-id="ba5ef-101">Modulo AZ. NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="ba5ef-101">Az.NotificationHubs Module</span></span>
## <span data-ttu-id="ba5ef-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba5ef-102">Description</span></span>
<span data-ttu-id="ba5ef-103">Questo argomento Mostra gli argomenti della Guida per i cmdlet di Azure Notification Hub.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="ba5ef-104">Gli hub di notifica vengono usati per inviare notifiche push a più client, indipendentemente dalla piattaforma (iOS, Android, Windows Phone 8, Windows Store e così via) usati da tali client.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="ba5ef-105">Questi hub equivalgono approssimativamente alle singole app: ognuna delle tue app avrà in genere un hub di notifica personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="ba5ef-106">Gli hub di notifica sono organizzati in contenitori logici noti come spazi dei nomi e le regole di autorizzazione della firma di accesso condiviso (SAS) vengono usate per gestire l'accesso agli hub e agli spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="ba5ef-107">Tutti questi elementi possono essere amministrati usando i cmdlet dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="ba5ef-108">Cmdlet AZ. NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="ba5ef-108">Az.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="ba5ef-109">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="ba5ef-109">Get-AzNotificationHub</span></span>](Get-AzNotificationHub.md)
<span data-ttu-id="ba5ef-110">Ottiene le informazioni sugli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="ba5ef-111">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ba5ef-111">Get-AzNotificationHubAuthorizationRule</span></span>](Get-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="ba5ef-112">Ottiene informazioni sulle regole di autorizzazione associate a un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="ba5ef-113">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="ba5ef-113">Get-AzNotificationHubListKey</span></span>](Get-AzNotificationHubListKey.md)
<span data-ttu-id="ba5ef-114">Ottiene le stringhe di connessione primarie e secondarie associate a una regola di autorizzazione dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="ba5ef-115">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="ba5ef-115">Get-AzNotificationHubPNSCredential</span></span>](Get-AzNotificationHubPNSCredential.md)
<span data-ttu-id="ba5ef-116">Ottiene le credenziali PNS per un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="ba5ef-117">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ba5ef-117">Get-AzNotificationHubsNamespace</span></span>](Get-AzNotificationHubsNamespace.md)
<span data-ttu-id="ba5ef-118">Ottiene informazioni su uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="ba5ef-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ba5ef-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Get-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="ba5ef-120">Ottiene informazioni sulle regole di autorizzazione associate a uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="ba5ef-121">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="ba5ef-121">Get-AzNotificationHubsNamespaceListKey</span></span>](Get-AzNotificationHubsNamespaceListKey.md)
<span data-ttu-id="ba5ef-122">Ottiene le stringhe di connessione primarie e secondarie associate a una regola di autorizzazione dello spazio dei nomi Hub notifica.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="ba5ef-123">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="ba5ef-123">New-AzNotificationHub</span></span>](New-AzNotificationHub.md)
<span data-ttu-id="ba5ef-124">Crea un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="ba5ef-125">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ba5ef-125">New-AzNotificationHubAuthorizationRule</span></span>](New-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="ba5ef-126">Crea una regola di autorizzazione e assegna la regola a un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="ba5ef-127">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="ba5ef-127">New-AzNotificationHubKey</span></span>](New-AzNotificationHubKey.md)
<span data-ttu-id="ba5ef-128">Rigenerare la chiave della regola di autorizzazione per un NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="ba5ef-129">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ba5ef-129">New-AzNotificationHubsNamespace</span></span>](New-AzNotificationHubsNamespace.md)
<span data-ttu-id="ba5ef-130">Crea uno spazio dei nomi Hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="ba5ef-131">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ba5ef-131">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](New-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="ba5ef-132">Crea una regola di autorizzazione e assegna la regola a uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="ba5ef-133">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="ba5ef-133">New-AzNotificationHubsNamespaceKey</span></span>](New-AzNotificationHubsNamespaceKey.md)
<span data-ttu-id="ba5ef-134">Rigenerare la chiave della regola di autorizzazione per uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="ba5ef-135">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="ba5ef-135">Remove-AzNotificationHub</span></span>](Remove-AzNotificationHub.md)
<span data-ttu-id="ba5ef-136">Rimuove un hub di notifica esistente.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="ba5ef-137">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ba5ef-137">Remove-AzNotificationHubAuthorizationRule</span></span>](Remove-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="ba5ef-138">Rimuove una regola di autorizzazione da un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="ba5ef-139">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ba5ef-139">Remove-AzNotificationHubsNamespace</span></span>](Remove-AzNotificationHubsNamespace.md)
<span data-ttu-id="ba5ef-140">Rimuove uno spazio dei nomi Hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="ba5ef-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ba5ef-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Remove-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="ba5ef-142">Rimuove una regola di autorizzazione da uno spazio dei nomi Hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="ba5ef-143">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="ba5ef-143">Set-AzNotificationHub</span></span>](Set-AzNotificationHub.md)
<span data-ttu-id="ba5ef-144">Imposta i valori delle proprietà per un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="ba5ef-145">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ba5ef-145">Set-AzNotificationHubAuthorizationRule</span></span>](Set-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="ba5ef-146">Imposta le regole di autorizzazione per un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="ba5ef-147">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ba5ef-147">Set-AzNotificationHubsNamespace</span></span>](Set-AzNotificationHubsNamespace.md)
<span data-ttu-id="ba5ef-148">Imposta i valori delle proprietà per uno spazio dei nomi Hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="ba5ef-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ba5ef-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Set-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="ba5ef-150">Imposta le regole di autorizzazione per uno spazio dei nomi Hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ba5ef-150">Sets authorization rules for a notification hub namespace.</span></span>


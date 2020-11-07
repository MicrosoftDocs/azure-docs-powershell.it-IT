---
Module Name: AzureRM.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/AzureRM.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/AzureRM.NotificationHubs.md
ms.openlocfilehash: e9f6fce095bd7ea4c494cf778587c3853f347c38
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2019
ms.locfileid: "93673260"
---
# <span data-ttu-id="fd931-101">Modulo AzureRM. NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="fd931-101">AzureRM.NotificationHubs Module</span></span>
## <span data-ttu-id="fd931-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd931-102">Description</span></span>
<span data-ttu-id="fd931-103">Questo argomento Mostra gli argomenti della Guida per i cmdlet di Azure Notification Hub.</span><span class="sxs-lookup"><span data-stu-id="fd931-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="fd931-104">Gli hub di notifica vengono usati per inviare notifiche push a più client, indipendentemente dalla piattaforma (iOS, Android, Windows Phone 8, Windows Store e così via) usati da tali client.</span><span class="sxs-lookup"><span data-stu-id="fd931-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="fd931-105">Questi hub equivalgono approssimativamente alle singole app: ognuna delle tue app avrà in genere un hub di notifica personalizzato.</span><span class="sxs-lookup"><span data-stu-id="fd931-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="fd931-106">Gli hub di notifica sono organizzati in contenitori logici noti come spazi dei nomi e le regole di autorizzazione della firma di accesso condiviso (SAS) vengono usate per gestire l'accesso agli hub e agli spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="fd931-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="fd931-107">Tutti questi elementi possono essere amministrati usando i cmdlet dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fd931-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="fd931-108">Cmdlet AzureRM. NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="fd931-108">AzureRM.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="fd931-109">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="fd931-109">Get-AzureRmNotificationHub</span></span>](Get-AzureRmNotificationHub.md)
<span data-ttu-id="fd931-110">Ottiene le informazioni sugli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fd931-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="fd931-111">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="fd931-111">Get-AzureRmNotificationHubAuthorizationRules</span></span>](Get-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="fd931-112">Ottiene informazioni sulle regole di autorizzazione associate a un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fd931-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="fd931-113">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="fd931-113">Get-AzureRmNotificationHubListKeys</span></span>](Get-AzureRmNotificationHubListKeys.md)
<span data-ttu-id="fd931-114">Ottiene le stringhe di connessione primarie e secondarie associate a una regola di autorizzazione dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fd931-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="fd931-115">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="fd931-115">Get-AzureRmNotificationHubPNSCredentials</span></span>](Get-AzureRmNotificationHubPNSCredentials.md)
<span data-ttu-id="fd931-116">Ottiene le credenziali PNS per un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fd931-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="fd931-117">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="fd931-117">Get-AzureRmNotificationHubsNamespace</span></span>](Get-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="fd931-118">Ottiene informazioni su uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fd931-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="fd931-119">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="fd931-119">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="fd931-120">Ottiene informazioni sulle regole di autorizzazione associate a uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fd931-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="fd931-121">Get-AzureRmNotificationHubsNamespaceListKeys</span><span class="sxs-lookup"><span data-stu-id="fd931-121">Get-AzureRmNotificationHubsNamespaceListKeys</span></span>](Get-AzureRmNotificationHubsNamespaceListKeys.md)
<span data-ttu-id="fd931-122">Ottiene le stringhe di connessione primarie e secondarie associate a una regola di autorizzazione dello spazio dei nomi Hub notifica.</span><span class="sxs-lookup"><span data-stu-id="fd931-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="fd931-123">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="fd931-123">New-AzureRmNotificationHub</span></span>](New-AzureRmNotificationHub.md)
<span data-ttu-id="fd931-124">Crea un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fd931-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="fd931-125">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="fd931-125">New-AzureRmNotificationHubAuthorizationRules</span></span>](New-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="fd931-126">Crea una regola di autorizzazione e assegna la regola a un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fd931-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="fd931-127">New-AzureRmNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="fd931-127">New-AzureRmNotificationHubKey</span></span>](New-AzureRmNotificationHubKey.md)
<span data-ttu-id="fd931-128">Rigenerare la chiave della regola di autorizzazione per un NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="fd931-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="fd931-129">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="fd931-129">New-AzureRmNotificationHubsNamespace</span></span>](New-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="fd931-130">Crea uno spazio dei nomi Hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fd931-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="fd931-131">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="fd931-131">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="fd931-132">Crea una regola di autorizzazione e assegna la regola a uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fd931-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="fd931-133">New-AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="fd931-133">New-AzureRmNotificationHubsNamespaceKey</span></span>](New-AzureRmNotificationHubsNamespaceKey.md)
<span data-ttu-id="fd931-134">Rigenerare la chiave della regola di autorizzazione per uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="fd931-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="fd931-135">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="fd931-135">Remove-AzureRmNotificationHub</span></span>](Remove-AzureRmNotificationHub.md)
<span data-ttu-id="fd931-136">Rimuove un hub di notifica esistente.</span><span class="sxs-lookup"><span data-stu-id="fd931-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="fd931-137">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="fd931-137">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](Remove-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="fd931-138">Rimuove una regola di autorizzazione da un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fd931-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="fd931-139">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="fd931-139">Remove-AzureRmNotificationHubsNamespace</span></span>](Remove-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="fd931-140">Rimuove uno spazio dei nomi Hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fd931-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="fd931-141">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="fd931-141">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="fd931-142">Rimuove una regola di autorizzazione da uno spazio dei nomi Hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fd931-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="fd931-143">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="fd931-143">Set-AzureRmNotificationHub</span></span>](Set-AzureRmNotificationHub.md)
<span data-ttu-id="fd931-144">Imposta i valori delle proprietà per un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fd931-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="fd931-145">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="fd931-145">Set-AzureRmNotificationHubAuthorizationRules</span></span>](Set-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="fd931-146">Imposta le regole di autorizzazione per un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fd931-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="fd931-147">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="fd931-147">Set-AzureRmNotificationHubsNamespace</span></span>](Set-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="fd931-148">Imposta i valori delle proprietà per uno spazio dei nomi Hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fd931-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="fd931-149">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="fd931-149">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="fd931-150">Imposta le regole di autorizzazione per uno spazio dei nomi Hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="fd931-150">Sets authorization rules for a notification hub namespace.</span></span>


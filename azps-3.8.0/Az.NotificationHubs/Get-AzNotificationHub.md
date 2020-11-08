---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: 6fc2cfd47d9b03fc02d935245d1ec87d6831d173
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022465"
---
# <span data-ttu-id="dead0-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="dead0-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="dead0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dead0-102">SYNOPSIS</span></span>
<span data-ttu-id="dead0-103">Ottiene le informazioni sugli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="dead0-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="dead0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dead0-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dead0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dead0-105">DESCRIPTION</span></span>
<span data-ttu-id="dead0-106">Il cmdlet **Get-AzNotificationHub** ottiene le informazioni sugli hub di notifica in uno spazio dei nomi specificato e assegnato a un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="dead0-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="dead0-107">Ad esempio, è possibile ottenere informazioni per tutti gli hub di notifica nello spazio dei nomi ContosoNamespace e assegnati al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="dead0-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="dead0-108">In alternativa, puoi usare il parametro *NotificationHub* per limitare i dati restituiti alle informazioni relative a un hub di notifica specifico.</span><span class="sxs-lookup"><span data-stu-id="dead0-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="dead0-109">Gli hub di notifica vengono usati per inviare notifiche push a più client, indipendentemente dalla piattaforma, ad esempio iOS, Android, Windows Phone 8 e Windows Store, usati da tali client.</span><span class="sxs-lookup"><span data-stu-id="dead0-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="dead0-110">Questi hub equivalgono approssimativamente alle singole app e ognuna delle tue app avrà in genere un hub di notifica personalizzato.</span><span class="sxs-lookup"><span data-stu-id="dead0-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="dead0-111">Questo cmdlet ottiene solo le informazioni sull'hub stesso.</span><span class="sxs-lookup"><span data-stu-id="dead0-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="dead0-112">Per ottenere informazioni sulle regole di autorizzazione, le stringhe di connessione e le credenziali del servizio di notifica della piattaforma, sono necessari altri cmdlet, ad esempio Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys e Get-AzNotificationHubPNSCredentials.</span><span class="sxs-lookup"><span data-stu-id="dead0-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="dead0-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dead0-113">EXAMPLES</span></span>

### <span data-ttu-id="dead0-114">Esempio 1: ottenere informazioni per tutti gli hub di notifica in uno spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="dead0-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="dead0-115">Questo comando ottiene le informazioni per tutti gli hub di notifica nello spazio dei nomi denominato ContosoNamespace assegnati al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="dead0-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="dead0-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dead0-116">PARAMETERS</span></span>

### <span data-ttu-id="dead0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dead0-117">-DefaultProfile</span></span>
<span data-ttu-id="dead0-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="dead0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dead0-119">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dead0-119">-Namespace</span></span>
<span data-ttu-id="dead0-120">Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="dead0-120">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="dead0-121">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="dead0-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="dead0-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="dead0-122">-NotificationHub</span></span>
<span data-ttu-id="dead0-123">Specifica il nome dell'hub di notifica ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dead0-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="dead0-124">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma utilizzata da tali client.</span><span class="sxs-lookup"><span data-stu-id="dead0-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="dead0-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dead0-125">-ResourceGroup</span></span>
<span data-ttu-id="dead0-126">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="dead0-126">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="dead0-127">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="dead0-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="dead0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dead0-128">CommonParameters</span></span>
<span data-ttu-id="dead0-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dead0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dead0-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dead0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dead0-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dead0-131">INPUTS</span></span>

### <span data-ttu-id="dead0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="dead0-132">System.String</span></span>

## <span data-ttu-id="dead0-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dead0-133">OUTPUTS</span></span>

### <span data-ttu-id="dead0-134">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="dead0-134">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="dead0-135">Note</span><span class="sxs-lookup"><span data-stu-id="dead0-135">NOTES</span></span>

## <span data-ttu-id="dead0-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dead0-136">RELATED LINKS</span></span>

[<span data-ttu-id="dead0-137">Get-AzNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="dead0-137">Get-AzNotificationHubAuthorizationRules</span></span>](./Get-AzNotificationHubAuthorizationRules.md)

[<span data-ttu-id="dead0-138">Get-AzNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="dead0-138">Get-AzNotificationHubListKeys</span></span>](./Get-AzNotificationHubListKeys.md)

[<span data-ttu-id="dead0-139">Get-AzNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="dead0-139">Get-AzNotificationHubPNSCredentials</span></span>](./Get-AzNotificationHubPNSCredentials.md)

[<span data-ttu-id="dead0-140">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="dead0-140">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="dead0-141">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="dead0-141">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="dead0-142">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="dead0-142">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)



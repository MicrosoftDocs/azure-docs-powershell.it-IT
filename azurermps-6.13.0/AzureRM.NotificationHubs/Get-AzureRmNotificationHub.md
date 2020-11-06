---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
ms.openlocfilehash: af2cc43b5f70c8a892e8b8fad0177a804689f007
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517403"
---
# <span data-ttu-id="f906f-101">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f906f-101">Get-AzureRmNotificationHub</span></span>

## <span data-ttu-id="f906f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f906f-102">SYNOPSIS</span></span>
<span data-ttu-id="f906f-103">Ottiene le informazioni sugli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="f906f-103">Gets information about your notification hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f906f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f906f-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f906f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f906f-105">DESCRIPTION</span></span>
<span data-ttu-id="f906f-106">Il cmdlet **Get-AzureRmNotificationHub** ottiene le informazioni sugli hub di notifica in uno spazio dei nomi specificato e assegnato a un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="f906f-106">The **Get-AzureRmNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="f906f-107">Ad esempio, è possibile ottenere informazioni per tutti gli hub di notifica nello spazio dei nomi ContosoNamespace e assegnati al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="f906f-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="f906f-108">In alternativa, puoi usare il parametro *NotificationHub* per limitare i dati restituiti alle informazioni relative a un hub di notifica specifico.</span><span class="sxs-lookup"><span data-stu-id="f906f-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="f906f-109">Gli hub di notifica vengono usati per inviare notifiche push a più client, indipendentemente dalla piattaforma, ad esempio iOS, Android, Windows Phone 8 e Windows Store, usati da tali client.</span><span class="sxs-lookup"><span data-stu-id="f906f-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="f906f-110">Questi hub equivalgono approssimativamente alle singole app e ognuna delle tue app avrà in genere un hub di notifica personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f906f-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="f906f-111">Questo cmdlet ottiene solo le informazioni sull'hub stesso.</span><span class="sxs-lookup"><span data-stu-id="f906f-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="f906f-112">Per ottenere informazioni sulle regole di autorizzazione, le stringhe di connessione e le credenziali del servizio di notifica della piattaforma, sono necessari altri cmdlet, ad esempio Get-AzureRmNotificationHubAuthorizationRules, Get-AzureRmNotificationHubListKeys e Get-AzureRmNotificationHubPNSCredentials.</span><span class="sxs-lookup"><span data-stu-id="f906f-112">Other cmdlets, such as Get-AzureRmNotificationHubAuthorizationRules, Get-AzureRmNotificationHubListKeys, and Get-AzureRmNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="f906f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f906f-113">EXAMPLES</span></span>

### <span data-ttu-id="f906f-114">Esempio 1: ottenere informazioni per tutti gli hub di notifica in uno spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="f906f-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="f906f-115">Questo comando ottiene le informazioni per tutti gli hub di notifica nello spazio dei nomi denominato ContosoNamespace assegnati al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="f906f-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="f906f-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f906f-116">PARAMETERS</span></span>

### <span data-ttu-id="f906f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f906f-117">-DefaultProfile</span></span>
<span data-ttu-id="f906f-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f906f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f906f-119">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f906f-119">-Namespace</span></span>
<span data-ttu-id="f906f-120">Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="f906f-120">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="f906f-121">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="f906f-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="f906f-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="f906f-122">-NotificationHub</span></span>
<span data-ttu-id="f906f-123">Specifica il nome dell'hub di notifica ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f906f-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="f906f-124">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma utilizzata da tali client.</span><span class="sxs-lookup"><span data-stu-id="f906f-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="f906f-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f906f-125">-ResourceGroup</span></span>
<span data-ttu-id="f906f-126">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="f906f-126">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="f906f-127">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f906f-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="f906f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f906f-128">CommonParameters</span></span>
<span data-ttu-id="f906f-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f906f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f906f-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f906f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f906f-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f906f-131">INPUTS</span></span>

### <span data-ttu-id="f906f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f906f-132">System.String</span></span>

## <span data-ttu-id="f906f-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f906f-133">OUTPUTS</span></span>

### <span data-ttu-id="f906f-134">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="f906f-134">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="f906f-135">Note</span><span class="sxs-lookup"><span data-stu-id="f906f-135">NOTES</span></span>

## <span data-ttu-id="f906f-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f906f-136">RELATED LINKS</span></span>

[<span data-ttu-id="f906f-137">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f906f-137">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="f906f-138">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="f906f-138">Get-AzureRmNotificationHubListKeys</span></span>](./Get-AzureRmNotificationHubListKeys.md)

[<span data-ttu-id="f906f-139">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="f906f-139">Get-AzureRmNotificationHubPNSCredentials</span></span>](./Get-AzureRmNotificationHubPNSCredentials.md)

[<span data-ttu-id="f906f-140">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f906f-140">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="f906f-141">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f906f-141">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

[<span data-ttu-id="f906f-142">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f906f-142">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)



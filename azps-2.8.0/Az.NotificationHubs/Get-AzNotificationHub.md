---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: ea16c01e5c528742702dd08f1f2bd4c14e0cebcd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400621"
---
# <span data-ttu-id="00288-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="00288-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="00288-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00288-102">SYNOPSIS</span></span>
<span data-ttu-id="00288-103">Recupera informazioni sugli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="00288-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="00288-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00288-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00288-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="00288-105">DESCRIPTION</span></span>
<span data-ttu-id="00288-106">Il cmdlet **Get-AzNotificationHub** riceve informazioni sugli hub di notifica in uno spazio dei nomi specificato e viene assegnato a un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="00288-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="00288-107">Ad esempio, è possibile ottenere informazioni per tutti gli hub di notifica nello spazio dei nomi ContosoCliente e assegnati al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="00288-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="00288-108">In alternativa, è possibile usare il parametro *NotificationHub* per limitare i dati restituiti alle informazioni su uno specifico hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="00288-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="00288-109">Gli hub di notifica vengono usati per inviare notifiche push a più client, indipendentemente dalla piattaforma usata dai client, ad esempio iOS, Android, Windows Phone 8 e Windows Store.</span><span class="sxs-lookup"><span data-stu-id="00288-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="00288-110">Questi hub sono approssimativamente equivalenti alle singole app e ognuna delle app in genere avrà un proprio hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="00288-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="00288-111">Questo cmdlet ottiene solo informazioni sull'hub stesso.</span><span class="sxs-lookup"><span data-stu-id="00288-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="00288-112">Altri cmdlet, come Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys e Get-AzNotificationHubPNSCredentials, sono necessari per ottenere informazioni sulle regole di autorizzazione, sulle stringhe di connessione e sulle credenziali del servizio di notifica piattaforma di un hub.</span><span class="sxs-lookup"><span data-stu-id="00288-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="00288-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00288-113">EXAMPLES</span></span>

### <span data-ttu-id="00288-114">Esempio 1: Ottenere informazioni per tutti gli hub di notifica in uno spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="00288-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="00288-115">Questo comando recupera le informazioni per tutti gli hub di notifica nello spazio dei nomi denominato Contoso Dello stesso nome che sono stati assegnati al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="00288-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="00288-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00288-116">PARAMETERS</span></span>

### <span data-ttu-id="00288-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00288-117">-DefaultProfile</span></span>
<span data-ttu-id="00288-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="00288-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00288-119">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="00288-119">-Namespace</span></span>
<span data-ttu-id="00288-120">Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="00288-120">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="00288-121">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="00288-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="00288-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="00288-122">-NotificationHub</span></span>
<span data-ttu-id="00288-123">Specifica il nome dell'hub di notifica che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00288-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="00288-124">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma usata da tali client.</span><span class="sxs-lookup"><span data-stu-id="00288-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="00288-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="00288-125">-ResourceGroup</span></span>
<span data-ttu-id="00288-126">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="00288-126">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="00288-127">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che consentono semplicemente la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="00288-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="00288-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00288-128">CommonParameters</span></span>
<span data-ttu-id="00288-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00288-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00288-130">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00288-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00288-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="00288-131">INPUTS</span></span>

### <span data-ttu-id="00288-132">System.String</span><span class="sxs-lookup"><span data-stu-id="00288-132">System.String</span></span>

## <span data-ttu-id="00288-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00288-133">OUTPUTS</span></span>

### <span data-ttu-id="00288-134">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="00288-134">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="00288-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="00288-135">NOTES</span></span>

## <span data-ttu-id="00288-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00288-136">RELATED LINKS</span></span>




[<span data-ttu-id="00288-137">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="00288-137">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="00288-138">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="00288-138">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="00288-139">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="00288-139">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)



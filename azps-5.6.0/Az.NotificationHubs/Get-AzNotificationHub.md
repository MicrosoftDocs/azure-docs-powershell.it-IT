---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: fe2949e5b7eb8c3c5f1261072e755bcbb0b6eb00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951421"
---
# <span data-ttu-id="5a591-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="5a591-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="5a591-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a591-102">SYNOPSIS</span></span>
<span data-ttu-id="5a591-103">Recupera informazioni sugli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5a591-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="5a591-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a591-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a591-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5a591-105">DESCRIPTION</span></span>
<span data-ttu-id="5a591-106">Il cmdlet **Get-AzNotificationHub** riceve informazioni sugli hub di notifica in uno spazio dei nomi specificato e viene assegnato a un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="5a591-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="5a591-107">Ad esempio, è possibile ottenere informazioni per tutti gli hub di notifica nello spazio dei nomi ContosoCliente e assegnati al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="5a591-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="5a591-108">In alternativa, è possibile usare il parametro *NotificationHub* per limitare i dati restituiti alle informazioni su uno specifico hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5a591-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="5a591-109">Gli hub di notifica vengono usati per inviare notifiche push a più client, indipendentemente dalla piattaforma usata dai client, ad esempio iOS, Android, Windows Phone 8 e Windows Store.</span><span class="sxs-lookup"><span data-stu-id="5a591-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="5a591-110">Questi hub sono approssimativamente equivalenti alle singole app e ognuna delle app in genere avrà un proprio hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5a591-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="5a591-111">Questo cmdlet ottiene solo informazioni sull'hub stesso.</span><span class="sxs-lookup"><span data-stu-id="5a591-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="5a591-112">Altri cmdlet, come Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys e Get-AzNotificationHubPNSCredentials, sono necessari per ottenere informazioni sulle regole di autorizzazione, sulle stringhe di connessione e sulle credenziali del servizio di notifica piattaforma di un hub.</span><span class="sxs-lookup"><span data-stu-id="5a591-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="5a591-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a591-113">EXAMPLES</span></span>

### <span data-ttu-id="5a591-114">Esempio 1: Ottenere informazioni per tutti gli hub di notifica in uno spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="5a591-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```powershell
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="5a591-115">Questo comando recupera le informazioni per tutti gli hub di notifica nello spazio dei nomi denominato Contoso Dello stesso nome che sono stati assegnati al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="5a591-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

### <span data-ttu-id="5a591-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5a591-116">Example 2</span></span>

<span data-ttu-id="5a591-117">Recupera informazioni sugli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5a591-117">Gets information about your notification hubs.</span></span> <span data-ttu-id="5a591-118">(autogenerati)</span><span class="sxs-lookup"><span data-stu-id="5a591-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHub 'ContosoInternalHub' -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="5a591-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a591-119">PARAMETERS</span></span>

### <span data-ttu-id="5a591-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a591-120">-DefaultProfile</span></span>
<span data-ttu-id="5a591-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5a591-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a591-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5a591-122">-Namespace</span></span>
<span data-ttu-id="5a591-123">Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5a591-123">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="5a591-124">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5a591-124">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="5a591-125">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="5a591-125">-NotificationHub</span></span>
<span data-ttu-id="5a591-126">Specifica il nome dell'hub di notifica che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a591-126">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="5a591-127">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma usata da tali client.</span><span class="sxs-lookup"><span data-stu-id="5a591-127">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="5a591-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5a591-128">-ResourceGroup</span></span>
<span data-ttu-id="5a591-129">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5a591-129">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="5a591-130">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che consentono semplicemente la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5a591-130">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="5a591-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a591-131">CommonParameters</span></span>
<span data-ttu-id="5a591-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a591-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a591-133">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a591-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a591-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="5a591-134">INPUTS</span></span>

### <span data-ttu-id="5a591-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5a591-135">System.String</span></span>

## <span data-ttu-id="5a591-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a591-136">OUTPUTS</span></span>

### <span data-ttu-id="5a591-137">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="5a591-137">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="5a591-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="5a591-138">NOTES</span></span>

## <span data-ttu-id="5a591-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a591-139">RELATED LINKS</span></span>

[<span data-ttu-id="5a591-140">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5a591-140">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="5a591-141">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="5a591-141">Get-AzNotificationHubListKey</span></span>](./Get-AzNotificationHubListKey.md)

[<span data-ttu-id="5a591-142">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="5a591-142">Get-AzNotificationHubPNSCredential</span></span>](./Get-AzNotificationHubPNSCredential.md)

[<span data-ttu-id="5a591-143">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="5a591-143">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="5a591-144">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="5a591-144">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="5a591-145">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="5a591-145">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)



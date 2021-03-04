---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/remove-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
ms.openlocfilehash: b7932eb4f5d68986033243bc3e5e5161861a0bb8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951150"
---
# <span data-ttu-id="059e0-101">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="059e0-101">Remove-AzNotificationHub</span></span>

## <span data-ttu-id="059e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="059e0-102">SYNOPSIS</span></span>
<span data-ttu-id="059e0-103">Rimuove un hub di notifica esistente.</span><span class="sxs-lookup"><span data-stu-id="059e0-103">Removes an existing notification hub.</span></span>

## <span data-ttu-id="059e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="059e0-104">SYNTAX</span></span>

```
Remove-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="059e0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="059e0-105">DESCRIPTION</span></span>
<span data-ttu-id="059e0-106">Il cmdlet **Remove-AzNotificationHub** rimuove un hub di notifica esistente.</span><span class="sxs-lookup"><span data-stu-id="059e0-106">The **Remove-AzNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="059e0-107">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma usata da tali client.</span><span class="sxs-lookup"><span data-stu-id="059e0-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="059e0-108">Le piattaforme includono, ma non solo: iOS, Android, Windows Phone 8 e Windows Store.</span><span class="sxs-lookup"><span data-stu-id="059e0-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="059e0-109">Gli hub di notifica sono approssimativamente equivalenti alle singole app: ogni app avrà in genere un proprio hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="059e0-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="059e0-110">È possibile rimuovere un hub di notifica esistente usando il cmdlet **Remove-AzNotificationHub.**</span><span class="sxs-lookup"><span data-stu-id="059e0-110">You can remove an existing notification hub by using the **Remove-AzNotificationHub** cmdlet.</span></span>
<span data-ttu-id="059e0-111">Dopo la rimozione di un hub, non è più possibile usarlo per inviare notifiche push agli utenti.</span><span class="sxs-lookup"><span data-stu-id="059e0-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="059e0-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="059e0-112">EXAMPLES</span></span>

### <span data-ttu-id="059e0-113">Esempio 1: Rimuovere un hub di notifica</span><span class="sxs-lookup"><span data-stu-id="059e0-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="059e0-114">Questo comando rimuove l'hub di notifica denominato ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="059e0-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="059e0-115">Per rimuovere l'hub, è necessario specificare lo spazio dei nomi in cui si trova l'hub e il gruppo di risorse a cui è assegnato l'hub.</span><span class="sxs-lookup"><span data-stu-id="059e0-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="059e0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="059e0-116">PARAMETERS</span></span>

### <span data-ttu-id="059e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="059e0-117">-DefaultProfile</span></span>
<span data-ttu-id="059e0-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="059e0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="059e0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="059e0-119">-Force</span></span>
<span data-ttu-id="059e0-120">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="059e0-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="059e0-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="059e0-121">-Namespace</span></span>
<span data-ttu-id="059e0-122">Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="059e0-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="059e0-123">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="059e0-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="059e0-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="059e0-124">-NotificationHub</span></span>
<span data-ttu-id="059e0-125">Specifica l'hub di notifica da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="059e0-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="059e0-126">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma usata da tali client.</span><span class="sxs-lookup"><span data-stu-id="059e0-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="059e0-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="059e0-127">-ResourceGroup</span></span>
<span data-ttu-id="059e0-128">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="059e0-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="059e0-129">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che consentono semplicemente la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="059e0-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="059e0-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="059e0-130">-Confirm</span></span>
<span data-ttu-id="059e0-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="059e0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="059e0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="059e0-132">-WhatIf</span></span>
<span data-ttu-id="059e0-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="059e0-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="059e0-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="059e0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="059e0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="059e0-135">CommonParameters</span></span>
<span data-ttu-id="059e0-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="059e0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="059e0-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="059e0-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="059e0-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="059e0-138">INPUTS</span></span>

### <span data-ttu-id="059e0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="059e0-139">System.String</span></span>

## <span data-ttu-id="059e0-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="059e0-140">OUTPUTS</span></span>

### <span data-ttu-id="059e0-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="059e0-141">System.Void</span></span>

## <span data-ttu-id="059e0-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="059e0-142">NOTES</span></span>

## <span data-ttu-id="059e0-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="059e0-143">RELATED LINKS</span></span>

[<span data-ttu-id="059e0-144">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="059e0-144">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="059e0-145">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="059e0-145">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="059e0-146">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="059e0-146">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)



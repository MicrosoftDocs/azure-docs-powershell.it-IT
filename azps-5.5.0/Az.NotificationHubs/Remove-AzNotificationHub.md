---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
ms.openlocfilehash: 66f3dae7d92b9db18db418bf9de62671f084b7c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179295"
---
# <span data-ttu-id="f5138-101">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f5138-101">Remove-AzNotificationHub</span></span>

## <span data-ttu-id="f5138-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5138-102">SYNOPSIS</span></span>
<span data-ttu-id="f5138-103">Rimuove un hub di notifica esistente.</span><span class="sxs-lookup"><span data-stu-id="f5138-103">Removes an existing notification hub.</span></span>

## <span data-ttu-id="f5138-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f5138-104">SYNTAX</span></span>

```
Remove-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5138-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f5138-105">DESCRIPTION</span></span>
<span data-ttu-id="f5138-106">Il cmdlet **Remove-AzNotificationHub** rimuove un hub di notifica esistente.</span><span class="sxs-lookup"><span data-stu-id="f5138-106">The **Remove-AzNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="f5138-107">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma usata da tali client.</span><span class="sxs-lookup"><span data-stu-id="f5138-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="f5138-108">Le piattaforme includono, ma non solo: iOS, Android, Windows Phone 8 e Windows Store.</span><span class="sxs-lookup"><span data-stu-id="f5138-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="f5138-109">Gli hub di notifica sono approssimativamente equivalenti alle singole app: ogni app avrà in genere un proprio hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="f5138-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="f5138-110">È possibile rimuovere un hub di notifica esistente usando il cmdlet **Remove-AzNotificationHub.**</span><span class="sxs-lookup"><span data-stu-id="f5138-110">You can remove an existing notification hub by using the **Remove-AzNotificationHub** cmdlet.</span></span>
<span data-ttu-id="f5138-111">Dopo la rimozione di un hub, non è più possibile usarlo per inviare notifiche push agli utenti.</span><span class="sxs-lookup"><span data-stu-id="f5138-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="f5138-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f5138-112">EXAMPLES</span></span>

### <span data-ttu-id="f5138-113">Esempio 1: Rimuovere un hub di notifica</span><span class="sxs-lookup"><span data-stu-id="f5138-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="f5138-114">Questo comando rimuove l'hub di notifica denominato ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="f5138-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="f5138-115">Per rimuovere l'hub, è necessario specificare lo spazio dei nomi in cui si trova l'hub e il gruppo di risorse a cui è assegnato l'hub.</span><span class="sxs-lookup"><span data-stu-id="f5138-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="f5138-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5138-116">PARAMETERS</span></span>

### <span data-ttu-id="f5138-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5138-117">-DefaultProfile</span></span>
<span data-ttu-id="f5138-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="f5138-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5138-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f5138-119">-Force</span></span>
<span data-ttu-id="f5138-120">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="f5138-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f5138-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f5138-121">-Namespace</span></span>
<span data-ttu-id="f5138-122">Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="f5138-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="f5138-123">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="f5138-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="f5138-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="f5138-124">-NotificationHub</span></span>
<span data-ttu-id="f5138-125">Specifica l'hub di notifica da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="f5138-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="f5138-126">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma usata da tali client.</span><span class="sxs-lookup"><span data-stu-id="f5138-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="f5138-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f5138-127">-ResourceGroup</span></span>
<span data-ttu-id="f5138-128">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="f5138-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="f5138-129">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che consentono semplicemente la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f5138-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="f5138-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5138-130">-Confirm</span></span>
<span data-ttu-id="f5138-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5138-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5138-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5138-132">-WhatIf</span></span>
<span data-ttu-id="f5138-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f5138-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5138-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f5138-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5138-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5138-135">CommonParameters</span></span>
<span data-ttu-id="f5138-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5138-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5138-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5138-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5138-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="f5138-138">INPUTS</span></span>

### <span data-ttu-id="f5138-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f5138-139">System.String</span></span>

## <span data-ttu-id="f5138-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f5138-140">OUTPUTS</span></span>

### <span data-ttu-id="f5138-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="f5138-141">System.Void</span></span>

## <span data-ttu-id="f5138-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="f5138-142">NOTES</span></span>

## <span data-ttu-id="f5138-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f5138-143">RELATED LINKS</span></span>

[<span data-ttu-id="f5138-144">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f5138-144">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="f5138-145">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f5138-145">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="f5138-146">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f5138-146">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)



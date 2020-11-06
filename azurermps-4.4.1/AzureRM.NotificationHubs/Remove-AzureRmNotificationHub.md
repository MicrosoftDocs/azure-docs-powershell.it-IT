---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
ms.openlocfilehash: b0911045313b26b19fd1de70af926e8c8e066ca8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513164"
---
# <span data-ttu-id="acff1-101">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="acff1-101">Remove-AzureRmNotificationHub</span></span>

## <span data-ttu-id="acff1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="acff1-102">SYNOPSIS</span></span>
<span data-ttu-id="acff1-103">Rimuove un hub di notifica esistente.</span><span class="sxs-lookup"><span data-stu-id="acff1-103">Removes an existing notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acff1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="acff1-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acff1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="acff1-105">DESCRIPTION</span></span>
<span data-ttu-id="acff1-106">Il cmdlet **Remove-AzureRmNotificationHub** rimuove un hub di notifica esistente.</span><span class="sxs-lookup"><span data-stu-id="acff1-106">The **Remove-AzureRmNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="acff1-107">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma utilizzata da tali client.</span><span class="sxs-lookup"><span data-stu-id="acff1-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="acff1-108">Le piattaforme includono, ma non sono limitate a: iOS, Android, Windows Phone 8 e Windows Store.</span><span class="sxs-lookup"><span data-stu-id="acff1-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="acff1-109">Gli hub di notifica equivalgono approssimativamente alle singole app: ognuna delle tue app avrà in genere un hub di notifica personalizzato.</span><span class="sxs-lookup"><span data-stu-id="acff1-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="acff1-110">Puoi rimuovere un hub di notifica esistente usando il cmdlet **Remove-AzureRmNotificationHub** .</span><span class="sxs-lookup"><span data-stu-id="acff1-110">You can remove an existing notification hub by using the **Remove-AzureRmNotificationHub** cmdlet.</span></span>
<span data-ttu-id="acff1-111">Dopo aver rimosso un hub, non è più possibile usare tale hub per inviare notifiche push agli utenti.</span><span class="sxs-lookup"><span data-stu-id="acff1-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="acff1-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="acff1-112">EXAMPLES</span></span>

### <span data-ttu-id="acff1-113">Esempio 1: rimuovere un hub di notifica</span><span class="sxs-lookup"><span data-stu-id="acff1-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="acff1-114">Questo comando rimuove l'hub di notifica denominato ContosoInternalHub.</span><span class="sxs-lookup"><span data-stu-id="acff1-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="acff1-115">Per rimuovere l'hub, devi specificare lo spazio dei nomi in cui si trova l'hub e il gruppo di risorse a cui è assegnato l'hub.</span><span class="sxs-lookup"><span data-stu-id="acff1-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="acff1-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="acff1-116">PARAMETERS</span></span>

### <span data-ttu-id="acff1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="acff1-117">-Force</span></span>
<span data-ttu-id="acff1-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="acff1-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="acff1-119">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="acff1-119">-Namespace</span></span>
<span data-ttu-id="acff1-120">Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="acff1-120">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="acff1-121">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="acff1-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="acff1-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="acff1-122">-NotificationHub</span></span>
<span data-ttu-id="acff1-123">Specifica l'hub di notifica da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="acff1-123">Specifies the notification hub to be removed.</span></span>

<span data-ttu-id="acff1-124">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma utilizzata da tali client.</span><span class="sxs-lookup"><span data-stu-id="acff1-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="acff1-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="acff1-125">-ResourceGroup</span></span>
<span data-ttu-id="acff1-126">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="acff1-126">Specifies the resource group to which the notification hub is assigned.</span></span>

<span data-ttu-id="acff1-127">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="acff1-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="acff1-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="acff1-128">-Confirm</span></span>
<span data-ttu-id="acff1-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acff1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acff1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acff1-130">-WhatIf</span></span>
<span data-ttu-id="acff1-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="acff1-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="acff1-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="acff1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acff1-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acff1-133">-DefaultProfile</span></span>
<span data-ttu-id="acff1-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="acff1-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acff1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acff1-135">CommonParameters</span></span>
<span data-ttu-id="acff1-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acff1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acff1-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acff1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acff1-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="acff1-138">INPUTS</span></span>

## <span data-ttu-id="acff1-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="acff1-139">OUTPUTS</span></span>

## <span data-ttu-id="acff1-140">Note</span><span class="sxs-lookup"><span data-stu-id="acff1-140">NOTES</span></span>

## <span data-ttu-id="acff1-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="acff1-141">RELATED LINKS</span></span>

[<span data-ttu-id="acff1-142">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="acff1-142">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="acff1-143">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="acff1-143">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="acff1-144">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="acff1-144">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)



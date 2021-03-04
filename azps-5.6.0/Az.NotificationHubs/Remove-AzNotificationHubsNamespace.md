---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
ms.openlocfilehash: a1e5a8b33ab9df4e48495d00b6a27e105088f4fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951134"
---
# <span data-ttu-id="6351e-101">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="6351e-101">Remove-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="6351e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6351e-102">SYNOPSIS</span></span>
<span data-ttu-id="6351e-103">Rimuove uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="6351e-103">Removes a notification hub namespace.</span></span>

## <span data-ttu-id="6351e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6351e-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6351e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6351e-105">DESCRIPTION</span></span>
<span data-ttu-id="6351e-106">Il cmdlet **Remove-AzNotificationHubs Unificato rimuove** uno spazio dei nomi dell'hub di notifica dalla distribuzione.</span><span class="sxs-lookup"><span data-stu-id="6351e-106">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="6351e-107">Gli spazi dei nomi sono contenitori logici che consentono di organizzare e gestire gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="6351e-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="6351e-108">Il cmdlet **Remove-AzNotificationHubs Unificato rimuove** uno spazio dei nomi dell'hub di notifica dalla distribuzione.</span><span class="sxs-lookup"><span data-stu-id="6351e-108">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="6351e-109">Quando si esegue questo cmdlet, lo spazio dei nomi specificato viene eliminato insieme a tutti gli hub di notifica associati a tale spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6351e-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="6351e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6351e-110">EXAMPLES</span></span>

### <span data-ttu-id="6351e-111">Esempio 1: Rimuovere uno spazio dei nomi dell'hub di notifica</span><span class="sxs-lookup"><span data-stu-id="6351e-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="6351e-112">Questo comando rimuove lo spazio dei nomi denominato ContosoNtassi.</span><span class="sxs-lookup"><span data-stu-id="6351e-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="6351e-113">È necessario specificare il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6351e-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="6351e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6351e-114">PARAMETERS</span></span>

### <span data-ttu-id="6351e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6351e-115">-DefaultProfile</span></span>
<span data-ttu-id="6351e-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6351e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6351e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6351e-117">-Force</span></span>
<span data-ttu-id="6351e-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="6351e-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6351e-119">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6351e-119">-Namespace</span></span>
<span data-ttu-id="6351e-120">Specifica lo spazio dei nomi rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6351e-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="6351e-121">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="6351e-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="6351e-122">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6351e-122">-ResourceGroup</span></span>
<span data-ttu-id="6351e-123">Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6351e-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="6351e-124">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che consentono semplicemente la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6351e-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="6351e-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6351e-125">-Confirm</span></span>
<span data-ttu-id="6351e-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6351e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6351e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6351e-127">-WhatIf</span></span>
<span data-ttu-id="6351e-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6351e-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6351e-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6351e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6351e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6351e-130">CommonParameters</span></span>
<span data-ttu-id="6351e-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6351e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6351e-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6351e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6351e-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="6351e-133">INPUTS</span></span>

### <span data-ttu-id="6351e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="6351e-134">System.String</span></span>

## <span data-ttu-id="6351e-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6351e-135">OUTPUTS</span></span>

### <span data-ttu-id="6351e-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="6351e-136">System.Void</span></span>

## <span data-ttu-id="6351e-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="6351e-137">NOTES</span></span>

## <span data-ttu-id="6351e-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6351e-138">RELATED LINKS</span></span>

[<span data-ttu-id="6351e-139">Get-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="6351e-139">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="6351e-140">New-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="6351e-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="6351e-141">Set-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="6351e-141">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)



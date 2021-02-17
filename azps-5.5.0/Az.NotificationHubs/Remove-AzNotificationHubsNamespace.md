---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
ms.openlocfilehash: e03be5a1daae753e1538b171586d9a8e46ad8021
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191518"
---
# <span data-ttu-id="a2754-101">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="a2754-101">Remove-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="a2754-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2754-102">SYNOPSIS</span></span>
<span data-ttu-id="a2754-103">Rimuove uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="a2754-103">Removes a notification hub namespace.</span></span>

## <span data-ttu-id="a2754-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2754-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2754-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a2754-105">DESCRIPTION</span></span>
<span data-ttu-id="a2754-106">Il cmdlet **Remove-AzNotificationHubs Unificato rimuove** uno spazio dei nomi dell'hub di notifica dalla distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a2754-106">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="a2754-107">Gli spazi dei nomi sono contenitori logici che consentono di organizzare e gestire gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="a2754-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="a2754-108">Il cmdlet **Remove-AzNotificationHubs Unificato rimuove** uno spazio dei nomi dell'hub di notifica dalla distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a2754-108">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="a2754-109">Quando si esegue questo cmdlet, lo spazio dei nomi specificato viene eliminato insieme a tutti gli hub di notifica associati a tale spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a2754-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="a2754-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2754-110">EXAMPLES</span></span>

### <span data-ttu-id="a2754-111">Esempio 1: Rimuovere uno spazio dei nomi dell'hub di notifica</span><span class="sxs-lookup"><span data-stu-id="a2754-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="a2754-112">Questo comando rimuove lo spazio dei nomi denominato ContosoNtassi.</span><span class="sxs-lookup"><span data-stu-id="a2754-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="a2754-113">È necessario specificare il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a2754-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="a2754-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2754-114">PARAMETERS</span></span>

### <span data-ttu-id="a2754-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2754-115">-DefaultProfile</span></span>
<span data-ttu-id="a2754-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="a2754-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2754-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a2754-117">-Force</span></span>
<span data-ttu-id="a2754-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="a2754-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a2754-119">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a2754-119">-Namespace</span></span>
<span data-ttu-id="a2754-120">Specifica lo spazio dei nomi rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2754-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="a2754-121">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="a2754-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="a2754-122">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a2754-122">-ResourceGroup</span></span>
<span data-ttu-id="a2754-123">Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a2754-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="a2754-124">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che consentono semplicemente la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a2754-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="a2754-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2754-125">-Confirm</span></span>
<span data-ttu-id="a2754-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2754-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2754-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2754-127">-WhatIf</span></span>
<span data-ttu-id="a2754-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2754-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2754-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2754-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2754-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2754-130">CommonParameters</span></span>
<span data-ttu-id="a2754-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2754-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2754-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2754-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2754-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="a2754-133">INPUTS</span></span>

### <span data-ttu-id="a2754-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a2754-134">System.String</span></span>

## <span data-ttu-id="a2754-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2754-135">OUTPUTS</span></span>

### <span data-ttu-id="a2754-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="a2754-136">System.Void</span></span>

## <span data-ttu-id="a2754-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="a2754-137">NOTES</span></span>

## <span data-ttu-id="a2754-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2754-138">RELATED LINKS</span></span>

[<span data-ttu-id="a2754-139">Get-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="a2754-139">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="a2754-140">New-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="a2754-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="a2754-141">Set-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="a2754-141">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)



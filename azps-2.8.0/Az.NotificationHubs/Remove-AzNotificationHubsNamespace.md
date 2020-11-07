---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
ms.openlocfilehash: 3b239e1d459ca8c942c896123521ec6b09e8f7b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855553"
---
# <span data-ttu-id="a03e4-101">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="a03e4-101">Remove-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="a03e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a03e4-102">SYNOPSIS</span></span>
<span data-ttu-id="a03e4-103">Rimuove uno spazio dei nomi Hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="a03e4-103">Removes a notification hub namespace.</span></span>

## <span data-ttu-id="a03e4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a03e4-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a03e4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a03e4-105">DESCRIPTION</span></span>
<span data-ttu-id="a03e4-106">Il cmdlet **Remove-AzNotificationHubsNamespace** rimuove uno spazio dei nomi dell'hub di notifica dalla distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a03e4-106">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="a03e4-107">Gli spazi dei nomi sono contenitori logici che consentono di organizzare e gestire gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="a03e4-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="a03e4-108">Il cmdlet **Remove-AzNotificationHubsNamespace** rimuove uno spazio dei nomi dell'hub di notifica dalla distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a03e4-108">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="a03e4-109">Quando si esegue questo cmdlet, lo spazio dei nomi specificato verrà eliminato insieme a tutti gli hub di notifica associati a tale spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a03e4-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="a03e4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a03e4-110">EXAMPLES</span></span>

### <span data-ttu-id="a03e4-111">Esempio 1: rimuovere uno spazio dei nomi dell'hub di notifica</span><span class="sxs-lookup"><span data-stu-id="a03e4-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="a03e4-112">Questo comando rimuove lo spazio dei nomi denominato ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="a03e4-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="a03e4-113">Devi specificare il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a03e4-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="a03e4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a03e4-114">PARAMETERS</span></span>

### <span data-ttu-id="a03e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a03e4-115">-DefaultProfile</span></span>
<span data-ttu-id="a03e4-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a03e4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a03e4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a03e4-117">-Force</span></span>
<span data-ttu-id="a03e4-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="a03e4-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a03e4-119">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a03e4-119">-Namespace</span></span>
<span data-ttu-id="a03e4-120">Specifica lo spazio dei nomi rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a03e4-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="a03e4-121">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="a03e4-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="a03e4-122">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a03e4-122">-ResourceGroup</span></span>
<span data-ttu-id="a03e4-123">Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="a03e4-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="a03e4-124">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a03e4-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="a03e4-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a03e4-125">-Confirm</span></span>
<span data-ttu-id="a03e4-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a03e4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a03e4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a03e4-127">-WhatIf</span></span>
<span data-ttu-id="a03e4-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a03e4-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a03e4-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a03e4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a03e4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a03e4-130">CommonParameters</span></span>
<span data-ttu-id="a03e4-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a03e4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a03e4-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a03e4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a03e4-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a03e4-133">INPUTS</span></span>

### <span data-ttu-id="a03e4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a03e4-134">System.String</span></span>

## <span data-ttu-id="a03e4-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a03e4-135">OUTPUTS</span></span>

### <span data-ttu-id="a03e4-136">System. void</span><span class="sxs-lookup"><span data-stu-id="a03e4-136">System.Void</span></span>

## <span data-ttu-id="a03e4-137">Note</span><span class="sxs-lookup"><span data-stu-id="a03e4-137">NOTES</span></span>

## <span data-ttu-id="a03e4-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a03e4-138">RELATED LINKS</span></span>

[<span data-ttu-id="a03e4-139">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="a03e4-139">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="a03e4-140">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="a03e4-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="a03e4-141">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="a03e4-141">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)



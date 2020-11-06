---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: c574fd511bbdcb4c134a2cc99656ebb82614a12c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514979"
---
# <span data-ttu-id="9e840-101">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="9e840-101">Remove-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="9e840-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e840-102">SYNOPSIS</span></span>
<span data-ttu-id="9e840-103">Rimuove uno spazio dei nomi Hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="9e840-103">Removes a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e840-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e840-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e840-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e840-105">DESCRIPTION</span></span>
<span data-ttu-id="9e840-106">Il cmdlet **Remove-AzureRmNotificationHubsNamespace** rimuove uno spazio dei nomi dell'hub di notifica dalla distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9e840-106">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="9e840-107">Gli spazi dei nomi sono contenitori logici che consentono di organizzare e gestire gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="9e840-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="9e840-108">Il cmdlet **Remove-AzureRmNotificationHubsNamespace** rimuove uno spazio dei nomi dell'hub di notifica dalla distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9e840-108">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="9e840-109">Quando si esegue questo cmdlet, lo spazio dei nomi specificato verrà eliminato insieme a tutti gli hub di notifica associati a tale spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="9e840-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="9e840-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e840-110">EXAMPLES</span></span>

### <span data-ttu-id="9e840-111">Esempio 1: rimuovere uno spazio dei nomi dell'hub di notifica</span><span class="sxs-lookup"><span data-stu-id="9e840-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="9e840-112">Questo comando rimuove lo spazio dei nomi denominato ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="9e840-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="9e840-113">Devi specificare il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="9e840-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="9e840-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e840-114">PARAMETERS</span></span>

### <span data-ttu-id="9e840-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e840-115">-DefaultProfile</span></span>
<span data-ttu-id="9e840-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9e840-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e840-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9e840-117">-Force</span></span>
<span data-ttu-id="9e840-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="9e840-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9e840-119">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9e840-119">-Namespace</span></span>
<span data-ttu-id="9e840-120">Specifica lo spazio dei nomi rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e840-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="9e840-121">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="9e840-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="9e840-122">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9e840-122">-ResourceGroup</span></span>
<span data-ttu-id="9e840-123">Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="9e840-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="9e840-124">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9e840-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="9e840-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9e840-125">-Confirm</span></span>
<span data-ttu-id="9e840-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e840-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e840-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e840-127">-WhatIf</span></span>
<span data-ttu-id="9e840-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e840-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e840-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e840-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e840-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e840-130">CommonParameters</span></span>
<span data-ttu-id="9e840-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e840-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e840-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e840-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e840-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e840-133">INPUTS</span></span>

### <span data-ttu-id="9e840-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9e840-134">System.String</span></span>

## <span data-ttu-id="9e840-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e840-135">OUTPUTS</span></span>

### <span data-ttu-id="9e840-136">System. void</span><span class="sxs-lookup"><span data-stu-id="9e840-136">System.Void</span></span>

## <span data-ttu-id="9e840-137">Note</span><span class="sxs-lookup"><span data-stu-id="9e840-137">NOTES</span></span>

## <span data-ttu-id="9e840-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e840-138">RELATED LINKS</span></span>

[<span data-ttu-id="9e840-139">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="9e840-139">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="9e840-140">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="9e840-140">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="9e840-141">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="9e840-141">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)



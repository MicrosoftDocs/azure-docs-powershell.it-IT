---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 3d0e604d3984a40acde02fb1f977e2922ae2d1d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206435"
---
# <span data-ttu-id="5ef62-101">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="5ef62-101">Get-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="5ef62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ef62-102">SYNOPSIS</span></span>
<span data-ttu-id="5ef62-103">Ottiene informazioni sullo spazio dei nomi di un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5ef62-103">Gets information about a notification hub namespace.</span></span>

## <span data-ttu-id="5ef62-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ef62-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ef62-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5ef62-105">DESCRIPTION</span></span>
<span data-ttu-id="5ef62-106">Il cmdlet **Get-AzNotificationHubsHubsBlock ottiene** informazioni sugli spazi dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5ef62-106">**The Get-AzNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="5ef62-107">Questo cmdlet consente di ottenere informazioni per tutti gli spazi dei nomi, informazioni sugli spazi dei nomi assegnati a un gruppo di risorse specificato; o per restituire informazioni su uno spazio dei nomi specifico.</span><span class="sxs-lookup"><span data-stu-id="5ef62-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>
<span data-ttu-id="5ef62-108">Gli spazi dei nomi sono contenitori logici che consentono di organizzare e gestire gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5ef62-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="5ef62-109">È necessario avere almeno uno spazio dei nomi dell'hub di notifica: tutti gli hub di notifica devono essere assegnati a uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="5ef62-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="5ef62-110">Un singolo spazio dei nomi può ospitare più hub, quindi potrebbe essere necessario un solo spazio dei nomi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="5ef62-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="5ef62-111">Tuttavia, è anche possibile avere più spazi dei nomi per organizzare meglio gli hub o per assegnare a utenti specifici l'autorizzazione per gestire un sottoinsieme selezionato di hub.</span><span class="sxs-lookup"><span data-stu-id="5ef62-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>
<span data-ttu-id="5ef62-112">Il cmdlet **Get-AzNotificationHubsHub restituisce** informazioni di base sullo spazio dei nomi stesso.</span><span class="sxs-lookup"><span data-stu-id="5ef62-112">The **Get-AzNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="5ef62-113">Per ottenere informazioni sulle regole di autorizzazione associate a uno spazio dei nomi, usare Get-AzNotificationHubsAuthorizationRules.</span><span class="sxs-lookup"><span data-stu-id="5ef62-113">To get information about the authorization rules associated with a namespace use Get-AzNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="5ef62-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ef62-114">EXAMPLES</span></span>

### <span data-ttu-id="5ef62-115">Esempio 1: Ottenere informazioni per tutti gli spazi dei nomi dell'hub di notifica</span><span class="sxs-lookup"><span data-stu-id="5ef62-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace
```

<span data-ttu-id="5ef62-116">Questo comando restituisce informazioni per tutti gli spazi dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5ef62-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="5ef62-117">Esempio 2: Ottenere informazioni per lo spazio dei nomi di un singolo hub di notifica</span><span class="sxs-lookup"><span data-stu-id="5ef62-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="5ef62-118">Questo comando recupera le informazioni per un singolo spazio dei nomi dell'hub di notifica: Contoso Contoso Contoso.</span><span class="sxs-lookup"><span data-stu-id="5ef62-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="5ef62-119">Esempio 3: Ottenere informazioni per tutti gli hub di notifica assegnati a uno spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="5ef62-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="5ef62-120">Questo comando recupera le informazioni per tutti gli spazi dei nomi dell'hub di notifica assegnati al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="5ef62-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="5ef62-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ef62-121">PARAMETERS</span></span>

### <span data-ttu-id="5ef62-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ef62-122">-DefaultProfile</span></span>
<span data-ttu-id="5ef62-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="5ef62-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ef62-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5ef62-124">-Namespace</span></span>
<span data-ttu-id="5ef62-125">Specifica un nome univoco per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="5ef62-125">Specifies a unique name for the namespace.</span></span>
<span data-ttu-id="5ef62-126">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5ef62-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ef62-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5ef62-127">-ResourceGroup</span></span>
<span data-ttu-id="5ef62-128">Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="5ef62-128">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="5ef62-129">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che consentono semplicemente la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5ef62-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ef62-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ef62-130">CommonParameters</span></span>
<span data-ttu-id="5ef62-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ef62-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ef62-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ef62-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ef62-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="5ef62-133">INPUTS</span></span>

### <span data-ttu-id="5ef62-134">System.String</span><span class="sxs-lookup"><span data-stu-id="5ef62-134">System.String</span></span>

## <span data-ttu-id="5ef62-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ef62-135">OUTPUTS</span></span>

### <span data-ttu-id="5ef62-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="5ef62-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="5ef62-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="5ef62-137">NOTES</span></span>

## <span data-ttu-id="5ef62-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ef62-138">RELATED LINKS</span></span>

[<span data-ttu-id="5ef62-139">Get-AzNotificationHubsAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5ef62-139">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="5ef62-140">New-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="5ef62-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="5ef62-141">Remove-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="5ef62-141">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="5ef62-142">Set-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="5ef62-142">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)



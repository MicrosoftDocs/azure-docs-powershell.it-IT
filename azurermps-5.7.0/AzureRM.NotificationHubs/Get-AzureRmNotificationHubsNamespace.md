---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 996904a68e8cb55aa4964a6c776064722c63dbab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515519"
---
# <span data-ttu-id="003af-101">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="003af-101">Get-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="003af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="003af-102">SYNOPSIS</span></span>
<span data-ttu-id="003af-103">Ottiene informazioni su uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="003af-103">Gets information about a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="003af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="003af-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="003af-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="003af-105">DESCRIPTION</span></span>
<span data-ttu-id="003af-106">**Il cmdlet Get-AzureRmNotificationHubsNamespace** ottiene le informazioni sugli spazi dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="003af-106">**The Get-AzureRmNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="003af-107">Questo cmdlet offre la possibilità di ottenere informazioni per tutti gli spazi dei nomi, informazioni sugli spazi dei nomi assegnati a un gruppo di risorse specificato. o per restituire informazioni su uno spazio dei nomi specifico.</span><span class="sxs-lookup"><span data-stu-id="003af-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>

<span data-ttu-id="003af-108">Gli spazi dei nomi sono contenitori logici che consentono di organizzare e gestire gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="003af-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="003af-109">È necessario avere almeno uno spazio dei nomi dell'hub di notifica: tutti gli hub di notifica devono essere assegnati a uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="003af-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="003af-110">Un singolo spazio dei nomi può ospitare più hub, quindi potrebbe essere necessario uno spazio dei nomi nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="003af-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="003af-111">Tuttavia, puoi anche avere più spazi dei nomi per organizzare meglio i tuoi Hub o per dare agli utenti specifici l'autorizzazione per gestire un subset selezionato di hub.</span><span class="sxs-lookup"><span data-stu-id="003af-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>

<span data-ttu-id="003af-112">Il cmdlet **Get-AzureRmNotificationHubsNamespace** restituisce le informazioni di base sullo spazio dei nomi stesso.</span><span class="sxs-lookup"><span data-stu-id="003af-112">The **Get-AzureRmNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="003af-113">Per ottenere informazioni sulle regole di autorizzazione associate a uno spazio dei nomi, utilizzare Get-AzureRmNotificationHubsNamespaceAuthorizationRules.</span><span class="sxs-lookup"><span data-stu-id="003af-113">To get information about the authorization rules associated with a namespace use Get-AzureRmNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="003af-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="003af-114">EXAMPLES</span></span>

### <span data-ttu-id="003af-115">Esempio 1: ottenere informazioni per tutti gli spazi dei nomi dell'hub di notifica</span><span class="sxs-lookup"><span data-stu-id="003af-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace
```

<span data-ttu-id="003af-116">Questo comando restituisce informazioni per tutti gli spazi dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="003af-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="003af-117">Esempio 2: ottenere informazioni per un singolo spazio dei nomi dell'hub di notifica</span><span class="sxs-lookup"><span data-stu-id="003af-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="003af-118">Questo comando ottiene le informazioni per un singolo spazio dei nomi dell'hub di notifica: ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="003af-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="003af-119">Esempio 3: ottenere informazioni per tutti gli hub di notifica assegnati a uno spazio dei nomi specifico</span><span class="sxs-lookup"><span data-stu-id="003af-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="003af-120">Questo comando ottiene le informazioni per tutti gli spazi dei nomi dell'hub di notifica assegnati al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="003af-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="003af-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="003af-121">PARAMETERS</span></span>

### <span data-ttu-id="003af-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="003af-122">-DefaultProfile</span></span>
<span data-ttu-id="003af-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="003af-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="003af-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="003af-124">-Namespace</span></span>
<span data-ttu-id="003af-125">Specifica un nome univoco per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="003af-125">Specifies a unique name for the namespace.</span></span>

<span data-ttu-id="003af-126">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="003af-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003af-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="003af-127">-ResourceGroup</span></span>
<span data-ttu-id="003af-128">Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="003af-128">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="003af-129">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="003af-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003af-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="003af-130">CommonParameters</span></span>
<span data-ttu-id="003af-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="003af-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="003af-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="003af-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="003af-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="003af-133">INPUTS</span></span>

### <span data-ttu-id="003af-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="003af-134">None</span></span>
<span data-ttu-id="003af-135">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="003af-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="003af-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="003af-136">OUTPUTS</span></span>

### <span data-ttu-id="003af-137">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceAttributes]</span><span class="sxs-lookup"><span data-stu-id="003af-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes]</span></span>

## <span data-ttu-id="003af-138">Note</span><span class="sxs-lookup"><span data-stu-id="003af-138">NOTES</span></span>

## <span data-ttu-id="003af-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="003af-139">RELATED LINKS</span></span>

[<span data-ttu-id="003af-140">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="003af-140">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="003af-141">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="003af-141">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="003af-142">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="003af-142">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="003af-143">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="003af-143">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)



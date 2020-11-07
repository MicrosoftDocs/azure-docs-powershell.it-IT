---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: e9b699e8839f2ba9426945ef0de883c4bfac40d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687140"
---
# <span data-ttu-id="9abca-101">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9abca-101">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="9abca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9abca-102">SYNOPSIS</span></span>
<span data-ttu-id="9abca-103">Rimuove una regola di autorizzazione da uno spazio dei nomi Hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="9abca-103">Removes an authorization rule from a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9abca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9abca-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9abca-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9abca-105">DESCRIPTION</span></span>
<span data-ttu-id="9abca-106">Il cmdlet **Remove-AzureRmNotificationHubsNamespaceAuthorizationRules** rimuove una regola di autorizzazione della firma di accesso condiviso (SAS) da uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="9abca-106">The **Remove-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>

<span data-ttu-id="9abca-107">Le regole di autorizzazione gestiscono l'accesso a uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="9abca-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="9abca-108">Questa operazione viene eseguita tramite la creazione di collegamenti, come URI, in base a livelli di autorizzazione diversi.</span><span class="sxs-lookup"><span data-stu-id="9abca-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="9abca-109">I livelli di autorizzazione possono essere i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9abca-109">Permission levels can be of the following:</span></span> 

- <span data-ttu-id="9abca-110">Ascoltare</span><span class="sxs-lookup"><span data-stu-id="9abca-110">Listen</span></span>
- <span data-ttu-id="9abca-111">Invia</span><span class="sxs-lookup"><span data-stu-id="9abca-111">Send</span></span>
- <span data-ttu-id="9abca-112">Gestire</span><span class="sxs-lookup"><span data-stu-id="9abca-112">Manage</span></span>

<span data-ttu-id="9abca-113">I client vengono indirizzati a uno di questi URI in base al livello di autorizzazione appropriato.</span><span class="sxs-lookup"><span data-stu-id="9abca-113">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="9abca-114">Ad esempio, un client assegnato l'autorizzazione listen viene indirizzato all'URI per l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="9abca-114">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>

<span data-ttu-id="9abca-115">La rimozione di una regola di autorizzazione consente inoltre di rimuovere l'autorizzazione utente corrispondente.</span><span class="sxs-lookup"><span data-stu-id="9abca-115">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="9abca-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9abca-116">EXAMPLES</span></span>

### <span data-ttu-id="9abca-117">Esempio 1: rimuovere una regola di autorizzazione da uno spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9abca-117">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="9abca-118">Questo comando rimuove la regola di autorizzazione denominata ListenRule dallo spazio dei nomi denominato ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="9abca-118">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="9abca-119">Quando si esegue questo comando, è necessario specificare il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="9abca-119">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="9abca-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9abca-120">PARAMETERS</span></span>

### <span data-ttu-id="9abca-121">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9abca-121">-AuthorizationRule</span></span>
<span data-ttu-id="9abca-122">Specifica il nome della regola di autenticazione SAS da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="9abca-122">Specifies the name of the SAS authentication rule to be removed.</span></span>

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

### <span data-ttu-id="9abca-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9abca-123">-Force</span></span>
<span data-ttu-id="9abca-124">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="9abca-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9abca-125">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9abca-125">-Namespace</span></span>
<span data-ttu-id="9abca-126">Specifica lo spazio dei nomi a cui vengono assegnate le regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="9abca-126">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="9abca-127">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="9abca-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="9abca-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9abca-128">-ResourceGroup</span></span>
<span data-ttu-id="9abca-129">Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="9abca-129">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="9abca-130">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9abca-130">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="9abca-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9abca-131">-Confirm</span></span>
<span data-ttu-id="9abca-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9abca-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9abca-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9abca-133">-WhatIf</span></span>
<span data-ttu-id="9abca-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9abca-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9abca-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9abca-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9abca-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9abca-136">-DefaultProfile</span></span>
<span data-ttu-id="9abca-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9abca-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9abca-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9abca-138">CommonParameters</span></span>
<span data-ttu-id="9abca-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9abca-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9abca-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9abca-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9abca-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9abca-141">INPUTS</span></span>

## <span data-ttu-id="9abca-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9abca-142">OUTPUTS</span></span>

### <span data-ttu-id="9abca-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9abca-143">System.Boolean</span></span>

## <span data-ttu-id="9abca-144">Note</span><span class="sxs-lookup"><span data-stu-id="9abca-144">NOTES</span></span>

## <span data-ttu-id="9abca-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9abca-145">RELATED LINKS</span></span>

[<span data-ttu-id="9abca-146">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9abca-146">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="9abca-147">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9abca-147">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="9abca-148">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9abca-148">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md)



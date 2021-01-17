---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: a25535e3aef21894091197d816c61f2aa5131df9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385080"
---
# <span data-ttu-id="b7792-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b7792-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="b7792-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7792-102">SYNOPSIS</span></span>
<span data-ttu-id="b7792-103">Rimuove una regola di autorizzazione da uno spazio dei nomi Hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="b7792-103">Removes an authorization rule from a notification hub namespace.</span></span>

## <span data-ttu-id="b7792-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7792-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7792-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7792-105">DESCRIPTION</span></span>
<span data-ttu-id="b7792-106">Il cmdlet **Remove-AzNotificationHubsNamespaceAuthorizationRule** rimuove una regola di autorizzazione della firma di accesso condiviso (SAS) da uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="b7792-106">The **Remove-AzNotificationHubsNamespaceAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>
<span data-ttu-id="b7792-107">Le regole di autorizzazione gestiscono l'accesso a uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="b7792-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="b7792-108">Questa operazione viene eseguita tramite la creazione di collegamenti, come URI, in base a livelli di autorizzazione diversi.</span><span class="sxs-lookup"><span data-stu-id="b7792-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="b7792-109">I livelli di autorizzazione possono essere i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b7792-109">Permission levels can be of the following:</span></span> 
- <span data-ttu-id="b7792-110">Ascoltare</span><span class="sxs-lookup"><span data-stu-id="b7792-110">Listen</span></span>
- <span data-ttu-id="b7792-111">Invia</span><span class="sxs-lookup"><span data-stu-id="b7792-111">Send</span></span>
- <span data-ttu-id="b7792-112">I client di gestione vengono indirizzati a uno di questi URI in base al livello di autorizzazione appropriato.</span><span class="sxs-lookup"><span data-stu-id="b7792-112">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="b7792-113">Ad esempio, un client assegnato l'autorizzazione listen viene indirizzato all'URI per l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="b7792-113">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>
<span data-ttu-id="b7792-114">La rimozione di una regola di autorizzazione consente inoltre di rimuovere l'autorizzazione utente corrispondente.</span><span class="sxs-lookup"><span data-stu-id="b7792-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="b7792-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7792-115">EXAMPLES</span></span>

### <span data-ttu-id="b7792-116">Esempio 1: rimuovere una regola di autorizzazione da uno spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b7792-116">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzNotificationHubNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="b7792-117">Questo comando rimuove la regola di autorizzazione denominata ListenRule dallo spazio dei nomi denominato ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="b7792-117">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="b7792-118">Quando si esegue questo comando, è necessario specificare il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="b7792-118">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="b7792-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7792-119">PARAMETERS</span></span>

### <span data-ttu-id="b7792-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b7792-120">-AuthorizationRule</span></span>
<span data-ttu-id="b7792-121">Specifica il nome della regola di autenticazione SAS da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b7792-121">Specifies the name of the SAS authentication rule to be removed.</span></span>

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

### <span data-ttu-id="b7792-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7792-122">-DefaultProfile</span></span>
<span data-ttu-id="b7792-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b7792-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7792-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b7792-124">-Force</span></span>
<span data-ttu-id="b7792-125">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="b7792-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b7792-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b7792-126">-Namespace</span></span>
<span data-ttu-id="b7792-127">Specifica lo spazio dei nomi a cui vengono assegnate le regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="b7792-127">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="b7792-128">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="b7792-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="b7792-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b7792-129">-ResourceGroup</span></span>
<span data-ttu-id="b7792-130">Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="b7792-130">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="b7792-131">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b7792-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="b7792-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b7792-132">-Confirm</span></span>
<span data-ttu-id="b7792-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7792-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7792-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7792-134">-WhatIf</span></span>
<span data-ttu-id="b7792-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7792-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7792-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7792-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7792-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7792-137">CommonParameters</span></span>
<span data-ttu-id="b7792-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7792-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7792-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7792-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7792-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7792-140">INPUTS</span></span>

### <span data-ttu-id="b7792-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b7792-141">System.String</span></span>

## <span data-ttu-id="b7792-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7792-142">OUTPUTS</span></span>

### <span data-ttu-id="b7792-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b7792-143">System.Boolean</span></span>

## <span data-ttu-id="b7792-144">Note</span><span class="sxs-lookup"><span data-stu-id="b7792-144">NOTES</span></span>

## <span data-ttu-id="b7792-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7792-145">RELATED LINKS</span></span>

[<span data-ttu-id="b7792-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b7792-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="b7792-147">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b7792-147">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="b7792-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b7792-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Set-AzNotificationHubsNamespaceAuthorizationRule.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 0b16a7feb2d0cba7355b6064c1a0e1e6fb327066
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951133"
---
# <span data-ttu-id="45ca5-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="45ca5-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="45ca5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45ca5-102">SYNOPSIS</span></span>
<span data-ttu-id="45ca5-103">Rimuove una regola di autorizzazione da uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="45ca5-103">Removes an authorization rule from a notification hub namespace.</span></span>

## <span data-ttu-id="45ca5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45ca5-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45ca5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="45ca5-105">DESCRIPTION</span></span>
<span data-ttu-id="45ca5-106">Il cmdlet **Remove-AzNotificationHubsAuthorizationRule** rimuove una regola di autorizzazione della firma di accesso condiviso da uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="45ca5-106">The **Remove-AzNotificationHubsNamespaceAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>
<span data-ttu-id="45ca5-107">Le regole di autorizzazione gestiscono l'accesso a uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="45ca5-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="45ca5-108">A tale scopo, è necessario creare collegamenti, come URI, in base a diversi livelli di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="45ca5-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="45ca5-109">I livelli di autorizzazione possono essere i seguenti:</span><span class="sxs-lookup"><span data-stu-id="45ca5-109">Permission levels can be of the following:</span></span> 
- <span data-ttu-id="45ca5-110">Ascoltare</span><span class="sxs-lookup"><span data-stu-id="45ca5-110">Listen</span></span>
- <span data-ttu-id="45ca5-111">Invia</span><span class="sxs-lookup"><span data-stu-id="45ca5-111">Send</span></span>
- <span data-ttu-id="45ca5-112">La gestione dei client viene indirizzata a uno di questi URL in base al livello di autorizzazione appropriato.</span><span class="sxs-lookup"><span data-stu-id="45ca5-112">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="45ca5-113">Ad esempio, un client con l'autorizzazione di ascolto viene indirizzato all'URI per tale autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="45ca5-113">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>
<span data-ttu-id="45ca5-114">La rimozione di una regola di autorizzazione comporta anche la rimozione dell'autorizzazione utente corrispondente.</span><span class="sxs-lookup"><span data-stu-id="45ca5-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="45ca5-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45ca5-115">EXAMPLES</span></span>

### <span data-ttu-id="45ca5-116">Esempio 1: Rimuovere una regola di autorizzazione da uno spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="45ca5-116">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzNotificationHubNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="45ca5-117">Questo comando rimuove la regola di autorizzazione denominata ListenRule dallo spazio dei nomi denominato Contoso Dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="45ca5-117">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="45ca5-118">Quando si esegue questo comando è necessario specificare il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="45ca5-118">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="45ca5-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45ca5-119">PARAMETERS</span></span>

### <span data-ttu-id="45ca5-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="45ca5-120">-AuthorizationRule</span></span>
<span data-ttu-id="45ca5-121">Specifica il nome della regola di autenticazione della firma di accesso condiviso da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="45ca5-121">Specifies the name of the SAS authentication rule to be removed.</span></span>

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

### <span data-ttu-id="45ca5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45ca5-122">-DefaultProfile</span></span>
<span data-ttu-id="45ca5-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="45ca5-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45ca5-124">-Force</span><span class="sxs-lookup"><span data-stu-id="45ca5-124">-Force</span></span>
<span data-ttu-id="45ca5-125">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="45ca5-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="45ca5-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="45ca5-126">-Namespace</span></span>
<span data-ttu-id="45ca5-127">Specifica lo spazio dei nomi a cui vengono assegnate le regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="45ca5-127">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="45ca5-128">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="45ca5-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="45ca5-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="45ca5-129">-ResourceGroup</span></span>
<span data-ttu-id="45ca5-130">Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="45ca5-130">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="45ca5-131">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che consentono semplicemente la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="45ca5-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="45ca5-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45ca5-132">-Confirm</span></span>
<span data-ttu-id="45ca5-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45ca5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45ca5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45ca5-134">-WhatIf</span></span>
<span data-ttu-id="45ca5-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45ca5-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45ca5-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45ca5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45ca5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45ca5-137">CommonParameters</span></span>
<span data-ttu-id="45ca5-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45ca5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45ca5-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45ca5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45ca5-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="45ca5-140">INPUTS</span></span>

### <span data-ttu-id="45ca5-141">System.String</span><span class="sxs-lookup"><span data-stu-id="45ca5-141">System.String</span></span>

## <span data-ttu-id="45ca5-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45ca5-142">OUTPUTS</span></span>

### <span data-ttu-id="45ca5-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="45ca5-143">System.Boolean</span></span>

## <span data-ttu-id="45ca5-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="45ca5-144">NOTES</span></span>

## <span data-ttu-id="45ca5-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45ca5-145">RELATED LINKS</span></span>

[<span data-ttu-id="45ca5-146">Get-AzNotificationHubsAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="45ca5-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="45ca5-147">New-AzNotificationHubsAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="45ca5-147">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="45ca5-148">Set-AzNotificationHubsAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="45ca5-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Set-AzNotificationHubsNamespaceAuthorizationRule.md)



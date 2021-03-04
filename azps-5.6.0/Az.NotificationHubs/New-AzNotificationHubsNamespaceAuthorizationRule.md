---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 49a856ef38d529c7d60b7c09b4d4a4fcdab5b59b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951246"
---
# <span data-ttu-id="466cd-101">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="466cd-101">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="466cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="466cd-102">SYNOPSIS</span></span>
<span data-ttu-id="466cd-103">Crea una regola di autorizzazione e la assegna a uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="466cd-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

## <span data-ttu-id="466cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="466cd-104">SYNTAX</span></span>

### <span data-ttu-id="466cd-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="466cd-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="466cd-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="466cd-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="466cd-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="466cd-107">DESCRIPTION</span></span>
<span data-ttu-id="466cd-108">Il cmdlet **New-AzNotificationHubsAuthorizationRule** crea una regola di autorizzazione della firma di accesso condiviso e la assegna a uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="466cd-108">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="466cd-109">Le regole di autorizzazione gestiscono i diritti degli utenti per lo spazio dei nomi e per gli hub di notifica contenuti in tale spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="466cd-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>
<span data-ttu-id="466cd-110">Questo cmdlet consente di creare una nuova regola di autorizzazione e assegnarla a uno spazio dei nomi in due modi.</span><span class="sxs-lookup"><span data-stu-id="466cd-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="466cd-111">È possibile creare un'istanza dell'oggetto **SharedAccessAuthorizationRuleAttributes** e quindi configurare tale oggetto con i valori delle proprietà che si vuole che la nuova regola possieda.</span><span class="sxs-lookup"><span data-stu-id="466cd-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="466cd-112">Questa operazione può essere eseguita con .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="466cd-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="466cd-113">È quindi possibile copiare i valori delle proprietà nella nuova regola usando il *parametro SASRule.*</span><span class="sxs-lookup"><span data-stu-id="466cd-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="466cd-114">In alternativa, è possibile creare un file JSON (JavaScript Object Notation) contenente i valori di configurazione pertinenti e quindi applicarlo usando il *parametro InputFile.*</span><span class="sxs-lookup"><span data-stu-id="466cd-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="466cd-115">Un file JSON è un file di testo che usa una sintassi simile alla seguente: {</span><span class="sxs-lookup"><span data-stu-id="466cd-115">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="466cd-116">"Name": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="466cd-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="466cd-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span><span class="sxs-lookup"><span data-stu-id="466cd-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="466cd-118">"Diritti": \[</span><span class="sxs-lookup"><span data-stu-id="466cd-118">"Rights": \[</span></span>  
        <span data-ttu-id="466cd-119">"Ascolta",</span><span class="sxs-lookup"><span data-stu-id="466cd-119">"Listen",</span></span>  
        <span data-ttu-id="466cd-120">"Invia"</span><span class="sxs-lookup"><span data-stu-id="466cd-120">"Send"</span></span>  
    \]  
<span data-ttu-id="466cd-121">} Se usato insieme al cmdlet **New-AzNotificationHubsAuthorizationRule,** l'esempio JSON precedente crea una regola di autorizzazione denominata ContosoAuthorizationRule che fornisce agli utenti i diritti di ascolto e invio allo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="466cd-121">} When used in conjunction with the **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="466cd-122">La *chiave* primaria usata per l'autenticazione può essere generata casualmente usando il comando Windows PowerShell \[ seguente: Convert \] ::ToBase64String((1..32 |% { \[ byte/](Get-Random -Minimum 0 -Maximum 255) }))</span><span class="sxs-lookup"><span data-stu-id="466cd-122">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command: \[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="466cd-123">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="466cd-123">EXAMPLES</span></span>

### <span data-ttu-id="466cd-124">Esempio 1: Creare una regola di autorizzazione e assegnarla a uno spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="466cd-124">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="466cd-125">Questo comando crea una regola di autorizzazione e la assegna allo spazio dei nomi ContosoNtassi.</span><span class="sxs-lookup"><span data-stu-id="466cd-125">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="466cd-126">Quando si crea questa regola, è necessario specificare lo spazio dei nomi appropriato e il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="466cd-126">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="466cd-127">Non è tuttavia necessario specificare informazioni sulla regola stessa: le informazioni sulla regola verranno prese dal file C:\Configuration\NamespaceAuthorizationRules.jsdi input.</span><span class="sxs-lookup"><span data-stu-id="466cd-127">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="466cd-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="466cd-128">PARAMETERS</span></span>

### <span data-ttu-id="466cd-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="466cd-129">-DefaultProfile</span></span>
<span data-ttu-id="466cd-130">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="466cd-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="466cd-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="466cd-131">-InputFile</span></span>
<span data-ttu-id="466cd-132">Specifica il percorso di un file JSON contenente informazioni di configurazione per la nuova regola di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="466cd-132">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="466cd-133">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="466cd-133">-Namespace</span></span>
<span data-ttu-id="466cd-134">Specifica lo spazio dei nomi a cui verranno assegnate le regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="466cd-134">Specifies the namespace to which the authorization rules will be assigned.</span></span>
<span data-ttu-id="466cd-135">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="466cd-135">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="466cd-136">Le nuove regole devono essere assegnate a uno spazio dei nomi esistente.</span><span class="sxs-lookup"><span data-stu-id="466cd-136">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="466cd-137">Il cmdlet **New-AzNotificationHubsAuthorizationRule** non può creare un nuovo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="466cd-137">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="466cd-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="466cd-138">-ResourceGroup</span></span>
<span data-ttu-id="466cd-139">Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="466cd-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="466cd-140">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che consentono semplicemente la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="466cd-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="466cd-141">È necessario usare un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="466cd-141">You must use an existing resource group.</span></span>
<span data-ttu-id="466cd-142">Questo cmdlet non può creare un nuovo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="466cd-142">This cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="466cd-143">-SASRule</span><span class="sxs-lookup"><span data-stu-id="466cd-143">-SASRule</span></span>
<span data-ttu-id="466cd-144">Specifica **l'oggetto SharedAccessAuthorizationRuleAttributes** contenente informazioni di configurazione per le nuove regole.</span><span class="sxs-lookup"><span data-stu-id="466cd-144">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="466cd-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="466cd-145">-Confirm</span></span>
<span data-ttu-id="466cd-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="466cd-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="466cd-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="466cd-147">-WhatIf</span></span>
<span data-ttu-id="466cd-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="466cd-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="466cd-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="466cd-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="466cd-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="466cd-150">CommonParameters</span></span>
<span data-ttu-id="466cd-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="466cd-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="466cd-152">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="466cd-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="466cd-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="466cd-153">INPUTS</span></span>

### <span data-ttu-id="466cd-154">System.String</span><span class="sxs-lookup"><span data-stu-id="466cd-154">System.String</span></span>

## <span data-ttu-id="466cd-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="466cd-155">OUTPUTS</span></span>

### <span data-ttu-id="466cd-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="466cd-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="466cd-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="466cd-157">NOTES</span></span>

## <span data-ttu-id="466cd-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="466cd-158">RELATED LINKS</span></span>

[<span data-ttu-id="466cd-159">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="466cd-159">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="466cd-160">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="466cd-160">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="466cd-161">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="466cd-161">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)



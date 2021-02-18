---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 34f63dfc89f2bb1b3b9601e8ff51b280fee9ee42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206378"
---
# <span data-ttu-id="ad5e2-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ad5e2-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="ad5e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad5e2-102">SYNOPSIS</span></span>
<span data-ttu-id="ad5e2-103">Imposta le regole di autorizzazione per uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ad5e2-103">Sets authorization rules for a notification hub namespace.</span></span>

## <span data-ttu-id="ad5e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad5e2-104">SYNTAX</span></span>

### <span data-ttu-id="ad5e2-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad5e2-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad5e2-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad5e2-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad5e2-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ad5e2-107">DESCRIPTION</span></span>
<span data-ttu-id="ad5e2-108">Il cmdlet **Set-AzNotificationHubsAuthorizationRule** modifica una regola di autorizzazione della firma di accesso condiviso assegnata a uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ad5e2-108">The **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="ad5e2-109">Le regole di autorizzazione gestiscono i diritti degli utenti per lo spazio dei nomi e per gli hub di notifica contenuti in tale spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ad5e2-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>
<span data-ttu-id="ad5e2-110">Questo cmdlet consente di modificare una regola di autorizzazione assegnata a uno spazio dei nomi in due modi.</span><span class="sxs-lookup"><span data-stu-id="ad5e2-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="ad5e2-111">Per un oggetto, è possibile creare un'istanza dell'oggetto **SharedAccessAuthorizationRuleAttributes** e quindi configurarlo con i valori delle proprietà che si vuole che la regola possieda.</span><span class="sxs-lookup"><span data-stu-id="ad5e2-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="ad5e2-112">A questo scopo, è possibile usare .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ad5e2-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="ad5e2-113">È quindi possibile copiare questi valori di proprietà nella regola tramite il *parametro SASRule.*</span><span class="sxs-lookup"><span data-stu-id="ad5e2-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>
<span data-ttu-id="ad5e2-114">In alternativa, è possibile creare un file JSON (JavaScript Object Notation) contenente i valori di configurazione pertinenti e quindi applicarlo tramite il *parametro InputFile.*</span><span class="sxs-lookup"><span data-stu-id="ad5e2-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="ad5e2-115">Un file JSON è un file di testo che usa una sintassi simile alla seguente: {</span><span class="sxs-lookup"><span data-stu-id="ad5e2-115">A JSON file is a text file that uses syntax similar to this: {</span></span>  
    <span data-ttu-id="ad5e2-116">"Name": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="ad5e2-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="ad5e2-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span><span class="sxs-lookup"><span data-stu-id="ad5e2-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="ad5e2-118">"Diritti": \[</span><span class="sxs-lookup"><span data-stu-id="ad5e2-118">"Rights": \[</span></span>  
        <span data-ttu-id="ad5e2-119">"Ascolta",</span><span class="sxs-lookup"><span data-stu-id="ad5e2-119">"Listen",</span></span>  
        <span data-ttu-id="ad5e2-120">"Invia"</span><span class="sxs-lookup"><span data-stu-id="ad5e2-120">"Send"</span></span>  
    \]  
<span data-ttu-id="ad5e2-121">} Se usato insieme al cmdlet **Set-AzNotificationHubsAuthorizationRule,** l'esempio JSON precedente modifica una regola di autorizzazione denominata ContosoAuthorizationRule per concedere agli utenti i diritti di ascolto e invio allo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ad5e2-121">} When used in conjunction with the **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="ad5e2-122">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad5e2-122">EXAMPLES</span></span>

### <span data-ttu-id="ad5e2-123">Esempio 1: Modificare una regola di autorizzazione assegnata a uno spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ad5e2-123">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="ad5e2-124">Questo comando modifica una regola di autorizzazione assegnata allo spazio dei nomi denominato Contoso Dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ad5e2-124">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="ad5e2-125">È necessario specificare il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ad5e2-125">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="ad5e2-126">Le informazioni sulla regola di autorizzazione non vengono incluse nel comando stesso.</span><span class="sxs-lookup"><span data-stu-id="ad5e2-126">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="ad5e2-127">Queste informazioni vengono ottenute dal file di input C:\Configuration\AuthorizationRules.jsavanti.</span><span class="sxs-lookup"><span data-stu-id="ad5e2-127">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="ad5e2-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad5e2-128">PARAMETERS</span></span>

### <span data-ttu-id="ad5e2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad5e2-129">-DefaultProfile</span></span>
<span data-ttu-id="ad5e2-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="ad5e2-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad5e2-131">-Force</span><span class="sxs-lookup"><span data-stu-id="ad5e2-131">-Force</span></span>
<span data-ttu-id="ad5e2-132">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ad5e2-132">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ad5e2-133">-InputFile</span><span class="sxs-lookup"><span data-stu-id="ad5e2-133">-InputFile</span></span>
<span data-ttu-id="ad5e2-134">Specifica il percorso di un file JSON contenente informazioni di configurazione per la nuova regola.</span><span class="sxs-lookup"><span data-stu-id="ad5e2-134">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="ad5e2-135">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ad5e2-135">-Namespace</span></span>
<span data-ttu-id="ad5e2-136">Specifica lo spazio dei nomi che contiene le regole di autorizzazione che il cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="ad5e2-136">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="ad5e2-137">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="ad5e2-137">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="ad5e2-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ad5e2-138">-ResourceGroup</span></span>
<span data-ttu-id="ad5e2-139">Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="ad5e2-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="ad5e2-140">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che consentono semplicemente la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5e2-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="ad5e2-141">-SASRule</span><span class="sxs-lookup"><span data-stu-id="ad5e2-141">-SASRule</span></span>
<span data-ttu-id="ad5e2-142">Specifica **l'oggetto SharedAccessAuthorizationRuleAttributes** che contiene informazioni di configurazione per le regole di autorizzazione che il cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="ad5e2-142">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ad5e2-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad5e2-143">-Confirm</span></span>
<span data-ttu-id="ad5e2-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad5e2-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad5e2-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad5e2-145">-WhatIf</span></span>
<span data-ttu-id="ad5e2-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad5e2-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad5e2-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad5e2-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad5e2-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad5e2-148">CommonParameters</span></span>
<span data-ttu-id="ad5e2-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad5e2-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad5e2-150">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad5e2-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad5e2-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="ad5e2-151">INPUTS</span></span>

### <span data-ttu-id="ad5e2-152">System.String</span><span class="sxs-lookup"><span data-stu-id="ad5e2-152">System.String</span></span>

## <span data-ttu-id="ad5e2-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad5e2-153">OUTPUTS</span></span>

### <span data-ttu-id="ad5e2-154">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ad5e2-154">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ad5e2-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="ad5e2-155">NOTES</span></span>

## <span data-ttu-id="ad5e2-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad5e2-156">RELATED LINKS</span></span>

[<span data-ttu-id="ad5e2-157">Get-AzNotificationHubsAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ad5e2-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="ad5e2-158">New-AzNotificationHubsAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ad5e2-158">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="ad5e2-159">Remove-AzNotificationHubsAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ad5e2-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Remove-AzNotificationHubsNamespaceAuthorizationRule.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/set-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 30c6a16d7b9cfb94f1fb2032940aa4587d27e550
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951102"
---
# <span data-ttu-id="665b0-101">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="665b0-101">Set-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="665b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="665b0-102">SYNOPSIS</span></span>
<span data-ttu-id="665b0-103">Imposta le regole di autorizzazione per un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="665b0-103">Sets authorization rules for a notification hub.</span></span>

## <span data-ttu-id="665b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="665b0-104">SYNTAX</span></span>

### <span data-ttu-id="665b0-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="665b0-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="665b0-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="665b0-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="665b0-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="665b0-107">DESCRIPTION</span></span>
<span data-ttu-id="665b0-108">Il cmdlet **Set-AzNotificationHubAuthorizationRule** modifica una regola di autorizzazione della firma di accesso condiviso assegnata a un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="665b0-108">The **Set-AzNotificationHubAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="665b0-109">Le regole di autorizzazione gestiscono l'accesso agli hub di notifica tramite la creazione di collegamenti, come URI, in base a diversi livelli di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="665b0-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="665b0-110">I livelli di autorizzazione possono essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="665b0-110">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="665b0-111">Ascoltare</span><span class="sxs-lookup"><span data-stu-id="665b0-111">Listen</span></span>
- <span data-ttu-id="665b0-112">Invia</span><span class="sxs-lookup"><span data-stu-id="665b0-112">Send</span></span>
- <span data-ttu-id="665b0-113">La gestione dei client viene indirizzata a uno di questi URI in base al livello di autorizzazione appropriato.</span><span class="sxs-lookup"><span data-stu-id="665b0-113">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="665b0-114">Ad esempio, un client con l'autorizzazione di ascolto verrà indirizzato all'URI per tale autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="665b0-114">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="665b0-115">Questo cmdlet consente di modificare una regola di autorizzazione assegnata a un hub di notifica in due modi.</span><span class="sxs-lookup"><span data-stu-id="665b0-115">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="665b0-116">Per un oggetto, è possibile creare un'istanza dell'oggetto **SharedAccessAuthorizationRuleAttributes** e quindi configurarlo con i valori delle proprietà che si vuole che la regola possieda.</span><span class="sxs-lookup"><span data-stu-id="665b0-116">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="665b0-117">È possibile configurare l'oggetto tramite la .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="665b0-117">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="665b0-118">È quindi possibile copiare tali valori di proprietà nella regola usando il *parametro SASRule.*</span><span class="sxs-lookup"><span data-stu-id="665b0-118">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="665b0-119">In alternativa, è possibile creare un file JSON (JavaScript Object Notation) contenente i valori di configurazione pertinenti e quindi applicarlo tramite il *parametro InputFile.*</span><span class="sxs-lookup"><span data-stu-id="665b0-119">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="665b0-120">Un file JSON è un file di testo che usa una sintassi simile alla seguente: { "Name": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="665b0-120">A JSON file is a text file that uses syntax similar to this: {      "Name": "ContosoAuthorizationRule",</span></span>  
  <span data-ttu-id="665b0-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span><span class="sxs-lookup"><span data-stu-id="665b0-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
  <span data-ttu-id="665b0-122">"Diritti": \[</span><span class="sxs-lookup"><span data-stu-id="665b0-122">"Rights": \[</span></span>  
        <span data-ttu-id="665b0-123">"Ascolta",</span><span class="sxs-lookup"><span data-stu-id="665b0-123">"Listen",</span></span>  
        <span data-ttu-id="665b0-124">"Invia"</span><span class="sxs-lookup"><span data-stu-id="665b0-124">"Send"</span></span>  
    \]  
  <span data-ttu-id="665b0-125">} Se usato insieme al cmdlet New-AzNotificationHubAuthorizationRule, l'esempio JSON precedente modifica una regola di autorizzazione denominata ContosoAuthorizationRule per fornire agli utenti i diritti di ascolto e invio all'hub.</span><span class="sxs-lookup"><span data-stu-id="665b0-125">} When used in conjunction with the New-AzNotificationHubAuthorizationRule cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="665b0-126">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="665b0-126">EXAMPLES</span></span>

### <span data-ttu-id="665b0-127">Esempio 1: Modificare una regola di autorizzazione assegnata a un hub di notifica</span><span class="sxs-lookup"><span data-stu-id="665b0-127">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="665b0-128">Questo comando modifica una regola di autorizzazione assegnata all'hub di notifica denominato ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="665b0-128">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="665b0-129">È necessario specificare lo spazio dei nomi in cui si trova l'hub e il gruppo di risorse a cui è assegnato l'hub.</span><span class="sxs-lookup"><span data-stu-id="665b0-129">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="665b0-130">Le informazioni sulla regola modificata non vengono incluse nel comando stesso.</span><span class="sxs-lookup"><span data-stu-id="665b0-130">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="665b0-131">Queste informazioni si trovano invece nel file di input C:\Configuration\AuthorizationRules.jsavanti.</span><span class="sxs-lookup"><span data-stu-id="665b0-131">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="665b0-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="665b0-132">PARAMETERS</span></span>

### <span data-ttu-id="665b0-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="665b0-133">-DefaultProfile</span></span>
<span data-ttu-id="665b0-134">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="665b0-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="665b0-135">-Force</span><span class="sxs-lookup"><span data-stu-id="665b0-135">-Force</span></span>
<span data-ttu-id="665b0-136">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="665b0-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="665b0-137">-InputFile</span><span class="sxs-lookup"><span data-stu-id="665b0-137">-InputFile</span></span>
<span data-ttu-id="665b0-138">Specifica il percorso di un file JSON contenente informazioni di configurazione per la nuova regola.</span><span class="sxs-lookup"><span data-stu-id="665b0-138">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="665b0-139">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="665b0-139">-Namespace</span></span>
<span data-ttu-id="665b0-140">Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="665b0-140">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="665b0-141">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="665b0-141">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="665b0-142">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="665b0-142">-NotificationHub</span></span>
<span data-ttu-id="665b0-143">Specifica l'hub di notifica a cui questo cmdlet assegna regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="665b0-143">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="665b0-144">Gli hub di notifica vengono usati per inviare notifiche push a più client, indipendentemente da quelli usati.</span><span class="sxs-lookup"><span data-stu-id="665b0-144">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="665b0-145">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="665b0-145">-ResourceGroup</span></span>
<span data-ttu-id="665b0-146">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="665b0-146">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="665b0-147">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che consentono semplicemente la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="665b0-147">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="665b0-148">-SASRule</span><span class="sxs-lookup"><span data-stu-id="665b0-148">-SASRule</span></span>
<span data-ttu-id="665b0-149">Specifica **l'oggetto SharedAccessAuthorizationRuleAttributes** che contiene informazioni di configurazione per le regole di autorizzazione modificate.</span><span class="sxs-lookup"><span data-stu-id="665b0-149">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="665b0-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="665b0-150">-Confirm</span></span>
<span data-ttu-id="665b0-151">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="665b0-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="665b0-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="665b0-152">-WhatIf</span></span>
<span data-ttu-id="665b0-153">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="665b0-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="665b0-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="665b0-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="665b0-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="665b0-155">CommonParameters</span></span>
<span data-ttu-id="665b0-156">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="665b0-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="665b0-157">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="665b0-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="665b0-158">INPUT</span><span class="sxs-lookup"><span data-stu-id="665b0-158">INPUTS</span></span>

### <span data-ttu-id="665b0-159">System.String</span><span class="sxs-lookup"><span data-stu-id="665b0-159">System.String</span></span>

## <span data-ttu-id="665b0-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="665b0-160">OUTPUTS</span></span>

### <span data-ttu-id="665b0-161">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="665b0-161">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="665b0-162">NOTE</span><span class="sxs-lookup"><span data-stu-id="665b0-162">NOTES</span></span>

## <span data-ttu-id="665b0-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="665b0-163">RELATED LINKS</span></span>

[<span data-ttu-id="665b0-164">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="665b0-164">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="665b0-165">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="665b0-165">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="665b0-166">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="665b0-166">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)



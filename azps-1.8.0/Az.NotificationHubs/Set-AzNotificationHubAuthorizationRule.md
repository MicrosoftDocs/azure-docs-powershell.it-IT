---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 74aa4d00d387e832c1abf02a5c65ca5e34e42123
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677839"
---
# <span data-ttu-id="510e4-101">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="510e4-101">Set-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="510e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="510e4-102">SYNOPSIS</span></span>
<span data-ttu-id="510e4-103">Imposta le regole di autorizzazione per un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="510e4-103">Sets authorization rules for a notification hub.</span></span>

## <span data-ttu-id="510e4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="510e4-104">SYNTAX</span></span>

### <span data-ttu-id="510e4-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="510e4-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="510e4-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="510e4-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="510e4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="510e4-107">DESCRIPTION</span></span>
<span data-ttu-id="510e4-108">Il cmdlet **set-AzNotificationHubAuthorizationRule** modifica una regola di autorizzazione della firma di accesso condiviso (SAS) assegnata a un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="510e4-108">The **Set-AzNotificationHubAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="510e4-109">Le regole di autorizzazione gestiscono l'accesso agli hub di notifica tramite la creazione di collegamenti, come URI, in base a livelli di autorizzazione diversi.</span><span class="sxs-lookup"><span data-stu-id="510e4-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="510e4-110">I livelli di autorizzazione possono essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="510e4-110">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="510e4-111">Ascoltare</span><span class="sxs-lookup"><span data-stu-id="510e4-111">Listen</span></span>
- <span data-ttu-id="510e4-112">Invia</span><span class="sxs-lookup"><span data-stu-id="510e4-112">Send</span></span>
- <span data-ttu-id="510e4-113">I client di gestione vengono indirizzati a uno di questi URI in base al livello di autorizzazione appropriato.</span><span class="sxs-lookup"><span data-stu-id="510e4-113">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="510e4-114">Ad esempio, un client assegnato l'autorizzazione Listen verrà indirizzato all'URI per l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="510e4-114">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="510e4-115">Questo cmdlet offre due modi per modificare una regola di autorizzazione assegnata a un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="510e4-115">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="510e4-116">Per uno, puoi creare un'istanza dell'oggetto **SharedAccessAuthorizationRuleAttributes** e quindi configurare l'oggetto con i valori della proprietà che vuoi che la regola possieda.</span><span class="sxs-lookup"><span data-stu-id="510e4-116">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="510e4-117">Puoi configurare l'oggetto tramite .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="510e4-117">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="510e4-118">Puoi quindi copiare questi valori di proprietà nella regola usando il parametro *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="510e4-118">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="510e4-119">In alternativa, puoi creare un file JSON (JavaScript Object Notation) contenente i valori di configurazione rilevanti e quindi applicare tali valori tramite il parametro *inputfile* .</span><span class="sxs-lookup"><span data-stu-id="510e4-119">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="510e4-120">Un file JSON è un file di testo che usa una sintassi simile alla seguente: {"Name": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="510e4-120">A JSON file is a text file that uses syntax similar to this: {      "Name": "ContosoAuthorizationRule",</span></span>  
  <span data-ttu-id="510e4-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",</span><span class="sxs-lookup"><span data-stu-id="510e4-121">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
  <span data-ttu-id="510e4-122">"Diritti": \[</span><span class="sxs-lookup"><span data-stu-id="510e4-122">"Rights": \[</span></span>  
        <span data-ttu-id="510e4-123">"Ascolta",</span><span class="sxs-lookup"><span data-stu-id="510e4-123">"Listen",</span></span>  
        <span data-ttu-id="510e4-124">Inviare</span><span class="sxs-lookup"><span data-stu-id="510e4-124">"Send"</span></span>  
    \]  
  <span data-ttu-id="510e4-125">} Se usato insieme al cmdlet New-AzNotificationHubAuthorizationRule, l'esempio JSON precedente modifica una regola di autorizzazione denominata ContosoAuthorizationRule per consentire agli utenti di ascoltare e inviare diritti all'hub.</span><span class="sxs-lookup"><span data-stu-id="510e4-125">} When used in conjunction with the New-AzNotificationHubAuthorizationRule cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="510e4-126">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="510e4-126">EXAMPLES</span></span>

### <span data-ttu-id="510e4-127">Esempio 1: modificare una regola di autorizzazione assegnata a un hub di notifica</span><span class="sxs-lookup"><span data-stu-id="510e4-127">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="510e4-128">Questo comando consente di modificare una regola di autorizzazione assegnata all'hub di notifica denominato ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="510e4-128">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="510e4-129">Devi specificare lo spazio dei nomi in cui si trova l'hub e il gruppo di risorse assegnato all'hub.</span><span class="sxs-lookup"><span data-stu-id="510e4-129">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="510e4-130">Le informazioni sulla regola modificata non sono incluse nel comando stesso.</span><span class="sxs-lookup"><span data-stu-id="510e4-130">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="510e4-131">Queste informazioni si trovano invece nel file di input C:\Configuration\AuthorizationRules.jsattivato.</span><span class="sxs-lookup"><span data-stu-id="510e4-131">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="510e4-132">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="510e4-132">PARAMETERS</span></span>

### <span data-ttu-id="510e4-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="510e4-133">-DefaultProfile</span></span>
<span data-ttu-id="510e4-134">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="510e4-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="510e4-135">-Force</span><span class="sxs-lookup"><span data-stu-id="510e4-135">-Force</span></span>
<span data-ttu-id="510e4-136">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="510e4-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="510e4-137">-InputFile</span><span class="sxs-lookup"><span data-stu-id="510e4-137">-InputFile</span></span>
<span data-ttu-id="510e4-138">Specifica il percorso di un file JSON contenente le informazioni di configurazione per la nuova regola.</span><span class="sxs-lookup"><span data-stu-id="510e4-138">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="510e4-139">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="510e4-139">-Namespace</span></span>
<span data-ttu-id="510e4-140">Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="510e4-140">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="510e4-141">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="510e4-141">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="510e4-142">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="510e4-142">-NotificationHub</span></span>
<span data-ttu-id="510e4-143">Specifica l'hub di notifica a cui questo cmdlet assegna le regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="510e4-143">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="510e4-144">Gli hub di notifica vengono usati per inviare notifiche push a più client, indipendentemente dall'uso usato da tali client.</span><span class="sxs-lookup"><span data-stu-id="510e4-144">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="510e4-145">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="510e4-145">-ResourceGroup</span></span>
<span data-ttu-id="510e4-146">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="510e4-146">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="510e4-147">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="510e4-147">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="510e4-148">-SASRule</span><span class="sxs-lookup"><span data-stu-id="510e4-148">-SASRule</span></span>
<span data-ttu-id="510e4-149">Specifica l'oggetto **SharedAccessAuthorizationRuleAttributes** che contiene le informazioni di configurazione per le regole di autorizzazione modificate.</span><span class="sxs-lookup"><span data-stu-id="510e4-149">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

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

### <span data-ttu-id="510e4-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="510e4-150">-Confirm</span></span>
<span data-ttu-id="510e4-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="510e4-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="510e4-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="510e4-152">-WhatIf</span></span>
<span data-ttu-id="510e4-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="510e4-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="510e4-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="510e4-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="510e4-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="510e4-155">CommonParameters</span></span>
<span data-ttu-id="510e4-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="510e4-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="510e4-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="510e4-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="510e4-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="510e4-158">INPUTS</span></span>

### <span data-ttu-id="510e4-159">System. String</span><span class="sxs-lookup"><span data-stu-id="510e4-159">System.String</span></span>

## <span data-ttu-id="510e4-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="510e4-160">OUTPUTS</span></span>

### <span data-ttu-id="510e4-161">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="510e4-161">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="510e4-162">Note</span><span class="sxs-lookup"><span data-stu-id="510e4-162">NOTES</span></span>

## <span data-ttu-id="510e4-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="510e4-163">RELATED LINKS</span></span>

[<span data-ttu-id="510e4-164">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="510e4-164">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="510e4-165">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="510e4-165">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="510e4-166">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="510e4-166">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)



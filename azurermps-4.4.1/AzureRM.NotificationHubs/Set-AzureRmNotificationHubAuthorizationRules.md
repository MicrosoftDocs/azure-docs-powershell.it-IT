---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: BD311CEF-378B-463E-8998-CC3E9A5B3A7B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 5396605719908d468399c126fbeca116060c25b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513151"
---
# <span data-ttu-id="91b6e-101">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="91b6e-101">Set-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="91b6e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91b6e-102">SYNOPSIS</span></span>
<span data-ttu-id="91b6e-103">Imposta le regole di autorizzazione per un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="91b6e-103">Sets authorization rules for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91b6e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91b6e-104">SYNTAX</span></span>

### <span data-ttu-id="91b6e-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="91b6e-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91b6e-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="91b6e-106">SASRuleParameterSet</span></span>
```
Set-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91b6e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91b6e-107">DESCRIPTION</span></span>
<span data-ttu-id="91b6e-108">Il cmdlet **set-AzureRmNotificationHubAuthorizationRules** modifica una regola di autorizzazione della firma di accesso condiviso (SAS) assegnata a un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="91b6e-108">The **Set-AzureRmNotificationHubAuthorizationRules** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub.</span></span>

<span data-ttu-id="91b6e-109">Le regole di autorizzazione gestiscono l'accesso agli hub di notifica tramite la creazione di collegamenti, come URI, in base a livelli di autorizzazione diversi.</span><span class="sxs-lookup"><span data-stu-id="91b6e-109">Authorization rules manage access to your notification hubs by the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="91b6e-110">I livelli di autorizzazione possono essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="91b6e-110">Permission levels can be one of the following:</span></span> 

- <span data-ttu-id="91b6e-111">Ascoltare</span><span class="sxs-lookup"><span data-stu-id="91b6e-111">Listen</span></span>
- <span data-ttu-id="91b6e-112">Invia</span><span class="sxs-lookup"><span data-stu-id="91b6e-112">Send</span></span>
- <span data-ttu-id="91b6e-113">Gestire</span><span class="sxs-lookup"><span data-stu-id="91b6e-113">Manage</span></span>

<span data-ttu-id="91b6e-114">I client vengono indirizzati a uno di questi URI in base al livello di autorizzazione appropriato.</span><span class="sxs-lookup"><span data-stu-id="91b6e-114">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="91b6e-115">Ad esempio, un client assegnato l'autorizzazione Listen verrà indirizzato all'URI per l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="91b6e-115">For example, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="91b6e-116">Questo cmdlet offre due modi per modificare una regola di autorizzazione assegnata a un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="91b6e-116">This cmdlet provides two ways to modify an authorization rule assigned to a notification hub.</span></span>
<span data-ttu-id="91b6e-117">Per uno, puoi creare un'istanza dell'oggetto **SharedAccessAuthorizationRuleAttributes** e quindi configurare l'oggetto con i valori della proprietà che vuoi che la regola possieda.</span><span class="sxs-lookup"><span data-stu-id="91b6e-117">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="91b6e-118">Puoi configurare l'oggetto tramite .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="91b6e-118">You can configure the object through the .NET Framework.</span></span>
<span data-ttu-id="91b6e-119">Puoi quindi copiare questi valori di proprietà nella regola usando il parametro *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="91b6e-119">You can then copy those property values to your rule by using *SASRule* parameter.</span></span>

<span data-ttu-id="91b6e-120">In alternativa, puoi creare un file JSON (JavaScript Object Notation) contenente i valori di configurazione rilevanti e quindi applicare tali valori tramite il parametro *inputfile* .</span><span class="sxs-lookup"><span data-stu-id="91b6e-120">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="91b6e-121">Un file JSON è un file di testo che usa una sintassi simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="91b6e-121">A JSON file is a text file that uses syntax similar to this:</span></span>

<span data-ttu-id="91b6e-122">{"Nome": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="91b6e-122">{      "Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="91b6e-123">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",</span><span class="sxs-lookup"><span data-stu-id="91b6e-123">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="91b6e-124">"Diritti": \[</span><span class="sxs-lookup"><span data-stu-id="91b6e-124">"Rights": \[</span></span>  
        <span data-ttu-id="91b6e-125">"Ascolta",</span><span class="sxs-lookup"><span data-stu-id="91b6e-125">"Listen",</span></span>  
        <span data-ttu-id="91b6e-126">Inviare</span><span class="sxs-lookup"><span data-stu-id="91b6e-126">"Send"</span></span>  
    \]  
<span data-ttu-id="91b6e-127">}</span><span class="sxs-lookup"><span data-stu-id="91b6e-127">}</span></span>

<span data-ttu-id="91b6e-128">Se usato insieme al cmdlet New-AzureRmNotificationHubAuthorizationRules, l'esempio JSON precedente modifica una regola di autorizzazione denominata ContosoAuthorizationRule per consentire agli utenti di ascoltare e inviare diritti all'hub.</span><span class="sxs-lookup"><span data-stu-id="91b6e-128">When used in conjunction with the New-AzureRmNotificationHubAuthorizationRules cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule in order to give users Listen and Send rights to the hub.</span></span>

## <span data-ttu-id="91b6e-129">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91b6e-129">EXAMPLES</span></span>

### <span data-ttu-id="91b6e-130">Esempio 1: modificare una regola di autorizzazione assegnata a un hub di notifica</span><span class="sxs-lookup"><span data-stu-id="91b6e-130">Example 1: Modify an authorization rule assigned to a notification hub</span></span>
```
PS C:\>Set-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -NotificationHub "ContosoExternalHub" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="91b6e-131">Questo comando consente di modificare una regola di autorizzazione assegnata all'hub di notifica denominato ContosoExternalHub.</span><span class="sxs-lookup"><span data-stu-id="91b6e-131">This command modifies an authorization rule assigned to the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="91b6e-132">Devi specificare lo spazio dei nomi in cui si trova l'hub e il gruppo di risorse assegnato all'hub.</span><span class="sxs-lookup"><span data-stu-id="91b6e-132">You must specify the namespace where the hub is located as well as the resource group that the hub is assigned.</span></span>
<span data-ttu-id="91b6e-133">Le informazioni sulla regola modificata non sono incluse nel comando stesso.</span><span class="sxs-lookup"><span data-stu-id="91b6e-133">Information about the rule that is modified is not included in the command itself.</span></span>
<span data-ttu-id="91b6e-134">Queste informazioni si trovano invece nel file di input C:\Configuration\AuthorizationRules.jsattivato.</span><span class="sxs-lookup"><span data-stu-id="91b6e-134">Instead, that information is found in the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="91b6e-135">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91b6e-135">PARAMETERS</span></span>

### <span data-ttu-id="91b6e-136">-Force</span><span class="sxs-lookup"><span data-stu-id="91b6e-136">-Force</span></span>
<span data-ttu-id="91b6e-137">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="91b6e-137">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="91b6e-138">-InputFile</span><span class="sxs-lookup"><span data-stu-id="91b6e-138">-InputFile</span></span>
<span data-ttu-id="91b6e-139">Specifica il percorso di un file JSON contenente le informazioni di configurazione per la nuova regola.</span><span class="sxs-lookup"><span data-stu-id="91b6e-139">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="91b6e-140">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="91b6e-140">-Namespace</span></span>
<span data-ttu-id="91b6e-141">Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="91b6e-141">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="91b6e-142">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="91b6e-142">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="91b6e-143">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="91b6e-143">-NotificationHub</span></span>
<span data-ttu-id="91b6e-144">Specifica l'hub di notifica a cui questo cmdlet assegna le regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="91b6e-144">Specifies the notification hub that this cmdlet assigns authorization rules to.</span></span>
<span data-ttu-id="91b6e-145">Gli hub di notifica vengono usati per inviare notifiche push a più client, indipendentemente dall'uso usato da tali client.</span><span class="sxs-lookup"><span data-stu-id="91b6e-145">Notification hubs are used to send push notifications to multiple clients regardless of the used by those clients.</span></span>

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

### <span data-ttu-id="91b6e-146">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="91b6e-146">-ResourceGroup</span></span>
<span data-ttu-id="91b6e-147">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="91b6e-147">Specifies the resource group to which the notification hub is assigned.</span></span> <span data-ttu-id="91b6e-148">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="91b6e-148">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="91b6e-149">-SASRule</span><span class="sxs-lookup"><span data-stu-id="91b6e-149">-SASRule</span></span>
<span data-ttu-id="91b6e-150">Specifica l'oggetto **SharedAccessAuthorizationRuleAttributes** che contiene le informazioni di configurazione per le regole di autorizzazione modificate.</span><span class="sxs-lookup"><span data-stu-id="91b6e-150">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that are modified.</span></span>

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

### <span data-ttu-id="91b6e-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="91b6e-151">-Confirm</span></span>
<span data-ttu-id="91b6e-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91b6e-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91b6e-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91b6e-153">-WhatIf</span></span>
<span data-ttu-id="91b6e-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91b6e-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91b6e-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91b6e-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91b6e-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91b6e-156">-DefaultProfile</span></span>
<span data-ttu-id="91b6e-157">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91b6e-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91b6e-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91b6e-158">CommonParameters</span></span>
<span data-ttu-id="91b6e-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91b6e-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91b6e-160">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91b6e-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91b6e-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91b6e-161">INPUTS</span></span>

## <span data-ttu-id="91b6e-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91b6e-162">OUTPUTS</span></span>

### <span data-ttu-id="91b6e-163">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="91b6e-163">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="91b6e-164">Note</span><span class="sxs-lookup"><span data-stu-id="91b6e-164">NOTES</span></span>

## <span data-ttu-id="91b6e-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91b6e-165">RELATED LINKS</span></span>

[<span data-ttu-id="91b6e-166">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="91b6e-166">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="91b6e-167">New-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="91b6e-167">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="91b6e-168">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="91b6e-168">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)



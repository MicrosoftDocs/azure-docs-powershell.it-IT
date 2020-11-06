---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: ed94e34f754298e89bf1f18d5264f11c2c9c308c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521873"
---
# <span data-ttu-id="9e016-101">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9e016-101">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="9e016-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e016-102">SYNOPSIS</span></span>
<span data-ttu-id="9e016-103">Imposta le regole di autorizzazione per uno spazio dei nomi Hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="9e016-103">Sets authorization rules for a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e016-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e016-104">SYNTAX</span></span>

### <span data-ttu-id="9e016-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e016-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e016-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e016-106">SASRuleParameterSet</span></span>
```
Set-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e016-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e016-107">DESCRIPTION</span></span>
<span data-ttu-id="9e016-108">Il cmdlet **set-AzureRmNotificationHubsNamespaceAuthorizationRules** modifica una regola di autorizzazione della firma di accesso condiviso (SAS) assegnata a uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="9e016-108">The **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="9e016-109">Le regole di autorizzazione gestiscono i diritti degli utenti allo spazio dei nomi e agli hub di notifica contenuti nello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="9e016-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>

<span data-ttu-id="9e016-110">Questo cmdlet offre due modi per modificare una regola di autorizzazione assegnata a uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="9e016-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="9e016-111">Per uno, puoi creare un'istanza dell'oggetto **SharedAccessAuthorizationRuleAttributes** e quindi configurare l'oggetto con i valori della proprietà che vuoi che la regola possieda.</span><span class="sxs-lookup"><span data-stu-id="9e016-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="9e016-112">Puoi usare .NET Framework per eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="9e016-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="9e016-113">Puoi quindi copiare questi valori della proprietà nella regola tramite il parametro *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="9e016-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>

<span data-ttu-id="9e016-114">In alternativa, puoi creare un file JSON (JavaScript Object Notation) contenente i valori di configurazione rilevanti e quindi applicare tali valori tramite il parametro *inputfile* .</span><span class="sxs-lookup"><span data-stu-id="9e016-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="9e016-115">Un file JSON è un file di testo che usa una sintassi simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="9e016-115">A JSON file is a text file that uses syntax similar to this:</span></span>

<span data-ttu-id="9e016-116">{</span><span class="sxs-lookup"><span data-stu-id="9e016-116">{</span></span>  
    <span data-ttu-id="9e016-117">"Nome": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="9e016-117">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="9e016-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",</span><span class="sxs-lookup"><span data-stu-id="9e016-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="9e016-119">"Diritti": \[</span><span class="sxs-lookup"><span data-stu-id="9e016-119">"Rights": \[</span></span>  
        <span data-ttu-id="9e016-120">"Ascolta",</span><span class="sxs-lookup"><span data-stu-id="9e016-120">"Listen",</span></span>  
        <span data-ttu-id="9e016-121">Inviare</span><span class="sxs-lookup"><span data-stu-id="9e016-121">"Send"</span></span>  
    \]  
<span data-ttu-id="9e016-122">}</span><span class="sxs-lookup"><span data-stu-id="9e016-122">}</span></span>

<span data-ttu-id="9e016-123">Quando viene usato insieme al cmdlet **set-AzureRmNotificationHubsNamespaceAuthorizationRules** , l'esempio JSON precedente modifica una regola di autorizzazione denominata ContosoAuthorizationRule per consentire agli utenti di ascoltare e inviare diritti allo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="9e016-123">When used in conjunction with the **Set-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="9e016-124">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e016-124">EXAMPLES</span></span>

### <span data-ttu-id="9e016-125">Esempio 1: modificare una regola di autorizzazione assegnata a uno spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9e016-125">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="9e016-126">Questo comando consente di modificare una regola di autorizzazione assegnata allo spazio dei nomi denominato ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="9e016-126">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="9e016-127">Devi specificare il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="9e016-127">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="9e016-128">Le informazioni sulla regola di autorizzazione non sono incluse nel comando stesso.</span><span class="sxs-lookup"><span data-stu-id="9e016-128">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="9e016-129">Queste informazioni vengono invece ottenute dal file di input C:\Configuration\AuthorizationRules.jsattivato.</span><span class="sxs-lookup"><span data-stu-id="9e016-129">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="9e016-130">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e016-130">PARAMETERS</span></span>

### <span data-ttu-id="9e016-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e016-131">-DefaultProfile</span></span>
<span data-ttu-id="9e016-132">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9e016-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e016-133">-Force</span><span class="sxs-lookup"><span data-stu-id="9e016-133">-Force</span></span>
<span data-ttu-id="9e016-134">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="9e016-134">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e016-135">-InputFile</span><span class="sxs-lookup"><span data-stu-id="9e016-135">-InputFile</span></span>
<span data-ttu-id="9e016-136">Specifica il percorso di un file JSON contenente le informazioni di configurazione per la nuova regola.</span><span class="sxs-lookup"><span data-stu-id="9e016-136">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e016-137">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9e016-137">-Namespace</span></span>
<span data-ttu-id="9e016-138">Specifica lo spazio dei nomi che contiene le regole di autorizzazione modificate da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e016-138">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="9e016-139">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="9e016-139">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e016-140">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9e016-140">-ResourceGroup</span></span>
<span data-ttu-id="9e016-141">Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="9e016-141">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="9e016-142">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9e016-142">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e016-143">-SASRule</span><span class="sxs-lookup"><span data-stu-id="9e016-143">-SASRule</span></span>
<span data-ttu-id="9e016-144">Specifica l'oggetto **SharedAccessAuthorizationRuleAttributes** che contiene le informazioni di configurazione per le regole di autorizzazione modificate dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e016-144">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e016-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9e016-145">-Confirm</span></span>
<span data-ttu-id="9e016-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e016-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e016-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e016-147">-WhatIf</span></span>
<span data-ttu-id="9e016-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e016-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e016-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e016-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e016-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e016-150">CommonParameters</span></span>
<span data-ttu-id="9e016-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e016-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e016-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e016-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e016-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e016-153">INPUTS</span></span>

### <span data-ttu-id="9e016-154">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9e016-154">None</span></span>
<span data-ttu-id="9e016-155">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="9e016-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e016-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e016-156">OUTPUTS</span></span>

### <span data-ttu-id="9e016-157">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="9e016-157">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="9e016-158">Note</span><span class="sxs-lookup"><span data-stu-id="9e016-158">NOTES</span></span>

## <span data-ttu-id="9e016-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e016-159">RELATED LINKS</span></span>

[<span data-ttu-id="9e016-160">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9e016-160">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="9e016-161">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9e016-161">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="9e016-162">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="9e016-162">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)



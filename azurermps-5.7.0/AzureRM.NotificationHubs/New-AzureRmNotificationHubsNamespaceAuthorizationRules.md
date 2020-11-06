---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: 2530d4b0075856b6a172bdcf104474d320f657bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519889"
---
# <span data-ttu-id="7b4e9-101">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="7b4e9-101">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="7b4e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b4e9-102">SYNOPSIS</span></span>
<span data-ttu-id="7b4e9-103">Crea una regola di autorizzazione e assegna la regola a uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b4e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b4e9-104">SYNTAX</span></span>

### <span data-ttu-id="7b4e9-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b4e9-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b4e9-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b4e9-106">SASRuleParameterSet</span></span>
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b4e9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b4e9-107">DESCRIPTION</span></span>
<span data-ttu-id="7b4e9-108">Il cmdlet **New-AzureRmNotificationHubsNamespaceAuthorizationRules** crea una regola di autorizzazione della firma di accesso condiviso (SAS) e la assegna a uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-108">The **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="7b4e9-109">Le regole di autorizzazione gestiscono i diritti degli utenti allo spazio dei nomi e agli hub di notifica contenuti in tale spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>

<span data-ttu-id="7b4e9-110">Questo cmdlet offre due modi per creare una nuova regola di autorizzazione e assegnarla a uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="7b4e9-111">Puoi creare un'istanza dell'oggetto **SharedAccessAuthorizationRuleAttributes** e quindi configurare l'oggetto con i valori della proprietà che vuoi che la nuova regola possieda.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="7b4e9-112">Questa operazione può essere eseguita usando .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="7b4e9-113">Puoi quindi copiare questi valori di proprietà nella nuova regola usando il parametro *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="7b4e9-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>

<span data-ttu-id="7b4e9-114">In alternativa, puoi creare un file JSON (JavaScript Object Notation) che contiene i valori di configurazione rilevanti e quindi applicare tali valori usando il parametro *inputfile* .</span><span class="sxs-lookup"><span data-stu-id="7b4e9-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="7b4e9-115">Un file JSON è un file di testo che usa una sintassi simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="7b4e9-115">A JSON file is a text file that uses syntax similar to the following:</span></span>

<span data-ttu-id="7b4e9-116">{</span><span class="sxs-lookup"><span data-stu-id="7b4e9-116">{</span></span>  
    <span data-ttu-id="7b4e9-117">"Nome": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="7b4e9-117">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="7b4e9-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",</span><span class="sxs-lookup"><span data-stu-id="7b4e9-118">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="7b4e9-119">"Diritti": \[</span><span class="sxs-lookup"><span data-stu-id="7b4e9-119">"Rights": \[</span></span>  
        <span data-ttu-id="7b4e9-120">"Ascolta",</span><span class="sxs-lookup"><span data-stu-id="7b4e9-120">"Listen",</span></span>  
        <span data-ttu-id="7b4e9-121">Inviare</span><span class="sxs-lookup"><span data-stu-id="7b4e9-121">"Send"</span></span>  
    \]  
<span data-ttu-id="7b4e9-122">}</span><span class="sxs-lookup"><span data-stu-id="7b4e9-122">}</span></span>

<span data-ttu-id="7b4e9-123">Se usato insieme al cmdlet **New-AzureRmNotificationHubsNamespaceAuthorizationRules** , l'esempio JSON precedente crea una regola di autorizzazione denominata ContosoAuthorizationRule che consente agli utenti di ascoltare e inviare diritti allo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-123">When used in conjunction with the **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="7b4e9-124">Il *PrimaryKey* usato per l'autenticazione può essere generato in modo casuale usando il comando di Windows PowerShell seguente:</span><span class="sxs-lookup"><span data-stu-id="7b4e9-124">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command:</span></span>

<span data-ttu-id="7b4e9-125">\[Convert \] :: ToBase64String ((1.. 32 |% { \[ byte/] (get-random-minimum 0-maximum 255)}))</span><span class="sxs-lookup"><span data-stu-id="7b4e9-125">\[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="7b4e9-126">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b4e9-126">EXAMPLES</span></span>

### <span data-ttu-id="7b4e9-127">Esempio 1: creare una regola di autorizzazione e assegnarla a uno spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7b4e9-127">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="7b4e9-128">Questo comando crea una regola di autorizzazione e assegna la regola allo spazio dei nomi ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-128">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="7b4e9-129">Quando si crea questa regola è necessario specificare lo spazio dei nomi appropriato e il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-129">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="7b4e9-130">Tuttavia, non è necessario specificare alcuna informazione sulla regola stessa: le informazioni sulle regole verranno ricavate dal file di input C:\Configuration\NamespaceAuthorizationRules.jsattivato.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-130">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="7b4e9-131">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b4e9-131">PARAMETERS</span></span>

### <span data-ttu-id="7b4e9-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b4e9-132">-DefaultProfile</span></span>
<span data-ttu-id="7b4e9-133">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7b4e9-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b4e9-134">-InputFile</span><span class="sxs-lookup"><span data-stu-id="7b4e9-134">-InputFile</span></span>
<span data-ttu-id="7b4e9-135">Specifica il percorso di un file JSON contenente le informazioni di configurazione per la nuova regola di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-135">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

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

### <span data-ttu-id="7b4e9-136">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7b4e9-136">-Namespace</span></span>
<span data-ttu-id="7b4e9-137">Specifica lo spazio dei nomi a cui verranno assegnate le regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-137">Specifies the namespace to which the authorization rules will be assigned.</span></span>

<span data-ttu-id="7b4e9-138">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-138">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="7b4e9-139">Le nuove regole devono essere assegnate a uno spazio dei nomi esistente.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-139">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="7b4e9-140">Il cmdlet **New-AzureRmNotificationHubsNamespaceAuthorizationRules** non può creare un nuovo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-140">The **New-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="7b4e9-141">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7b4e9-141">-ResourceGroup</span></span>
<span data-ttu-id="7b4e9-142">Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-142">Specifies the resource group to which the namespace is assigned.</span></span>

<span data-ttu-id="7b4e9-143">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-143">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

<span data-ttu-id="7b4e9-144">Devi usare un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-144">You must use an existing resource group.</span></span>
<span data-ttu-id="7b4e9-145">Questo cmdlet non può creare un nuovo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-145">This cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="7b4e9-146">-SASRule</span><span class="sxs-lookup"><span data-stu-id="7b4e9-146">-SASRule</span></span>
<span data-ttu-id="7b4e9-147">Specifica l'oggetto **SharedAccessAuthorizationRuleAttributes** che contiene le informazioni di configurazione per le nuove regole.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-147">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="7b4e9-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7b4e9-148">-Confirm</span></span>
<span data-ttu-id="7b4e9-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b4e9-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b4e9-150">-WhatIf</span></span>
<span data-ttu-id="7b4e9-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b4e9-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b4e9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b4e9-153">CommonParameters</span></span>
<span data-ttu-id="7b4e9-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b4e9-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b4e9-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b4e9-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b4e9-156">INPUTS</span></span>

### <span data-ttu-id="7b4e9-157">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7b4e9-157">None</span></span>
<span data-ttu-id="7b4e9-158">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7b4e9-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7b4e9-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b4e9-159">OUTPUTS</span></span>

### <span data-ttu-id="7b4e9-160">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7b4e9-160">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="7b4e9-161">Note</span><span class="sxs-lookup"><span data-stu-id="7b4e9-161">NOTES</span></span>

## <span data-ttu-id="7b4e9-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b4e9-162">RELATED LINKS</span></span>

[<span data-ttu-id="7b4e9-163">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="7b4e9-163">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="7b4e9-164">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="7b4e9-164">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="7b4e9-165">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="7b4e9-165">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)



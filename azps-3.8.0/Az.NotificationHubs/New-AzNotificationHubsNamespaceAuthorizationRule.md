---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: eaf34373cb17fea94c498e16f623cef4bf65e937
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020737"
---
# <span data-ttu-id="de2ee-101">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="de2ee-101">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="de2ee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de2ee-102">SYNOPSIS</span></span>
<span data-ttu-id="de2ee-103">Crea una regola di autorizzazione e assegna la regola a uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="de2ee-103">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

## <span data-ttu-id="de2ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de2ee-104">SYNTAX</span></span>

### <span data-ttu-id="de2ee-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="de2ee-105">InputFileParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de2ee-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="de2ee-106">SASRuleParameterSet</span></span>
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de2ee-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de2ee-107">DESCRIPTION</span></span>
<span data-ttu-id="de2ee-108">Il cmdlet **New-AzNotificationHubsNamespaceAuthorizationRule** crea una regola di autorizzazione della firma di accesso condiviso (SAS) e la assegna a uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="de2ee-108">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet creates a Shared Access Signature (SAS) authorization rule and assigns it to a notification hub namespace.</span></span>
<span data-ttu-id="de2ee-109">Le regole di autorizzazione gestiscono i diritti degli utenti allo spazio dei nomi e agli hub di notifica contenuti in tale spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="de2ee-109">Authorization rules manage user rights to the namespace and to the notification hubs contained with that namespace.</span></span>
<span data-ttu-id="de2ee-110">Questo cmdlet offre due modi per creare una nuova regola di autorizzazione e assegnarla a uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="de2ee-110">This cmdlet provides two ways to create a new authorization rule and assign it to a namespace.</span></span>
<span data-ttu-id="de2ee-111">Puoi creare un'istanza dell'oggetto **SharedAccessAuthorizationRuleAttributes** e quindi configurare l'oggetto con i valori della proprietà che vuoi che la nuova regola possieda.</span><span class="sxs-lookup"><span data-stu-id="de2ee-111">You can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the new rule to possess.</span></span>
<span data-ttu-id="de2ee-112">Questa operazione può essere eseguita usando .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="de2ee-112">This can be done using .NET Framework.</span></span>
<span data-ttu-id="de2ee-113">Puoi quindi copiare questi valori di proprietà nella nuova regola usando il parametro *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="de2ee-113">You can then copy those property values to your new rule by using *SASRule* parameter.</span></span>
<span data-ttu-id="de2ee-114">In alternativa, puoi creare un file JSON (JavaScript Object Notation) che contiene i valori di configurazione rilevanti e quindi applicare tali valori usando il parametro *inputfile* .</span><span class="sxs-lookup"><span data-stu-id="de2ee-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="de2ee-115">Un file JSON è un file di testo che usa una sintassi simile alla seguente: {</span><span class="sxs-lookup"><span data-stu-id="de2ee-115">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="de2ee-116">"Nome": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="de2ee-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="de2ee-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",</span><span class="sxs-lookup"><span data-stu-id="de2ee-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="de2ee-118">"Diritti": \[</span><span class="sxs-lookup"><span data-stu-id="de2ee-118">"Rights": \[</span></span>  
        <span data-ttu-id="de2ee-119">"Ascolta",</span><span class="sxs-lookup"><span data-stu-id="de2ee-119">"Listen",</span></span>  
        <span data-ttu-id="de2ee-120">Inviare</span><span class="sxs-lookup"><span data-stu-id="de2ee-120">"Send"</span></span>  
    \]  
<span data-ttu-id="de2ee-121">} Se usato insieme al cmdlet **New-AzNotificationHubsNamespaceAuthorizationRule** , l'esempio JSON precedente crea una regola di autorizzazione denominata ContosoAuthorizationRule che consente agli utenti di ascoltare e inviare diritti allo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="de2ee-121">} When used in conjunction with the **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample creates an authorization rule named ContosoAuthorizationRule that gives users Listen and Send rights to the namespace.</span></span>
<span data-ttu-id="de2ee-122">Il *PrimaryKey* usato per l'autenticazione può essere generato in modo casuale tramite il comando di Windows PowerShell seguente: \[ Convert \] :: ToBase64String ((1.. 32 |% { \[ byte/] (Get-Random-Minimum 0-Maximum 255)}))</span><span class="sxs-lookup"><span data-stu-id="de2ee-122">The *PrimaryKey* that is used for authentication, can be randomly generated by using the following Windows PowerShell command: \[Convert\]::ToBase64String((1..32 |% { \[byte/](Get-Random -Minimum 0 -Maximum 255) }))</span></span>

## <span data-ttu-id="de2ee-123">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de2ee-123">EXAMPLES</span></span>

### <span data-ttu-id="de2ee-124">Esempio 1: creare una regola di autorizzazione e assegnarla a uno spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="de2ee-124">Example 1: Create an authorization rule and assign it to a namespace</span></span>
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

<span data-ttu-id="de2ee-125">Questo comando crea una regola di autorizzazione e assegna la regola allo spazio dei nomi ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="de2ee-125">This command creates an authorization rule and assigns that rule to the namespace ContosoNamespace.</span></span>
<span data-ttu-id="de2ee-126">Quando si crea questa regola è necessario specificare lo spazio dei nomi appropriato e il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="de2ee-126">When creating this rule you must specify the appropriate namespace and the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="de2ee-127">Tuttavia, non è necessario specificare alcuna informazione sulla regola stessa: le informazioni sulle regole verranno ricavate dal file di input C:\Configuration\NamespaceAuthorizationRules.jsattivato.</span><span class="sxs-lookup"><span data-stu-id="de2ee-127">However, you do not need to specify any information about the rule itself: rule information will be taken from the input file C:\Configuration\NamespaceAuthorizationRules.json.</span></span>

## <span data-ttu-id="de2ee-128">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de2ee-128">PARAMETERS</span></span>

### <span data-ttu-id="de2ee-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de2ee-129">-DefaultProfile</span></span>
<span data-ttu-id="de2ee-130">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="de2ee-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de2ee-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="de2ee-131">-InputFile</span></span>
<span data-ttu-id="de2ee-132">Specifica il percorso di un file JSON contenente le informazioni di configurazione per la nuova regola di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="de2ee-132">Specifies the path to a JSON file containing configuration information for the new authorization rule.</span></span>

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

### <span data-ttu-id="de2ee-133">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="de2ee-133">-Namespace</span></span>
<span data-ttu-id="de2ee-134">Specifica lo spazio dei nomi a cui verranno assegnate le regole di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="de2ee-134">Specifies the namespace to which the authorization rules will be assigned.</span></span>
<span data-ttu-id="de2ee-135">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="de2ee-135">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="de2ee-136">Le nuove regole devono essere assegnate a uno spazio dei nomi esistente.</span><span class="sxs-lookup"><span data-stu-id="de2ee-136">The new rules must be assigned to an existing namespace.</span></span>
<span data-ttu-id="de2ee-137">Il cmdlet **New-AzNotificationHubsNamespaceAuthorizationRule** non può creare un nuovo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="de2ee-137">The **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="de2ee-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="de2ee-138">-ResourceGroup</span></span>
<span data-ttu-id="de2ee-139">Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="de2ee-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="de2ee-140">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="de2ee-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="de2ee-141">Devi usare un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="de2ee-141">You must use an existing resource group.</span></span>
<span data-ttu-id="de2ee-142">Questo cmdlet non può creare un nuovo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="de2ee-142">This cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="de2ee-143">-SASRule</span><span class="sxs-lookup"><span data-stu-id="de2ee-143">-SASRule</span></span>
<span data-ttu-id="de2ee-144">Specifica l'oggetto **SharedAccessAuthorizationRuleAttributes** che contiene le informazioni di configurazione per le nuove regole.</span><span class="sxs-lookup"><span data-stu-id="de2ee-144">Specifies the **SharedAccessAuthorizationRuleAttributes** object containing configuration information for the new rules.</span></span>

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

### <span data-ttu-id="de2ee-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="de2ee-145">-Confirm</span></span>
<span data-ttu-id="de2ee-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de2ee-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de2ee-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de2ee-147">-WhatIf</span></span>
<span data-ttu-id="de2ee-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de2ee-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de2ee-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de2ee-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de2ee-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de2ee-150">CommonParameters</span></span>
<span data-ttu-id="de2ee-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de2ee-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de2ee-152">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de2ee-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de2ee-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de2ee-153">INPUTS</span></span>

### <span data-ttu-id="de2ee-154">System. String</span><span class="sxs-lookup"><span data-stu-id="de2ee-154">System.String</span></span>

## <span data-ttu-id="de2ee-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de2ee-155">OUTPUTS</span></span>

### <span data-ttu-id="de2ee-156">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="de2ee-156">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="de2ee-157">Note</span><span class="sxs-lookup"><span data-stu-id="de2ee-157">NOTES</span></span>

## <span data-ttu-id="de2ee-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de2ee-158">RELATED LINKS</span></span>

[<span data-ttu-id="de2ee-159">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="de2ee-159">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="de2ee-160">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="de2ee-160">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="de2ee-161">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="de2ee-161">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)



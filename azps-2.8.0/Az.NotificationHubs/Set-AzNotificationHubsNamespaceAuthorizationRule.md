---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F0981A7A-1B17-4141-A267-927E5B78BE5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 5fb832a7a72f0b201ea20660a5e94e67d470ba95
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855534"
---
# <span data-ttu-id="cad63-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cad63-101">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="cad63-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cad63-102">SYNOPSIS</span></span>
<span data-ttu-id="cad63-103">Imposta le regole di autorizzazione per uno spazio dei nomi Hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="cad63-103">Sets authorization rules for a notification hub namespace.</span></span>

## <span data-ttu-id="cad63-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cad63-104">SYNTAX</span></span>

### <span data-ttu-id="cad63-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="cad63-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cad63-106">SASRuleParameterSet</span><span class="sxs-lookup"><span data-stu-id="cad63-106">SASRuleParameterSet</span></span>
```
Set-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cad63-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cad63-107">DESCRIPTION</span></span>
<span data-ttu-id="cad63-108">Il cmdlet **set-AzNotificationHubsNamespaceAuthorizationRule** modifica una regola di autorizzazione della firma di accesso condiviso (SAS) assegnata a uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="cad63-108">The **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet modifies a Shared Access Signature (SAS) authorization rule assigned to a notification hub namespace.</span></span>
<span data-ttu-id="cad63-109">Le regole di autorizzazione gestiscono i diritti degli utenti allo spazio dei nomi e agli hub di notifica contenuti nello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="cad63-109">Authorization rules manage user rights to the namespace and to the notification hubs contained in that namespace.</span></span>
<span data-ttu-id="cad63-110">Questo cmdlet offre due modi per modificare una regola di autorizzazione assegnata a uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="cad63-110">This cmdlet provides two ways to modify an authorization rule assigned to a namespace.</span></span>
<span data-ttu-id="cad63-111">Per uno, puoi creare un'istanza dell'oggetto **SharedAccessAuthorizationRuleAttributes** e quindi configurare l'oggetto con i valori della proprietà che vuoi che la regola possieda.</span><span class="sxs-lookup"><span data-stu-id="cad63-111">For one, you can create an instance of the **SharedAccessAuthorizationRuleAttributes** object and then configure that object with the property values you want the rule to possess.</span></span>
<span data-ttu-id="cad63-112">Puoi usare .NET Framework per eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="cad63-112">You can use the .NET Framework to accomplish this.</span></span>
<span data-ttu-id="cad63-113">Puoi quindi copiare questi valori della proprietà nella regola tramite il parametro *SASRule* .</span><span class="sxs-lookup"><span data-stu-id="cad63-113">You can then copy those property values to the rule through the *SASRule* parameter.</span></span>
<span data-ttu-id="cad63-114">In alternativa, puoi creare un file JSON (JavaScript Object Notation) contenente i valori di configurazione rilevanti e quindi applicare tali valori tramite il parametro *inputfile* .</span><span class="sxs-lookup"><span data-stu-id="cad63-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and then apply those values through the *InputFile* parameter.</span></span>
<span data-ttu-id="cad63-115">Un file JSON è un file di testo che usa una sintassi simile alla seguente: {</span><span class="sxs-lookup"><span data-stu-id="cad63-115">A JSON file is a text file that uses syntax similar to this: {</span></span>  
    <span data-ttu-id="cad63-116">"Nome": "ContosoAuthorizationRule",</span><span class="sxs-lookup"><span data-stu-id="cad63-116">"Name": "ContosoAuthorizationRule",</span></span>  
    <span data-ttu-id="cad63-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",</span><span class="sxs-lookup"><span data-stu-id="cad63-117">"PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",</span></span>  
    <span data-ttu-id="cad63-118">"Diritti": \[</span><span class="sxs-lookup"><span data-stu-id="cad63-118">"Rights": \[</span></span>  
        <span data-ttu-id="cad63-119">"Ascolta",</span><span class="sxs-lookup"><span data-stu-id="cad63-119">"Listen",</span></span>  
        <span data-ttu-id="cad63-120">Inviare</span><span class="sxs-lookup"><span data-stu-id="cad63-120">"Send"</span></span>  
    \]  
<span data-ttu-id="cad63-121">} Se usato insieme al cmdlet **set-AzNotificationHubsNamespaceAuthorizationRule** , l'esempio JSON precedente modifica una regola di autorizzazione denominata ContosoAuthorizationRule per consentire agli utenti di ascoltare e inviare diritti allo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="cad63-121">} When used in conjunction with the **Set-AzNotificationHubsNamespaceAuthorizationRule** cmdlet, the preceding JSON sample modifies an authorization rule named ContosoAuthorizationRule to give users Listen and Send rights to the namespace.</span></span>

## <span data-ttu-id="cad63-122">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cad63-122">EXAMPLES</span></span>

### <span data-ttu-id="cad63-123">Esempio 1: modificare una regola di autorizzazione assegnata a uno spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cad63-123">Example 1: Modify an authorization rule assigned to a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationGroup" -InputFile "C:\Configuration\AuthorizationRules.json"
```

<span data-ttu-id="cad63-124">Questo comando consente di modificare una regola di autorizzazione assegnata allo spazio dei nomi denominato ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="cad63-124">This command modifies an authorization rule assigned to the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="cad63-125">Devi specificare il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="cad63-125">You must specify the resource group that the namespace is assigned to.</span></span>
<span data-ttu-id="cad63-126">Le informazioni sulla regola di autorizzazione non sono incluse nel comando stesso.</span><span class="sxs-lookup"><span data-stu-id="cad63-126">Information about the authorization rule is not included in the command itself.</span></span>
<span data-ttu-id="cad63-127">Queste informazioni vengono invece ottenute dal file di input C:\Configuration\AuthorizationRules.jsattivato.</span><span class="sxs-lookup"><span data-stu-id="cad63-127">Instead, that information is obtained from the input file C:\Configuration\AuthorizationRules.json.</span></span>

## <span data-ttu-id="cad63-128">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cad63-128">PARAMETERS</span></span>

### <span data-ttu-id="cad63-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cad63-129">-DefaultProfile</span></span>
<span data-ttu-id="cad63-130">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cad63-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cad63-131">-Force</span><span class="sxs-lookup"><span data-stu-id="cad63-131">-Force</span></span>
<span data-ttu-id="cad63-132">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="cad63-132">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cad63-133">-InputFile</span><span class="sxs-lookup"><span data-stu-id="cad63-133">-InputFile</span></span>
<span data-ttu-id="cad63-134">Specifica il percorso di un file JSON contenente le informazioni di configurazione per la nuova regola.</span><span class="sxs-lookup"><span data-stu-id="cad63-134">Specifies the path to a JSON file containing configuration information for the new rule.</span></span>

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

### <span data-ttu-id="cad63-135">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cad63-135">-Namespace</span></span>
<span data-ttu-id="cad63-136">Specifica lo spazio dei nomi che contiene le regole di autorizzazione modificate da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cad63-136">Specifies the namespace that contains the authorization rules that this cmdlet modifies.</span></span>
<span data-ttu-id="cad63-137">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="cad63-137">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="cad63-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cad63-138">-ResourceGroup</span></span>
<span data-ttu-id="cad63-139">Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="cad63-139">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="cad63-140">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="cad63-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="cad63-141">-SASRule</span><span class="sxs-lookup"><span data-stu-id="cad63-141">-SASRule</span></span>
<span data-ttu-id="cad63-142">Specifica l'oggetto **SharedAccessAuthorizationRuleAttributes** che contiene le informazioni di configurazione per le regole di autorizzazione modificate dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cad63-142">Specifies the **SharedAccessAuthorizationRuleAttributes** object that contains configuration information for the authorization rules that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cad63-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cad63-143">-Confirm</span></span>
<span data-ttu-id="cad63-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cad63-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cad63-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cad63-145">-WhatIf</span></span>
<span data-ttu-id="cad63-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cad63-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cad63-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cad63-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cad63-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cad63-148">CommonParameters</span></span>
<span data-ttu-id="cad63-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cad63-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cad63-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cad63-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cad63-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cad63-151">INPUTS</span></span>

### <span data-ttu-id="cad63-152">System. String</span><span class="sxs-lookup"><span data-stu-id="cad63-152">System.String</span></span>

## <span data-ttu-id="cad63-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cad63-153">OUTPUTS</span></span>

### <span data-ttu-id="cad63-154">Microsoft. Azure. Commands. NotificationHubs. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="cad63-154">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="cad63-155">Note</span><span class="sxs-lookup"><span data-stu-id="cad63-155">NOTES</span></span>

## <span data-ttu-id="cad63-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cad63-156">RELATED LINKS</span></span>

[<span data-ttu-id="cad63-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cad63-157">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="cad63-158">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cad63-158">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="cad63-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cad63-159">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Remove-AzNotificationHubsNamespaceAuthorizationRule.md)



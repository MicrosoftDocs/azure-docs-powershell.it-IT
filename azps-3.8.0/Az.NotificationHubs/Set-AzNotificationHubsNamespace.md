---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: c367c4b4f7ebe7c9d6d51b832eed22249f262864
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020721"
---
# <span data-ttu-id="43ebb-101">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="43ebb-101">Set-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="43ebb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43ebb-102">SYNOPSIS</span></span>
<span data-ttu-id="43ebb-103">Imposta i valori delle proprietà per uno spazio dei nomi Hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="43ebb-103">Sets property values for a notification hub namespace.</span></span>

## <span data-ttu-id="43ebb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43ebb-104">SYNTAX</span></span>

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43ebb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43ebb-105">DESCRIPTION</span></span>
<span data-ttu-id="43ebb-106">Il cmdlet **set-AzNotificationHubsNamespace** imposta i valori delle proprietà di uno spazio dei nomi esistente dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="43ebb-106">The **Set-AzNotificationHubsNamespace** cmdlet sets the property values of an existing notification hub namespace.</span></span>
<span data-ttu-id="43ebb-107">Gli spazi dei nomi sono contenitori logici che consentono di organizzare e gestire gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="43ebb-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="43ebb-108">È necessario avere almeno uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="43ebb-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="43ebb-109">Inoltre, tutti gli hub di notifica devono avere uno spazio dei nomi assegnato.</span><span class="sxs-lookup"><span data-stu-id="43ebb-109">Additionally, all notification hubs must have an assigned namespace.</span></span>
<span data-ttu-id="43ebb-110">Questo cmdlet viene usato principalmente per abilitare e disabilitare uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="43ebb-110">This cmdlet is primarily used to enable and disable a namespace.</span></span>
<span data-ttu-id="43ebb-111">Quando uno spazio dei nomi è disabilitato, gli utenti non possono connettersi agli hub di notifica nello spazio dei nomi, né possono usare questi hub per inviare notifiche push.</span><span class="sxs-lookup"><span data-stu-id="43ebb-111">When a namespace is disabled, users cannot connect to any of the notification hubs in the namespace, nor can administrators use those hubs to send push notifications.</span></span>
<span data-ttu-id="43ebb-112">Per riabilitare uno spazio dei nomi disabilitato, usa questo cmdlet per impostare la proprietà **state** dello spazio dei nomi su Active.</span><span class="sxs-lookup"><span data-stu-id="43ebb-112">To re-enable a disabled namespace, use this cmdlet to set the **State** property of the namespace to Active.</span></span>
<span data-ttu-id="43ebb-113">Puoi anche usare questo cmdlet per contrassegnare uno spazio dei nomi come critico.</span><span class="sxs-lookup"><span data-stu-id="43ebb-113">You can also use this cmdlet to tag a namespace as critical.</span></span>
<span data-ttu-id="43ebb-114">In questo modo viene impedito l'eliminazione dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="43ebb-114">This prevents the namespace from being deleted.</span></span>
<span data-ttu-id="43ebb-115">Per rimuovere uno spazio dei nomi critico, devi prima rimuovere il tag critical.</span><span class="sxs-lookup"><span data-stu-id="43ebb-115">To remove a critical namespace you must first remove the Critical tag.</span></span>

## <span data-ttu-id="43ebb-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43ebb-116">EXAMPLES</span></span>

### <span data-ttu-id="43ebb-117">Esempio 1: disabilitare uno spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="43ebb-117">Example 1: Disable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

<span data-ttu-id="43ebb-118">Questo comando Disabilita lo spazio dei nomi denominato ContosoPartners situato nel Data Center ovest degli Stati Uniti e assegnato al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="43ebb-118">This command disables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="43ebb-119">Esempio 2: abilitare uno spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="43ebb-119">Example 2: Enable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

<span data-ttu-id="43ebb-120">Questo comando consente allo spazio dei nomi denominato ContosoPartners situato nel Data Center ovest degli Stati Uniti e assegnato al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="43ebb-120">This command enables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

## <span data-ttu-id="43ebb-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43ebb-121">PARAMETERS</span></span>

### <span data-ttu-id="43ebb-122">-Critical</span><span class="sxs-lookup"><span data-stu-id="43ebb-122">-Critical</span></span>
<span data-ttu-id="43ebb-123">Indica se lo spazio dei nomi è uno spazio dei nomi critico.</span><span class="sxs-lookup"><span data-stu-id="43ebb-123">Indicates whether the namespace is a critical namespace.</span></span>
<span data-ttu-id="43ebb-124">Gli spazi dei nomi critici non possono essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="43ebb-124">Critical namespaces cannot be deleted.</span></span>
<span data-ttu-id="43ebb-125">Per eliminare uno spazio dei nomi critico, è necessario impostare il valore di questa proprietà su false per contrassegnare lo spazio dei nomi come non critico.</span><span class="sxs-lookup"><span data-stu-id="43ebb-125">To delete a critical namespace, you must set the value of this property to False in order to mark the namespace as non-critical.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ebb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43ebb-126">-DefaultProfile</span></span>
<span data-ttu-id="43ebb-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="43ebb-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43ebb-128">-Force</span><span class="sxs-lookup"><span data-stu-id="43ebb-128">-Force</span></span>
<span data-ttu-id="43ebb-129">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="43ebb-129">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="43ebb-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="43ebb-130">-Location</span></span>
<span data-ttu-id="43ebb-131">Specifica il nome visualizzato del centro dati che ospita lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="43ebb-131">Specifies the display name of the datacenter that hosts the namespace.</span></span>
<span data-ttu-id="43ebb-132">Anche se è possibile impostare questo parametro su qualsiasi posizione di Azure valida, per ottenere prestazioni ottimali, è consigliabile usare un data center situato vicino alla maggior parte degli utenti.</span><span class="sxs-lookup"><span data-stu-id="43ebb-132">Although you can set this parameter to any valid Azure location, for optimal performance you should use a datacenter located near the majority of your users.</span></span>
<span data-ttu-id="43ebb-133">Per ottenere un elenco aggiornato delle posizioni di Azure, eseguire il comando seguente: `Get-AzLocation | Select-Object DisplayName`</span><span class="sxs-lookup"><span data-stu-id="43ebb-133">To get an up-to-date list of Azure locations run the following command: `Get-AzLocation | Select-Object DisplayName`</span></span>

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

### <span data-ttu-id="43ebb-134">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="43ebb-134">-Namespace</span></span>
<span data-ttu-id="43ebb-135">Specifica lo spazio dei nomi modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43ebb-135">Specifies the namespace that this cmdlet modifies.</span></span>
<span data-ttu-id="43ebb-136">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="43ebb-136">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="43ebb-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="43ebb-137">-ResourceGroup</span></span>
<span data-ttu-id="43ebb-138">Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="43ebb-138">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="43ebb-139">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="43ebb-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="43ebb-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="43ebb-140">-SkuTier</span></span>
<span data-ttu-id="43ebb-141">Livello SKU dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="43ebb-141">Sku tier of the namespace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ebb-142">-Stato</span><span class="sxs-lookup"><span data-stu-id="43ebb-142">-State</span></span>
<span data-ttu-id="43ebb-143">Specifica lo stato corrente dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="43ebb-143">Specifies the current state of the namespace.</span></span>
<span data-ttu-id="43ebb-144">I valori accettabili per questo parametro sono: Active e disabled.</span><span class="sxs-lookup"><span data-stu-id="43ebb-144">The acceptable values for this parameter are: Active and Disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ebb-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="43ebb-145">-Tag</span></span>
<span data-ttu-id="43ebb-146">Specifica le coppie nome/valore che possono essere usate per categorizzare e organizzare gli elementi Azure.</span><span class="sxs-lookup"><span data-stu-id="43ebb-146">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="43ebb-147">I tag funzionano in modo simile alle parole chiave e funzionano in una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="43ebb-147">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="43ebb-148">Ad esempio, se si cercano tutti gli elementi con il reparto Tag: la ricerca restituirà tutti gli elementi di Azure che hanno il tag, indipendentemente da oggetti come il tipo di elemento, la posizione o il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="43ebb-148">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="43ebb-149">Un singolo tag è costituito da due parti: il *nome* e (facoltativamente) il *valore*.</span><span class="sxs-lookup"><span data-stu-id="43ebb-149">An individual tag consists of two parts: the *Name* and (optionally) the *Value*.</span></span>
<span data-ttu-id="43ebb-150">Ad esempio, nel reparto: il nome del tag è reparto e il valore di tag è.</span><span class="sxs-lookup"><span data-stu-id="43ebb-150">For example, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="43ebb-151">Per aggiungere un tag, usa la sintassi della tabella hash simile alla seguente, che crea il tag CalendarYear: 2016:-Tags @ {Name = "CalendarYear"; Value = "2016"} per aggiungere più tag nello stesso comando, separare i singoli tag usando le virgole:-Tag @ {Name = "CalendarYear"; Value = "2016"}, @ {Name = "anno fiscale"; Value = "2017"}</span><span class="sxs-lookup"><span data-stu-id="43ebb-151">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016: -Tags @{Name="CalendarYear";Value="2016"} To add multiple tags in the same command, separate the individual tags by using commas: -Tag @{Name="CalendarYear";Value="2016"}, @{Name="FiscalYear";Value="2017"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43ebb-152">-Confermare</span><span class="sxs-lookup"><span data-stu-id="43ebb-152">-Confirm</span></span>
<span data-ttu-id="43ebb-153">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43ebb-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43ebb-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43ebb-154">-WhatIf</span></span>
<span data-ttu-id="43ebb-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43ebb-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43ebb-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43ebb-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43ebb-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43ebb-157">CommonParameters</span></span>
<span data-ttu-id="43ebb-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43ebb-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43ebb-159">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43ebb-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43ebb-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43ebb-160">INPUTS</span></span>

### <span data-ttu-id="43ebb-161">System. String</span><span class="sxs-lookup"><span data-stu-id="43ebb-161">System.String</span></span>

### <span data-ttu-id="43ebb-162">Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceState</span><span class="sxs-lookup"><span data-stu-id="43ebb-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span></span>

### <span data-ttu-id="43ebb-163">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43ebb-163">System.Boolean</span></span>

### <span data-ttu-id="43ebb-164">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="43ebb-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="43ebb-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43ebb-165">OUTPUTS</span></span>

### <span data-ttu-id="43ebb-166">Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="43ebb-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="43ebb-167">Note</span><span class="sxs-lookup"><span data-stu-id="43ebb-167">NOTES</span></span>

## <span data-ttu-id="43ebb-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43ebb-168">RELATED LINKS</span></span>

[<span data-ttu-id="43ebb-169">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="43ebb-169">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="43ebb-170">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="43ebb-170">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="43ebb-171">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="43ebb-171">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)



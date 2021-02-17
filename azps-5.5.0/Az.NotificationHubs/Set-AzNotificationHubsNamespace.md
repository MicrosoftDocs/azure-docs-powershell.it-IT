---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: c367c4b4f7ebe7c9d6d51b832eed22249f262864
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191487"
---
# <span data-ttu-id="e4bc1-101">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="e4bc1-101">Set-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="e4bc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4bc1-102">SYNOPSIS</span></span>
<span data-ttu-id="e4bc1-103">Imposta i valori delle proprietà per uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-103">Sets property values for a notification hub namespace.</span></span>

## <span data-ttu-id="e4bc1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4bc1-104">SYNTAX</span></span>

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4bc1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e4bc1-105">DESCRIPTION</span></span>
<span data-ttu-id="e4bc1-106">Il cmdlet **Set-AzNotificationHubs Consente di impostare** i valori delle proprietà di uno spazio dei nomi dell'hub di notifica esistente.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-106">The **Set-AzNotificationHubsNamespace** cmdlet sets the property values of an existing notification hub namespace.</span></span>
<span data-ttu-id="e4bc1-107">Gli spazi dei nomi sono contenitori logici che consentono di organizzare e gestire gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="e4bc1-108">È necessario avere almeno uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="e4bc1-109">Inoltre, tutti gli hub di notifica devono avere uno spazio dei nomi assegnato.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-109">Additionally, all notification hubs must have an assigned namespace.</span></span>
<span data-ttu-id="e4bc1-110">Questo cmdlet viene usato principalmente per abilitare e disabilitare uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-110">This cmdlet is primarily used to enable and disable a namespace.</span></span>
<span data-ttu-id="e4bc1-111">Quando uno spazio dei nomi è disabilitato, gli utenti non possono connettersi a nessuno degli hub di notifica nello spazio dei nomi, né gli amministratori possono usare questi hub per inviare notifiche push.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-111">When a namespace is disabled, users cannot connect to any of the notification hubs in the namespace, nor can administrators use those hubs to send push notifications.</span></span>
<span data-ttu-id="e4bc1-112">Per abilitare nuovamente uno spazio dei nomi disabilitato, usare questo cmdlet per impostare la **proprietà Stato** dello spazio dei nomi su Attivo.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-112">To re-enable a disabled namespace, use this cmdlet to set the **State** property of the namespace to Active.</span></span>
<span data-ttu-id="e4bc1-113">È anche possibile usare questo cmdlet per contrassegnare uno spazio dei nomi come critico.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-113">You can also use this cmdlet to tag a namespace as critical.</span></span>
<span data-ttu-id="e4bc1-114">In questo modo si impedisce l'eliminazione dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-114">This prevents the namespace from being deleted.</span></span>
<span data-ttu-id="e4bc1-115">Per rimuovere uno spazio dei nomi critico, è necessario rimuovere prima il tag critico.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-115">To remove a critical namespace you must first remove the Critical tag.</span></span>

## <span data-ttu-id="e4bc1-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4bc1-116">EXAMPLES</span></span>

### <span data-ttu-id="e4bc1-117">Esempio 1: Disabilitare uno spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e4bc1-117">Example 1: Disable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

<span data-ttu-id="e4bc1-118">Questo comando disabilita lo spazio dei nomi denominato ContosoPartners, situato nel data center degli Stati Uniti occidentali, e assegnato al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-118">This command disables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="e4bc1-119">Esempio 2: Abilitare uno spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e4bc1-119">Example 2: Enable a namespace</span></span>
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

<span data-ttu-id="e4bc1-120">Questo comando abilita lo spazio dei nomi denominato ContosoPartners che si trova nel data center Degli Stati Uniti occidentale e assegnato al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-120">This command enables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

## <span data-ttu-id="e4bc1-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4bc1-121">PARAMETERS</span></span>

### <span data-ttu-id="e4bc1-122">-Critico</span><span class="sxs-lookup"><span data-stu-id="e4bc1-122">-Critical</span></span>
<span data-ttu-id="e4bc1-123">Indica se lo spazio dei nomi è uno spazio dei nomi critico.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-123">Indicates whether the namespace is a critical namespace.</span></span>
<span data-ttu-id="e4bc1-124">Gli spazi dei nomi critici non possono essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-124">Critical namespaces cannot be deleted.</span></span>
<span data-ttu-id="e4bc1-125">Per eliminare uno spazio dei nomi critico, è necessario impostare il valore di questa proprietà su False per contrassegnare lo spazio dei nomi come non critico.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-125">To delete a critical namespace, you must set the value of this property to False in order to mark the namespace as non-critical.</span></span>

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

### <span data-ttu-id="e4bc1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4bc1-126">-DefaultProfile</span></span>
<span data-ttu-id="e4bc1-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e4bc1-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4bc1-128">-Force</span><span class="sxs-lookup"><span data-stu-id="e4bc1-128">-Force</span></span>
<span data-ttu-id="e4bc1-129">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-129">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e4bc1-130">-Location</span><span class="sxs-lookup"><span data-stu-id="e4bc1-130">-Location</span></span>
<span data-ttu-id="e4bc1-131">Specifica il nome visualizzato del data center che ospita lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-131">Specifies the display name of the datacenter that hosts the namespace.</span></span>
<span data-ttu-id="e4bc1-132">Anche se è possibile impostare questo parametro su qualsiasi posizione di Azure valida, per ottenere prestazioni ottimali è consigliabile usare un data center situato vicino alla maggior parte degli utenti.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-132">Although you can set this parameter to any valid Azure location, for optimal performance you should use a datacenter located near the majority of your users.</span></span>
<span data-ttu-id="e4bc1-133">Per ottenere un elenco aggiornato delle posizioni di Azure, eseguire il comando seguente: `Get-AzLocation | Select-Object DisplayName`</span><span class="sxs-lookup"><span data-stu-id="e4bc1-133">To get an up-to-date list of Azure locations run the following command: `Get-AzLocation | Select-Object DisplayName`</span></span>

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

### <span data-ttu-id="e4bc1-134">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e4bc1-134">-Namespace</span></span>
<span data-ttu-id="e4bc1-135">Specifica lo spazio dei nomi modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-135">Specifies the namespace that this cmdlet modifies.</span></span>
<span data-ttu-id="e4bc1-136">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-136">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="e4bc1-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e4bc1-137">-ResourceGroup</span></span>
<span data-ttu-id="e4bc1-138">Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-138">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="e4bc1-139">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che consentono semplicemente la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="e4bc1-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="e4bc1-140">-SkuTier</span></span>
<span data-ttu-id="e4bc1-141">Livello SKU dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e4bc1-141">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="e4bc1-142">-State</span><span class="sxs-lookup"><span data-stu-id="e4bc1-142">-State</span></span>
<span data-ttu-id="e4bc1-143">Specifica lo stato corrente dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-143">Specifies the current state of the namespace.</span></span>
<span data-ttu-id="e4bc1-144">I valori accettabili per questo parametro sono: Attivo e Disabilitato.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-144">The acceptable values for this parameter are: Active and Disabled.</span></span>

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

### <span data-ttu-id="e4bc1-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="e4bc1-145">-Tag</span></span>
<span data-ttu-id="e4bc1-146">Specifica coppie nome-valore che possono essere usate per categorizzare e organizzare gli elementi di Azure.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-146">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="e4bc1-147">I tag funzionano in modo simile alle parole chiave e operano in una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-147">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="e4bc1-148">Ad esempio, se si ricercano tutti gli elementi con il tag Department:IT, la ricerca restituirà tutti gli elementi azure che hanno quel tag, indipendentemente dal tipo di elemento, dalla posizione o dal gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-148">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="e4bc1-149">Un singolo tag è costituito da due parti: *Name e,* facoltativamente, *value.*</span><span class="sxs-lookup"><span data-stu-id="e4bc1-149">An individual tag consists of two parts: the *Name* and (optionally) the *Value*.</span></span>
<span data-ttu-id="e4bc1-150">Ad esempio, in Department:IT il nome del tag è Department e il valore del tag è IT.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-150">For example, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="e4bc1-151">Per aggiungere un tag, usare una sintassi della tabella hash simile alla seguente, che crea il tag CalendarYear:2016: -Tag @{Name="CalendarYear"; Value="2016"} Per aggiungere più tag nello stesso comando, separare i singoli tag con una virgola: -Tag @{Name="CalendarYear"; Value="2016"}, @{Name="FiscalYear"; Value="2017"}</span><span class="sxs-lookup"><span data-stu-id="e4bc1-151">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016: -Tags @{Name="CalendarYear";Value="2016"} To add multiple tags in the same command, separate the individual tags by using commas: -Tag @{Name="CalendarYear";Value="2016"}, @{Name="FiscalYear";Value="2017"}</span></span>

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

### <span data-ttu-id="e4bc1-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4bc1-152">-Confirm</span></span>
<span data-ttu-id="e4bc1-153">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4bc1-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4bc1-154">-WhatIf</span></span>
<span data-ttu-id="e4bc1-155">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4bc1-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4bc1-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4bc1-157">CommonParameters</span></span>
<span data-ttu-id="e4bc1-158">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4bc1-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4bc1-159">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4bc1-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4bc1-160">INPUT</span><span class="sxs-lookup"><span data-stu-id="e4bc1-160">INPUTS</span></span>

### <span data-ttu-id="e4bc1-161">System.String</span><span class="sxs-lookup"><span data-stu-id="e4bc1-161">System.String</span></span>

### <span data-ttu-id="e4bc1-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span><span class="sxs-lookup"><span data-stu-id="e4bc1-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span></span>

### <span data-ttu-id="e4bc1-163">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e4bc1-163">System.Boolean</span></span>

### <span data-ttu-id="e4bc1-164">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e4bc1-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e4bc1-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4bc1-165">OUTPUTS</span></span>

### <span data-ttu-id="e4bc1-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e4bc1-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="e4bc1-167">NOTE</span><span class="sxs-lookup"><span data-stu-id="e4bc1-167">NOTES</span></span>

## <span data-ttu-id="e4bc1-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4bc1-168">RELATED LINKS</span></span>

[<span data-ttu-id="e4bc1-169">Get-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="e4bc1-169">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="e4bc1-170">New-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="e4bc1-170">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="e4bc1-171">Remove-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="e4bc1-171">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)



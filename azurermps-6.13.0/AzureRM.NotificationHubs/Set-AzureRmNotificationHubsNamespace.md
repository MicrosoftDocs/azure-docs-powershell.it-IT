---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 2fb349628a686bb96df5685bff8a4329c0173212
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514971"
---
# <span data-ttu-id="db9e6-101">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="db9e6-101">Set-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="db9e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db9e6-102">SYNOPSIS</span></span>
<span data-ttu-id="db9e6-103">Imposta i valori delle proprietà per uno spazio dei nomi Hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="db9e6-103">Sets property values for a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db9e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db9e6-104">SYNTAX</span></span>

```
Set-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db9e6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db9e6-105">DESCRIPTION</span></span>
<span data-ttu-id="db9e6-106">Il cmdlet **set-AzureRmNotificationHubsNamespace** imposta i valori delle proprietà di uno spazio dei nomi esistente dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="db9e6-106">The **Set-AzureRmNotificationHubsNamespace** cmdlet sets the property values of an existing notification hub namespace.</span></span>
<span data-ttu-id="db9e6-107">Gli spazi dei nomi sono contenitori logici che consentono di organizzare e gestire gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="db9e6-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="db9e6-108">È necessario avere almeno uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="db9e6-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="db9e6-109">Inoltre, tutti gli hub di notifica devono avere uno spazio dei nomi assegnato.</span><span class="sxs-lookup"><span data-stu-id="db9e6-109">Additionally, all notification hubs must have an assigned namespace.</span></span>
<span data-ttu-id="db9e6-110">Questo cmdlet viene usato principalmente per abilitare e disabilitare uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="db9e6-110">This cmdlet is primarily used to enable and disable a namespace.</span></span>
<span data-ttu-id="db9e6-111">Quando uno spazio dei nomi è disabilitato, gli utenti non possono connettersi agli hub di notifica nello spazio dei nomi, né possono usare questi hub per inviare notifiche push.</span><span class="sxs-lookup"><span data-stu-id="db9e6-111">When a namespace is disabled, users cannot connect to any of the notification hubs in the namespace, nor can administrators use those hubs to send push notifications.</span></span>
<span data-ttu-id="db9e6-112">Per riabilitare uno spazio dei nomi disabilitato, usa questo cmdlet per impostare la proprietà **state** dello spazio dei nomi su Active.</span><span class="sxs-lookup"><span data-stu-id="db9e6-112">To re-enable a disabled namespace, use this cmdlet to set the **State** property of the namespace to Active.</span></span>
<span data-ttu-id="db9e6-113">Puoi anche usare questo cmdlet per contrassegnare uno spazio dei nomi come critico.</span><span class="sxs-lookup"><span data-stu-id="db9e6-113">You can also use this cmdlet to tag a namespace as critical.</span></span>
<span data-ttu-id="db9e6-114">In questo modo viene impedito l'eliminazione dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="db9e6-114">This prevents the namespace from being deleted.</span></span>
<span data-ttu-id="db9e6-115">Per rimuovere uno spazio dei nomi critico, devi prima rimuovere il tag critical.</span><span class="sxs-lookup"><span data-stu-id="db9e6-115">To remove a critical namespace you must first remove the Critical tag.</span></span>

## <span data-ttu-id="db9e6-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db9e6-116">EXAMPLES</span></span>

### <span data-ttu-id="db9e6-117">Esempio 1: disabilitare uno spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="db9e6-117">Example 1: Disable a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

<span data-ttu-id="db9e6-118">Questo comando Disabilita lo spazio dei nomi denominato ContosoPartners situato nel Data Center ovest degli Stati Uniti e assegnato al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="db9e6-118">This command disables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="db9e6-119">Esempio 2: abilitare uno spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="db9e6-119">Example 2: Enable a namespace</span></span>
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

<span data-ttu-id="db9e6-120">Questo comando consente allo spazio dei nomi denominato ContosoPartners situato nel Data Center ovest degli Stati Uniti e assegnato al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="db9e6-120">This command enables the namespace named ContosoPartners located in the West US datacenter and assigned to the ContosoNotificationsGroup resource group.</span></span>

## <span data-ttu-id="db9e6-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db9e6-121">PARAMETERS</span></span>

### <span data-ttu-id="db9e6-122">-Critical</span><span class="sxs-lookup"><span data-stu-id="db9e6-122">-Critical</span></span>
<span data-ttu-id="db9e6-123">Indica se lo spazio dei nomi è uno spazio dei nomi critico.</span><span class="sxs-lookup"><span data-stu-id="db9e6-123">Indicates whether the namespace is a critical namespace.</span></span>
<span data-ttu-id="db9e6-124">Gli spazi dei nomi critici non possono essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="db9e6-124">Critical namespaces cannot be deleted.</span></span>
<span data-ttu-id="db9e6-125">Per eliminare uno spazio dei nomi critico, è necessario impostare il valore di questa proprietà su false per contrassegnare lo spazio dei nomi come non critico.</span><span class="sxs-lookup"><span data-stu-id="db9e6-125">To delete a critical namespace, you must set the value of this property to False in order to mark the namespace as non-critical.</span></span>

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

### <span data-ttu-id="db9e6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db9e6-126">-DefaultProfile</span></span>
<span data-ttu-id="db9e6-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="db9e6-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db9e6-128">-Force</span><span class="sxs-lookup"><span data-stu-id="db9e6-128">-Force</span></span>
<span data-ttu-id="db9e6-129">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="db9e6-129">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="db9e6-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="db9e6-130">-Location</span></span>
<span data-ttu-id="db9e6-131">Specifica il nome visualizzato del centro dati che ospita lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="db9e6-131">Specifies the display name of the datacenter that hosts the namespace.</span></span>
<span data-ttu-id="db9e6-132">Anche se è possibile impostare questo parametro su qualsiasi posizione di Azure valida, per ottenere prestazioni ottimali, è consigliabile usare un data center situato vicino alla maggior parte degli utenti.</span><span class="sxs-lookup"><span data-stu-id="db9e6-132">Although you can set this parameter to any valid Azure location, for optimal performance you should use a datacenter located near the majority of your users.</span></span>
<span data-ttu-id="db9e6-133">Per ottenere un elenco aggiornato delle posizioni di Azure, eseguire il comando seguente: `Get-AzureLocation | Select-Object DisplayName`</span><span class="sxs-lookup"><span data-stu-id="db9e6-133">To get an up-to-date list of Azure locations run the following command: `Get-AzureLocation | Select-Object DisplayName`</span></span>

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

### <span data-ttu-id="db9e6-134">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="db9e6-134">-Namespace</span></span>
<span data-ttu-id="db9e6-135">Specifica lo spazio dei nomi modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db9e6-135">Specifies the namespace that this cmdlet modifies.</span></span>
<span data-ttu-id="db9e6-136">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="db9e6-136">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="db9e6-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="db9e6-137">-ResourceGroup</span></span>
<span data-ttu-id="db9e6-138">Specifica il gruppo di risorse a cui è assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="db9e6-138">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="db9e6-139">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="db9e6-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="db9e6-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="db9e6-140">-SkuTier</span></span>
<span data-ttu-id="db9e6-141">Livello SKU dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="db9e6-141">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="db9e6-142">-Stato</span><span class="sxs-lookup"><span data-stu-id="db9e6-142">-State</span></span>
<span data-ttu-id="db9e6-143">Specifica lo stato corrente dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="db9e6-143">Specifies the current state of the namespace.</span></span>
<span data-ttu-id="db9e6-144">I valori accettabili per questo parametro sono: Active e disabled.</span><span class="sxs-lookup"><span data-stu-id="db9e6-144">The acceptable values for this parameter are: Active and Disabled.</span></span>

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

### <span data-ttu-id="db9e6-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="db9e6-145">-Tag</span></span>
<span data-ttu-id="db9e6-146">Specifica le coppie nome/valore che possono essere usate per categorizzare e organizzare gli elementi Azure.</span><span class="sxs-lookup"><span data-stu-id="db9e6-146">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="db9e6-147">I tag funzionano in modo simile alle parole chiave e funzionano in una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="db9e6-147">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="db9e6-148">Ad esempio, se si cercano tutti gli elementi con il reparto Tag: la ricerca restituirà tutti gli elementi di Azure che hanno il tag, indipendentemente da oggetti come il tipo di elemento, la posizione o il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="db9e6-148">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="db9e6-149">Un singolo tag è costituito da due parti: il *nome* e (facoltativamente) il *valore*.</span><span class="sxs-lookup"><span data-stu-id="db9e6-149">An individual tag consists of two parts: the *Name* and (optionally) the *Value*.</span></span>
<span data-ttu-id="db9e6-150">Ad esempio, nel reparto: il nome del tag è reparto e il valore di tag è.</span><span class="sxs-lookup"><span data-stu-id="db9e6-150">For example, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="db9e6-151">Per aggiungere un tag, usa la sintassi della tabella hash simile alla seguente, che crea il tag CalendarYear: 2016:-Tags @ {Name = "CalendarYear"; Value = "2016"} per aggiungere più tag nello stesso comando, separare i singoli tag usando le virgole:-Tag @ {Name = "CalendarYear"; Value = "2016"}, @ {Name = "anno fiscale"; Value = "2017"}</span><span class="sxs-lookup"><span data-stu-id="db9e6-151">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016: -Tags @{Name="CalendarYear";Value="2016"} To add multiple tags in the same command, separate the individual tags by using commas: -Tag @{Name="CalendarYear";Value="2016"}, @{Name="FiscalYear";Value="2017"}</span></span>

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

### <span data-ttu-id="db9e6-152">-Confermare</span><span class="sxs-lookup"><span data-stu-id="db9e6-152">-Confirm</span></span>
<span data-ttu-id="db9e6-153">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db9e6-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db9e6-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db9e6-154">-WhatIf</span></span>
<span data-ttu-id="db9e6-155">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db9e6-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db9e6-156">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db9e6-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db9e6-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db9e6-157">CommonParameters</span></span>
<span data-ttu-id="db9e6-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db9e6-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db9e6-159">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db9e6-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db9e6-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db9e6-160">INPUTS</span></span>

### <span data-ttu-id="db9e6-161">System. String</span><span class="sxs-lookup"><span data-stu-id="db9e6-161">System.String</span></span>

### <span data-ttu-id="db9e6-162">Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceState</span><span class="sxs-lookup"><span data-stu-id="db9e6-162">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState</span></span>

### <span data-ttu-id="db9e6-163">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="db9e6-163">System.Boolean</span></span>

### <span data-ttu-id="db9e6-164">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="db9e6-164">System.Collections.Hashtable</span></span>

## <span data-ttu-id="db9e6-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db9e6-165">OUTPUTS</span></span>

### <span data-ttu-id="db9e6-166">Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="db9e6-166">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="db9e6-167">Note</span><span class="sxs-lookup"><span data-stu-id="db9e6-167">NOTES</span></span>

## <span data-ttu-id="db9e6-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db9e6-168">RELATED LINKS</span></span>

[<span data-ttu-id="db9e6-169">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="db9e6-169">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="db9e6-170">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="db9e6-170">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="db9e6-171">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="db9e6-171">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)



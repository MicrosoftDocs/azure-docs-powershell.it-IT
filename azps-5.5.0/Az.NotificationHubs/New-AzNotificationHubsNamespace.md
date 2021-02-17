---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 24a42fba23427f437cb064e1915c19e36e7a71bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191511"
---
# <span data-ttu-id="32c0a-101">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="32c0a-101">New-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="32c0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="32c0a-103">Crea uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="32c0a-103">Creates a notification hub namespace.</span></span>

## <span data-ttu-id="32c0a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32c0a-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32c0a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="32c0a-105">DESCRIPTION</span></span>
<span data-ttu-id="32c0a-106">Il cmdlet **New-AzNotificationHubsHubsNotification crea** uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="32c0a-106">The **New-AzNotificationHubsNamespace** cmdlet creates a notification hub namespace.</span></span>
<span data-ttu-id="32c0a-107">Gli spazi dei nomi sono contenitori logici che consentono di organizzare e gestire gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="32c0a-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="32c0a-108">È necessario avere almeno uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="32c0a-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="32c0a-109">Un singolo spazio dei nomi può ospitare più hub.</span><span class="sxs-lookup"><span data-stu-id="32c0a-109">A single namespace can house multiple hubs.</span></span>
<span data-ttu-id="32c0a-110">È possibile disporre di più spazi dei nomi per organizzare gli hub o per concedere a singoli utenti specifici l'autorizzazione per gestire un sottoinsieme selezionato di hub.</span><span class="sxs-lookup"><span data-stu-id="32c0a-110">You can have multiple namespaces to organize your hubs, or to give specific individuals permission to manage a selected subset of your hubs.</span></span>
<span data-ttu-id="32c0a-111">Per creare uno spazio dei nomi, assicurarsi di specificare un nome univoco per lo spazio dei nomi; specificare il data center in cui si trova lo spazio dei nomi; e specificare il gruppo di risorse a cui verrà assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="32c0a-111">To create a namespace, make sure that you specify a unique name for the namespace; specify the datacenter where the namespace will be located; and, specify the resource group that the namespace will be assigned to.</span></span>
<span data-ttu-id="32c0a-112">Dopo aver creato lo spazio dei nomi, è possibile usare il cmdlet New-AzNotificationHubsNamespaceAuthorizationRules per assegnare regole di autorizzazione a tale spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="32c0a-112">After the namespace has been created you can use the New-AzNotificationHubsNamespaceAuthorizationRules cmdlet to assign authorization rules to that namespace.</span></span>
<span data-ttu-id="32c0a-113">Le regole di autorizzazione vengono usate per gestire le autorizzazioni per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="32c0a-113">Authorization rules are used to manage permissions to the namespace.</span></span>

## <span data-ttu-id="32c0a-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32c0a-114">EXAMPLES</span></span>

### <span data-ttu-id="32c0a-115">Esempio 1: Creare un hub di notifica</span><span class="sxs-lookup"><span data-stu-id="32c0a-115">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

<span data-ttu-id="32c0a-116">Questo comando crea un hub di notifica denominato ContosoPartners.</span><span class="sxs-lookup"><span data-stu-id="32c0a-116">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="32c0a-117">Lo spazio dei nomi si trova nel data center degli Stati Uniti occidentali e verrà assegnato al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="32c0a-117">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="32c0a-118">Esempio 2: Creare un hub di notifica con tag</span><span class="sxs-lookup"><span data-stu-id="32c0a-118">Example 2: Create a notification hub with tags</span></span>
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

<span data-ttu-id="32c0a-119">Questo comando crea un hub di notifica denominato ContosoPartners.</span><span class="sxs-lookup"><span data-stu-id="32c0a-119">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="32c0a-120">Lo spazio dei nomi si trova nel data center degli Stati Uniti occidentali e verrà assegnato al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="32c0a-120">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="32c0a-121">Inoltre, questo comando crea un tag con il nome Gruppo di destinatari e il valore PartnerOrganizations e viene assegnato allo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="32c0a-121">In addition, this command creates a tag with the name Audience and the value PartnerOrganizations and is assigned to the namespace.</span></span>
<span data-ttu-id="32c0a-122">In questo modo lo spazio dei nomi verrà visualizzato ogni volta che si filtrano gli elementi in cui il tag Gruppo di destinatari è impostato su PartnerOrganizations.</span><span class="sxs-lookup"><span data-stu-id="32c0a-122">This ensures that the namespace will be displayed any time you filter for items where the Audience tag is set to PartnerOrganizations.</span></span>

## <span data-ttu-id="32c0a-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32c0a-123">PARAMETERS</span></span>

### <span data-ttu-id="32c0a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32c0a-124">-DefaultProfile</span></span>
<span data-ttu-id="32c0a-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="32c0a-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32c0a-126">-Location</span><span class="sxs-lookup"><span data-stu-id="32c0a-126">-Location</span></span>
<span data-ttu-id="32c0a-127">Specifica il nome visualizzato del data center che ospiterà lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="32c0a-127">Specifies the display name of the datacenter that will host the Namespace.</span></span>
<span data-ttu-id="32c0a-128">Anche se è possibile impostare questo parametro su qualsiasi posizione valida, per ottenere prestazioni ottimali è consigliabile usare un data center situato nella maggior parte degli utenti.</span><span class="sxs-lookup"><span data-stu-id="32c0a-128">Although you can set this parameter to any valid location, for optimal performance you might want to use a datacenter located near the majority of your users.</span></span>

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

### <span data-ttu-id="32c0a-129">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="32c0a-129">-Namespace</span></span>
<span data-ttu-id="32c0a-130">Specifica il nome del nuovo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="32c0a-130">Specifies the name of the new namespace.</span></span>
<span data-ttu-id="32c0a-131">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="32c0a-131">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="32c0a-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="32c0a-132">-ResourceGroup</span></span>
<span data-ttu-id="32c0a-133">Specifica il gruppo di risorse a cui verrà assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="32c0a-133">Specifies the resource group to which the namespace will be assigned.</span></span>
<span data-ttu-id="32c0a-134">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che consentono semplicemente la gestione e l'amministrazione dell'inventario.</span><span class="sxs-lookup"><span data-stu-id="32c0a-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and administration.</span></span>

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

### <span data-ttu-id="32c0a-135">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="32c0a-135">-SkuTier</span></span>
<span data-ttu-id="32c0a-136">Livello SKU dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="32c0a-136">Sku tier of the namespace</span></span>

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

### <span data-ttu-id="32c0a-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="32c0a-137">-Tag</span></span>
<span data-ttu-id="32c0a-138">Specifica coppie nome-valore che possono essere usate per categorizzare e organizzare gli elementi di Azure.</span><span class="sxs-lookup"><span data-stu-id="32c0a-138">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="32c0a-139">I tag funzionano in modo simile alle parole chiave e operano in una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="32c0a-139">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="32c0a-140">Ad esempio, se si ricercano tutti gli elementi con il tag Department:IT, la ricerca restituirà tutti gli elementi azure che hanno quel tag, indipendentemente dal tipo di elemento, dalla posizione o dal gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="32c0a-140">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>
<span data-ttu-id="32c0a-141">Un singolo tag è costituito da due parti: *Name e,* facoltativamente, *value.*</span><span class="sxs-lookup"><span data-stu-id="32c0a-141">An individual tag consists of two parts: the *Name* and, optionally, the *Value*.</span></span>
<span data-ttu-id="32c0a-142">Ad esempio, in Department:IT il nome del tag è Department e il valore del tag è IT.</span><span class="sxs-lookup"><span data-stu-id="32c0a-142">For instance, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="32c0a-143">Per aggiungere un tag, usare una sintassi della tabella hash simile alla seguente, che crea il tag CalendarYear:2016:</span><span class="sxs-lookup"><span data-stu-id="32c0a-143">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32c0a-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32c0a-144">-Confirm</span></span>
<span data-ttu-id="32c0a-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32c0a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32c0a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32c0a-146">-WhatIf</span></span>
<span data-ttu-id="32c0a-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32c0a-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="32c0a-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32c0a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32c0a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32c0a-149">CommonParameters</span></span>
<span data-ttu-id="32c0a-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32c0a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32c0a-151">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32c0a-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32c0a-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="32c0a-152">INPUTS</span></span>

### <span data-ttu-id="32c0a-153">System.String</span><span class="sxs-lookup"><span data-stu-id="32c0a-153">System.String</span></span>

### <span data-ttu-id="32c0a-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="32c0a-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="32c0a-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32c0a-155">OUTPUTS</span></span>

### <span data-ttu-id="32c0a-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="32c0a-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="32c0a-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="32c0a-157">NOTES</span></span>

## <span data-ttu-id="32c0a-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32c0a-158">RELATED LINKS</span></span>

[<span data-ttu-id="32c0a-159">Get-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="32c0a-159">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="32c0a-160">Remove-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="32c0a-160">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="32c0a-161">Set-AzNotificationHubsHubsHubs</span><span class="sxs-lookup"><span data-stu-id="32c0a-161">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)



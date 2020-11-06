---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 504fe8b5aad0e2e028bf27cf08a29fd335edfa33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515511"
---
# <span data-ttu-id="baed5-101">New-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="baed5-101">New-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="baed5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="baed5-102">SYNOPSIS</span></span>
<span data-ttu-id="baed5-103">Crea uno spazio dei nomi Hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="baed5-103">Creates a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="baed5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="baed5-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="baed5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="baed5-105">DESCRIPTION</span></span>
<span data-ttu-id="baed5-106">Il cmdlet **New-AzureRmNotificationHubsNamespace** crea uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="baed5-106">The **New-AzureRmNotificationHubsNamespace** cmdlet creates a notification hub namespace.</span></span>

<span data-ttu-id="baed5-107">Gli spazi dei nomi sono contenitori logici che consentono di organizzare e gestire gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="baed5-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="baed5-108">È necessario avere almeno uno spazio dei nomi dell'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="baed5-108">You must have at least one notification hub namespace.</span></span>
<span data-ttu-id="baed5-109">Un singolo spazio dei nomi può ospitare più hub.</span><span class="sxs-lookup"><span data-stu-id="baed5-109">A single namespace can house multiple hubs.</span></span>
<span data-ttu-id="baed5-110">Puoi disporre di più spazi dei nomi per organizzare i tuoi Hub o per dare agli utenti specifici l'autorizzazione per gestire un subset selezionato degli hub.</span><span class="sxs-lookup"><span data-stu-id="baed5-110">You can have multiple namespaces to organize your hubs, or to give specific individuals permission to manage a selected subset of your hubs.</span></span>

<span data-ttu-id="baed5-111">Per creare uno spazio dei nomi, assicurati di specificare un nome univoco per lo spazio dei nomi; specificare il Data Center in cui verrà posizionato lo spazio dei nomi; e specifica il gruppo di risorse a cui verrà assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="baed5-111">To create a namespace, make sure that you specify a unique name for the namespace; specify the datacenter where the namespace will be located; and, specify the resource group that the namespace will be assigned to.</span></span>
<span data-ttu-id="baed5-112">Dopo aver creato lo spazio dei nomi, puoi usare il cmdlet New-AzureRmNotificationHubsNamespaceAuthorizationRules per assegnare le regole di autorizzazione a tale spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="baed5-112">After the namespace has been created you can use the New-AzureRmNotificationHubsNamespaceAuthorizationRules cmdlet to assign authorization rules to that namespace.</span></span>
<span data-ttu-id="baed5-113">Le regole di autorizzazione vengono usate per gestire le autorizzazioni per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="baed5-113">Authorization rules are used to manage permissions to the namespace.</span></span>

## <span data-ttu-id="baed5-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="baed5-114">EXAMPLES</span></span>

### <span data-ttu-id="baed5-115">Esempio 1: creare un hub di notifica</span><span class="sxs-lookup"><span data-stu-id="baed5-115">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

<span data-ttu-id="baed5-116">Questo comando crea un hub di notifica denominato ContosoPartners.</span><span class="sxs-lookup"><span data-stu-id="baed5-116">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="baed5-117">Lo spazio dei nomi sarà disponibile nel Data Center ovest degli Stati Uniti e verrà assegnato al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="baed5-117">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="baed5-118">Esempio 2: creare un hub di notifica con tag</span><span class="sxs-lookup"><span data-stu-id="baed5-118">Example 2: Create a notification hub with tags</span></span>
```
PS C:\>New-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

<span data-ttu-id="baed5-119">Questo comando crea un hub di notifica denominato ContosoPartners.</span><span class="sxs-lookup"><span data-stu-id="baed5-119">This command creates a notification hub named ContosoPartners.</span></span>
<span data-ttu-id="baed5-120">Lo spazio dei nomi sarà disponibile nel Data Center ovest degli Stati Uniti e verrà assegnato al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="baed5-120">The namespace will be located in the West US datacenter and be assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="baed5-121">Questo comando crea inoltre un tag con il nome audience e il valore PartnerOrganizations e viene assegnato allo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="baed5-121">In addition, this command creates a tag with the name Audience and the value PartnerOrganizations and is assigned to the namespace.</span></span>
<span data-ttu-id="baed5-122">In questo modo, lo spazio dei nomi verrà visualizzato ogni volta che filtri per gli elementi in cui il tag audience è impostato su PartnerOrganizations.</span><span class="sxs-lookup"><span data-stu-id="baed5-122">This ensures that the namespace will be displayed any time you filter for items where the Audience tag is set to PartnerOrganizations.</span></span>

## <span data-ttu-id="baed5-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="baed5-123">PARAMETERS</span></span>

### <span data-ttu-id="baed5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baed5-124">-DefaultProfile</span></span>
<span data-ttu-id="baed5-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="baed5-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="baed5-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="baed5-126">-Location</span></span>
<span data-ttu-id="baed5-127">Specifica il nome visualizzato del centro dati che ospiterà lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="baed5-127">Specifies the display name of the datacenter that will host the Namespace.</span></span>
<span data-ttu-id="baed5-128">Anche se è possibile impostare questo parametro su qualsiasi posizione valida, per ottenere prestazioni ottimali, è consigliabile usare un data center situato in prossimità della maggior parte degli utenti.</span><span class="sxs-lookup"><span data-stu-id="baed5-128">Although you can set this parameter to any valid location, for optimal performance you might want to use a datacenter located near the majority of your users.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baed5-129">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="baed5-129">-Namespace</span></span>
<span data-ttu-id="baed5-130">Specifica il nome del nuovo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="baed5-130">Specifies the name of the new namespace.</span></span>
<span data-ttu-id="baed5-131">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="baed5-131">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="baed5-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="baed5-132">-ResourceGroup</span></span>
<span data-ttu-id="baed5-133">Specifica il gruppo di risorse a cui verrà assegnato lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="baed5-133">Specifies the resource group to which the namespace will be assigned.</span></span>
<span data-ttu-id="baed5-134">I gruppi di risorse organizzano elementi come spazi dei nomi, hub di notifica e regole di autorizzazione in modi che semplificano la gestione e l'amministrazione dell'inventario.</span><span class="sxs-lookup"><span data-stu-id="baed5-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and administration.</span></span>

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

### <span data-ttu-id="baed5-135">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="baed5-135">-SkuTier</span></span>
<span data-ttu-id="baed5-136">Livello SKU dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="baed5-136">Sku tier of the namespace</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baed5-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="baed5-137">-Tag</span></span>
<span data-ttu-id="baed5-138">Specifica le coppie nome/valore che possono essere usate per categorizzare e organizzare gli elementi Azure.</span><span class="sxs-lookup"><span data-stu-id="baed5-138">Specifies name-value pairs that can be used to categorize and organize Azure items.</span></span>
<span data-ttu-id="baed5-139">I tag funzionano in modo simile alle parole chiave e funzionano in una distribuzione.</span><span class="sxs-lookup"><span data-stu-id="baed5-139">Tags function similar to keywords, and operate across a deployment.</span></span>
<span data-ttu-id="baed5-140">Ad esempio, se si cercano tutti gli elementi con il reparto Tag: la ricerca restituirà tutti gli elementi di Azure che hanno il tag, indipendentemente da oggetti come il tipo di elemento, la posizione o il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="baed5-140">For example, if you search for all items with the tag Department:IT the search will return all the Azure items that have that tag, regardless of such things as item type, location, or resource group.</span></span>

<span data-ttu-id="baed5-141">Un singolo tag è costituito da due parti: il *nome* e, facoltativamente, il *valore*.</span><span class="sxs-lookup"><span data-stu-id="baed5-141">An individual tag consists of two parts: the *Name* and, optionally, the *Value*.</span></span>
<span data-ttu-id="baed5-142">Ad esempio, nel reparto: il nome del tag è reparto e il valore di tag è.</span><span class="sxs-lookup"><span data-stu-id="baed5-142">For instance, in Department:IT, the tag name is Department and the tag value is IT.</span></span>
<span data-ttu-id="baed5-143">Per aggiungere un tag, usa la sintassi della tabella hash simile alla seguente, che crea il tag CalendarYear: 2016:</span><span class="sxs-lookup"><span data-stu-id="baed5-143">To add a tag, use hash table syntax similar to this, which creates the tag CalendarYear:2016:</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baed5-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="baed5-144">-Confirm</span></span>
<span data-ttu-id="baed5-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baed5-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baed5-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baed5-146">-WhatIf</span></span>
<span data-ttu-id="baed5-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="baed5-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="baed5-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="baed5-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baed5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baed5-149">CommonParameters</span></span>
<span data-ttu-id="baed5-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baed5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baed5-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baed5-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baed5-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="baed5-152">INPUTS</span></span>

### <span data-ttu-id="baed5-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="baed5-153">None</span></span>
<span data-ttu-id="baed5-154">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="baed5-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="baed5-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="baed5-155">OUTPUTS</span></span>

### <span data-ttu-id="baed5-156">Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="baed5-156">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="baed5-157">Note</span><span class="sxs-lookup"><span data-stu-id="baed5-157">NOTES</span></span>

## <span data-ttu-id="baed5-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="baed5-158">RELATED LINKS</span></span>

[<span data-ttu-id="baed5-159">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="baed5-159">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="baed5-160">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="baed5-160">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="baed5-161">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="baed5-161">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)



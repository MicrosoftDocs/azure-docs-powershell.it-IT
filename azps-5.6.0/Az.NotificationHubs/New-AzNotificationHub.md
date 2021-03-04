---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
ms.openlocfilehash: 88ed662dc9938e6d4c9c3caa07ce733530dff6b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951293"
---
# <span data-ttu-id="3ea1a-101">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3ea1a-101">New-AzNotificationHub</span></span>

## <span data-ttu-id="3ea1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ea1a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ea1a-103">Crea un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-103">Creates a notification hub.</span></span>

## <span data-ttu-id="3ea1a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ea1a-104">SYNTAX</span></span>

### <span data-ttu-id="3ea1a-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ea1a-105">InputFileParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ea1a-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ea1a-106">NotificationHubParameterSet</span></span>
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ea1a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3ea1a-107">DESCRIPTION</span></span>
<span data-ttu-id="3ea1a-108">Il cmdlet **New-AzNotificationHub** crea un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-108">The **New-AzNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="3ea1a-109">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma usata da tali client.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="3ea1a-110">Gli hub di notifica sono approssimativamente equivalenti alle singole app: ogni app avrà in genere un proprio hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="3ea1a-111">Il cmdlet **New-AzNotificationHub** consente di creare un nuovo hub di notifica in due modi.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-111">The **New-AzNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="3ea1a-112">È possibile creare un'istanza **dell'oggetto NotificationHubAttributes** e quindi configurare tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="3ea1a-113">È quindi possibile copiare i valori delle proprietà nel nuovo hub tramite il *parametro NotificationHubObj.*</span><span class="sxs-lookup"><span data-stu-id="3ea1a-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="3ea1a-114">In alternativa, è possibile creare un file JSON (JavaScript Object Notation) contenente i valori di configurazione pertinenti e quindi applicarlo usando il *parametro InputFile.*</span><span class="sxs-lookup"><span data-stu-id="3ea1a-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="3ea1a-115">Se usato insieme al cmdlet **New-AzNotificationHub,** l'esempio JSON precedente crea un hub di notifica denominato ContosoNotificationHub situato nel data center degli Stati Uniti occidentali.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-115">When used in conjunction with the **New-AzNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="3ea1a-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ea1a-116">EXAMPLES</span></span>

### <span data-ttu-id="3ea1a-117">Esempio 1: Creare un hub di notifica</span><span class="sxs-lookup"><span data-stu-id="3ea1a-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="3ea1a-118">Questo comando crea un hub di notifica nello spazio dei nomi ContosoNtassi.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="3ea1a-119">Il nuovo hub verrà assegnato a ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="3ea1a-120">Non è necessario specificare un nome o altre informazioni di configurazione per l'hub; queste informazioni verranno prese dal file di input C:\Configurations\InternalHub.jsaperto.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="3ea1a-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ea1a-121">PARAMETERS</span></span>

### <span data-ttu-id="3ea1a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ea1a-122">-DefaultProfile</span></span>
<span data-ttu-id="3ea1a-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3ea1a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ea1a-124">-InputFile</span><span class="sxs-lookup"><span data-stu-id="3ea1a-124">-InputFile</span></span>
<span data-ttu-id="3ea1a-125">Specifica il percorso di un file JSON contenente valori di configurazione per il nuovo hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-125">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

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

### <span data-ttu-id="3ea1a-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3ea1a-126">-Namespace</span></span>
<span data-ttu-id="3ea1a-127">Specifica lo spazio dei nomi a cui verrà assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-127">Specifies the namespace to which the notification hub will be assigned.</span></span>
<span data-ttu-id="3ea1a-128">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-128">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="3ea1a-129">Gli hub di notifica devono essere assegnati a uno spazio dei nomi esistente.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-129">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="3ea1a-130">Il cmdlet **New-AzNotificationHub non** può creare un nuovo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-130">The **New-AzNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="3ea1a-131">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="3ea1a-131">-NotificationHubObj</span></span>
<span data-ttu-id="3ea1a-132">Specifica **l'oggetto NotificationHubAttributes** che contiene informazioni di configurazione per il nuovo hub.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-132">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ea1a-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3ea1a-133">-ResourceGroup</span></span>
<span data-ttu-id="3ea1a-134">Specifica il gruppo di risorse a cui verrà assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-134">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="3ea1a-135">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che consentono semplicemente la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="3ea1a-136">È necessario usare un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-136">You must use an existing resource group.</span></span>
<span data-ttu-id="3ea1a-137">Il cmdlet **New-AzNotificationHub non** può creare un nuovo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-137">The **New-AzNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="3ea1a-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ea1a-138">-Confirm</span></span>
<span data-ttu-id="3ea1a-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ea1a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ea1a-140">-WhatIf</span></span>
<span data-ttu-id="3ea1a-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ea1a-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ea1a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ea1a-143">CommonParameters</span></span>
<span data-ttu-id="3ea1a-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ea1a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ea1a-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ea1a-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ea1a-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="3ea1a-146">INPUTS</span></span>

### <span data-ttu-id="3ea1a-147">System.String</span><span class="sxs-lookup"><span data-stu-id="3ea1a-147">System.String</span></span>

## <span data-ttu-id="3ea1a-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ea1a-148">OUTPUTS</span></span>

### <span data-ttu-id="3ea1a-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="3ea1a-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="3ea1a-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="3ea1a-150">NOTES</span></span>

## <span data-ttu-id="3ea1a-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ea1a-151">RELATED LINKS</span></span>

[<span data-ttu-id="3ea1a-152">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3ea1a-152">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="3ea1a-153">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3ea1a-153">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="3ea1a-154">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="3ea1a-154">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)



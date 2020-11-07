---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHub.md
ms.openlocfilehash: c0a3e2231ef0f27689a08b9199876d04c4e68b2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686246"
---
# <span data-ttu-id="5991e-101">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="5991e-101">New-AzureRmNotificationHub</span></span>

## <span data-ttu-id="5991e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5991e-102">SYNOPSIS</span></span>
<span data-ttu-id="5991e-103">Crea un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5991e-103">Creates a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5991e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5991e-104">SYNTAX</span></span>

### <span data-ttu-id="5991e-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="5991e-105">InputFileParameterSet</span></span>
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5991e-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="5991e-106">NotificationHubParameterSet</span></span>
```
New-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5991e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5991e-107">DESCRIPTION</span></span>
<span data-ttu-id="5991e-108">Il cmdlet **New-AzureRmNotificationHub** crea un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5991e-108">The **New-AzureRmNotificationHub** cmdlet creates a notification hub.</span></span>
<span data-ttu-id="5991e-109">Gli hub di notifica vengono usati per inviare notifiche push a più client indipendentemente dalla piattaforma utilizzata da tali client.</span><span class="sxs-lookup"><span data-stu-id="5991e-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="5991e-110">Gli hub di notifica equivalgono approssimativamente alle singole app: ognuna delle tue app avrà in genere un hub di notifica personalizzato.</span><span class="sxs-lookup"><span data-stu-id="5991e-110">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="5991e-111">Il cmdlet **New-AzureRmNotificationHub** offre due modi per creare un nuovo hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5991e-111">The **New-AzureRmNotificationHub** cmdlet provides two ways to create a new notification hub.</span></span>
<span data-ttu-id="5991e-112">Puoi creare un'istanza dell'oggetto **NotificationHubAttributes** e quindi configurare quell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5991e-112">You can create an instance of the **NotificationHubAttributes** object and then configure that object.</span></span>
<span data-ttu-id="5991e-113">Puoi quindi copiare questi valori di proprietà nel nuovo hub tramite il parametro *NotificationHubObj* .</span><span class="sxs-lookup"><span data-stu-id="5991e-113">You can then copy those property values to your new hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="5991e-114">In alternativa, puoi creare un file JSON (JavaScript Object Notation) che contiene i valori di configurazione rilevanti e quindi applicare tali valori usando il parametro *inputfile* .</span><span class="sxs-lookup"><span data-stu-id="5991e-114">Alternatively, you can create a JSON (JavaScript Object Notation) file containing the relevant configuration values and  then apply those values by using the *InputFile* parameter.</span></span>
<span data-ttu-id="5991e-115">Se usato insieme al cmdlet **New-AzureRmNotificationHub** , nell'esempio JSON precedente viene creato un hub di notifica denominato ContosoNotificationHub che si trova nel Data Center ovest degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="5991e-115">When used in conjunction with the **New-AzureRmNotificationHub** cmdlet, the preceding JSON sample creates a notification hub named ContosoNotificationHub located on the West US datacenter.</span></span>

## <span data-ttu-id="5991e-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5991e-116">EXAMPLES</span></span>

### <span data-ttu-id="5991e-117">Esempio 1: creare un hub di notifica</span><span class="sxs-lookup"><span data-stu-id="5991e-117">Example 1: Create a notification hub</span></span>
```
PS C:\>New-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

<span data-ttu-id="5991e-118">Questo comando crea un hub di notifica nello spazio dei nomi ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="5991e-118">This command creates a notification hub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="5991e-119">Il nuovo hub verrà assegnato a ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="5991e-119">The new hub will be assigned to the ContosoNotificationsGroup.</span></span>
<span data-ttu-id="5991e-120">Non è necessario specificare un nome o altre informazioni di configurazione per l'hub; le informazioni verranno ricavate dal file di input C:\Configurations\InternalHub.jsattivato.</span><span class="sxs-lookup"><span data-stu-id="5991e-120">You do not need to specify a name or any other configuration information for the hub; that information will be taken from the input file C:\Configurations\InternalHub.json.</span></span>

## <span data-ttu-id="5991e-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5991e-121">PARAMETERS</span></span>

### <span data-ttu-id="5991e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5991e-122">-DefaultProfile</span></span>
<span data-ttu-id="5991e-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5991e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5991e-124">-InputFile</span><span class="sxs-lookup"><span data-stu-id="5991e-124">-InputFile</span></span>
<span data-ttu-id="5991e-125">Specifica il percorso di un file JSON contenente i valori di configurazione per il nuovo hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5991e-125">Specifies the path to a JSON file containing configuration values for the new notification hub.</span></span>

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

### <span data-ttu-id="5991e-126">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5991e-126">-Namespace</span></span>
<span data-ttu-id="5991e-127">Specifica lo spazio dei nomi a cui verrà assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5991e-127">Specifies the namespace to which the notification hub will be assigned.</span></span>
<span data-ttu-id="5991e-128">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5991e-128">Namespaces provide a way to group and categorize notification hubs.</span></span>
<span data-ttu-id="5991e-129">Gli hub di notifica devono essere assegnati a uno spazio dei nomi esistente.</span><span class="sxs-lookup"><span data-stu-id="5991e-129">Notification hubs must be assigned to an existing namespace.</span></span>
<span data-ttu-id="5991e-130">Il cmdlet **New-AzureRmNotificationHub** non può creare un nuovo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="5991e-130">The **New-AzureRmNotificationHub** cmdlet cannot create a new namespace.</span></span>

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

### <span data-ttu-id="5991e-131">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="5991e-131">-NotificationHubObj</span></span>
<span data-ttu-id="5991e-132">Specifica l'oggetto **NotificationHubAttributes** che contiene le informazioni di configurazione per il nuovo hub.</span><span class="sxs-lookup"><span data-stu-id="5991e-132">Specifies the **NotificationHubAttributes** object that contains configuration information for the new hub.</span></span>

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

### <span data-ttu-id="5991e-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5991e-133">-ResourceGroup</span></span>
<span data-ttu-id="5991e-134">Specifica il gruppo di risorse a cui verrà assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5991e-134">Specifies the resource group to which the notification hub will be assigned.</span></span>
<span data-ttu-id="5991e-135">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5991e-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>
<span data-ttu-id="5991e-136">Devi usare un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="5991e-136">You must use an existing resource group.</span></span>
<span data-ttu-id="5991e-137">Il cmdlet **New-AzureRmNotificationHub** non può creare un nuovo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5991e-137">The **New-AzureRmNotificationHub** cmdlet cannot create a new resource group.</span></span>

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

### <span data-ttu-id="5991e-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5991e-138">-Confirm</span></span>
<span data-ttu-id="5991e-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5991e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5991e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5991e-140">-WhatIf</span></span>
<span data-ttu-id="5991e-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5991e-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5991e-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5991e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5991e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5991e-143">CommonParameters</span></span>
<span data-ttu-id="5991e-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5991e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5991e-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5991e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5991e-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5991e-146">INPUTS</span></span>

### <span data-ttu-id="5991e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="5991e-147">System.String</span></span>

## <span data-ttu-id="5991e-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5991e-148">OUTPUTS</span></span>

### <span data-ttu-id="5991e-149">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="5991e-149">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="5991e-150">Note</span><span class="sxs-lookup"><span data-stu-id="5991e-150">NOTES</span></span>

## <span data-ttu-id="5991e-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5991e-151">RELATED LINKS</span></span>

[<span data-ttu-id="5991e-152">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="5991e-152">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="5991e-153">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="5991e-153">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

[<span data-ttu-id="5991e-154">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="5991e-154">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)



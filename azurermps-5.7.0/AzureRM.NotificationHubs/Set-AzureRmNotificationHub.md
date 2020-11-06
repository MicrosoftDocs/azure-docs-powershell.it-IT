---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/set-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHub.md
ms.openlocfilehash: e035cb24c6341eb6d5b3d8aba5cd86b67fdafca2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521877"
---
# <span data-ttu-id="4d22a-101">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="4d22a-101">Set-AzureRmNotificationHub</span></span>

## <span data-ttu-id="4d22a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d22a-102">SYNOPSIS</span></span>
<span data-ttu-id="4d22a-103">Imposta i valori delle proprietà per un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="4d22a-103">Sets property values for a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d22a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d22a-104">SYNTAX</span></span>

### <span data-ttu-id="4d22a-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d22a-105">InputFileParameterSet</span></span>
```
Set-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d22a-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d22a-106">NotificationHubParameterSet</span></span>
```
Set-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d22a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d22a-107">DESCRIPTION</span></span>
<span data-ttu-id="4d22a-108">Il cmdlet **set-AzureRmNotificationHub** modifica i valori delle proprietà di un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="4d22a-108">The **Set-AzureRmNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>

<span data-ttu-id="4d22a-109">È possibile modificare un valore della proprietà dell'hub di notifica in due modi.</span><span class="sxs-lookup"><span data-stu-id="4d22a-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="4d22a-110">Per uno, puoi creare un'istanza dell'oggetto **NotificationHubAttributes** e quindi configurare l'oggetto con i valori della proprietà che vuoi che il nuovo hub abbia in possesso.</span><span class="sxs-lookup"><span data-stu-id="4d22a-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="4d22a-111">Questa operazione può essere eseguita tramite .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="4d22a-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="4d22a-112">Puoi quindi copiare questi valori di proprietà nell'hub tramite il parametro *NotificationHubObj* .</span><span class="sxs-lookup"><span data-stu-id="4d22a-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>

<span data-ttu-id="4d22a-113">In alternativa, puoi creare un file JSON (JavaScript Object Notation) che contiene i valori di configurazione rilevanti e quindi applicare tali valori tramite il parametro *inputfile* .</span><span class="sxs-lookup"><span data-stu-id="4d22a-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="4d22a-114">Un file JSON è un file di testo che usa una sintassi simile alla seguente:</span><span class="sxs-lookup"><span data-stu-id="4d22a-114">A JSON file is a text file that uses syntax similar to the following:</span></span>

<span data-ttu-id="4d22a-115">{</span><span class="sxs-lookup"><span data-stu-id="4d22a-115">{</span></span>  
    <span data-ttu-id="4d22a-116">"Nome": "ContosoNotificationHub",</span><span class="sxs-lookup"><span data-stu-id="4d22a-116">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="4d22a-117">"Posizione": "West US",</span><span class="sxs-lookup"><span data-stu-id="4d22a-117">"Location": "West US",</span></span>  
<span data-ttu-id="4d22a-118">}</span><span class="sxs-lookup"><span data-stu-id="4d22a-118">}</span></span>

<span data-ttu-id="4d22a-119">Se usato insieme al cmdlet **set-AzureRmNotificationHub** , l'esempio JSON precedente imposta il valore della posizione di un hub di notifica denominato ContosoNotificationHub in West US.</span><span class="sxs-lookup"><span data-stu-id="4d22a-119">When used in conjunction with the **Set-AzureRmNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="4d22a-120">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d22a-120">EXAMPLES</span></span>

### <span data-ttu-id="4d22a-121">Esempio 1: modificare i valori delle proprietà per un hub di notifica</span><span class="sxs-lookup"><span data-stu-id="4d22a-121">Example 1: Modify the property values for a notification hub</span></span>
```
PS C:\>Set-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="4d22a-122">Questo comando modifica i valori delle proprietà per un hub di notifica trovato nello spazio dei nomi ContosoNamespace e lo assegna al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="4d22a-122">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="4d22a-123">I valori delle proprietà, oltre al nome dell'hub da modificare, non vengono specificati nel comando.</span><span class="sxs-lookup"><span data-stu-id="4d22a-123">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="4d22a-124">Queste informazioni sono invece contenute nel file di input C:\Configuration\Hubs.jsattivato.</span><span class="sxs-lookup"><span data-stu-id="4d22a-124">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

## <span data-ttu-id="4d22a-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d22a-125">PARAMETERS</span></span>

### <span data-ttu-id="4d22a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d22a-126">-DefaultProfile</span></span>
<span data-ttu-id="4d22a-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4d22a-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d22a-128">-Force</span><span class="sxs-lookup"><span data-stu-id="4d22a-128">-Force</span></span>
<span data-ttu-id="4d22a-129">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="4d22a-129">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d22a-130">-InputFile</span><span class="sxs-lookup"><span data-stu-id="4d22a-130">-InputFile</span></span>
<span data-ttu-id="4d22a-131">Specifica il percorso di un file JSON che contiene le informazioni di configurazione per l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="4d22a-131">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

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

### <span data-ttu-id="4d22a-132">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4d22a-132">-Namespace</span></span>
<span data-ttu-id="4d22a-133">Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="4d22a-133">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="4d22a-134">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="4d22a-134">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="4d22a-135">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="4d22a-135">-NotificationHubObj</span></span>
<span data-ttu-id="4d22a-136">Specifica l'oggetto **NotificationHubAttributes** che contiene le informazioni di configurazione per l'hub modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d22a-136">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

```yaml
Type: NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d22a-137">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4d22a-137">-ResourceGroup</span></span>
<span data-ttu-id="4d22a-138">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="4d22a-138">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="4d22a-139">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4d22a-139">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="4d22a-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4d22a-140">-Confirm</span></span>
<span data-ttu-id="4d22a-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d22a-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d22a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d22a-142">-WhatIf</span></span>
<span data-ttu-id="4d22a-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d22a-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d22a-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d22a-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d22a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d22a-145">CommonParameters</span></span>
<span data-ttu-id="4d22a-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d22a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d22a-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d22a-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d22a-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d22a-148">INPUTS</span></span>

### <span data-ttu-id="4d22a-149">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4d22a-149">None</span></span>
<span data-ttu-id="4d22a-150">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="4d22a-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4d22a-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d22a-151">OUTPUTS</span></span>

### <span data-ttu-id="4d22a-152">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="4d22a-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="4d22a-153">Note</span><span class="sxs-lookup"><span data-stu-id="4d22a-153">NOTES</span></span>

## <span data-ttu-id="4d22a-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d22a-154">RELATED LINKS</span></span>

[<span data-ttu-id="4d22a-155">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="4d22a-155">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="4d22a-156">New-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="4d22a-156">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="4d22a-157">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="4d22a-157">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)



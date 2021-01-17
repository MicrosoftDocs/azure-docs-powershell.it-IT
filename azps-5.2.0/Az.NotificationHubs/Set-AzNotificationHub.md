---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: 7083c6872981cefaa12dc01612f3eb27cc7676ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336139"
---
# <span data-ttu-id="10f89-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="10f89-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="10f89-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="10f89-102">SYNOPSIS</span></span>
<span data-ttu-id="10f89-103">Imposta i valori delle proprietà per un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10f89-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="10f89-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10f89-104">SYNTAX</span></span>

### <span data-ttu-id="10f89-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="10f89-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10f89-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="10f89-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10f89-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10f89-107">DESCRIPTION</span></span>
<span data-ttu-id="10f89-108">Il cmdlet **set-AzNotificationHub** modifica i valori delle proprietà di un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10f89-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="10f89-109">È possibile modificare un valore della proprietà dell'hub di notifica in due modi.</span><span class="sxs-lookup"><span data-stu-id="10f89-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="10f89-110">Per uno, puoi creare un'istanza dell'oggetto **NotificationHubAttributes** e quindi configurare l'oggetto con i valori della proprietà che vuoi che il nuovo hub abbia in possesso.</span><span class="sxs-lookup"><span data-stu-id="10f89-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="10f89-111">Questa operazione può essere eseguita tramite .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="10f89-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="10f89-112">Puoi quindi copiare questi valori di proprietà nell'hub tramite il parametro *NotificationHubObj* .</span><span class="sxs-lookup"><span data-stu-id="10f89-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="10f89-113">In alternativa, puoi creare un file JSON (JavaScript Object Notation) che contiene i valori di configurazione rilevanti e quindi applicare tali valori tramite il parametro *inputfile* .</span><span class="sxs-lookup"><span data-stu-id="10f89-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="10f89-114">Un file JSON è un file di testo che usa una sintassi simile alla seguente: {</span><span class="sxs-lookup"><span data-stu-id="10f89-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="10f89-115">"Nome": "ContosoNotificationHub",</span><span class="sxs-lookup"><span data-stu-id="10f89-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="10f89-116">"Posizione": "West US",</span><span class="sxs-lookup"><span data-stu-id="10f89-116">"Location": "West US",</span></span>  
<span data-ttu-id="10f89-117">} Se usato insieme al cmdlet **set-AzNotificationHub** , l'esempio JSON precedente imposta il valore della posizione di un hub di notifica denominato ContosoNotificationHub in West US.</span><span class="sxs-lookup"><span data-stu-id="10f89-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="10f89-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10f89-118">EXAMPLES</span></span>

### <span data-ttu-id="10f89-119">Esempio 1: modificare i valori delle proprietà per un hub di notifica</span><span class="sxs-lookup"><span data-stu-id="10f89-119">Example 1: Modify the property values for a notification hub</span></span>
```powershell
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="10f89-120">Questo comando modifica i valori delle proprietà per un hub di notifica trovato nello spazio dei nomi ContosoNamespace e lo assegna al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="10f89-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="10f89-121">I valori delle proprietà, oltre al nome dell'hub da modificare, non vengono specificati nel comando.</span><span class="sxs-lookup"><span data-stu-id="10f89-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="10f89-122">Queste informazioni sono invece contenute nel file di input C:\Configuration\Hubs.jsattivato.</span><span class="sxs-lookup"><span data-stu-id="10f89-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

### <span data-ttu-id="10f89-123">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="10f89-123">Example 2</span></span>

<span data-ttu-id="10f89-124">Imposta i valori delle proprietà per un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10f89-124">Sets property values for a notification hub.</span></span> <span data-ttu-id="10f89-125">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="10f89-125">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHubObj <NotificationHubAttributes> -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="10f89-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="10f89-126">PARAMETERS</span></span>

### <span data-ttu-id="10f89-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10f89-127">-DefaultProfile</span></span>
<span data-ttu-id="10f89-128">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="10f89-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10f89-129">-Force</span><span class="sxs-lookup"><span data-stu-id="10f89-129">-Force</span></span>
<span data-ttu-id="10f89-130">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="10f89-130">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="10f89-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="10f89-131">-InputFile</span></span>
<span data-ttu-id="10f89-132">Specifica il percorso di un file JSON che contiene le informazioni di configurazione per l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10f89-132">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

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

### <span data-ttu-id="10f89-133">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="10f89-133">-Namespace</span></span>
<span data-ttu-id="10f89-134">Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10f89-134">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="10f89-135">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10f89-135">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="10f89-136">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="10f89-136">-NotificationHubObj</span></span>
<span data-ttu-id="10f89-137">Specifica l'oggetto **NotificationHubAttributes** che contiene le informazioni di configurazione per l'hub modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10f89-137">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="10f89-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="10f89-138">-ResourceGroup</span></span>
<span data-ttu-id="10f89-139">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="10f89-139">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="10f89-140">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che semplificano la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="10f89-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="10f89-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="10f89-141">-Confirm</span></span>
<span data-ttu-id="10f89-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10f89-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10f89-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10f89-143">-WhatIf</span></span>
<span data-ttu-id="10f89-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10f89-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10f89-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10f89-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10f89-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10f89-146">CommonParameters</span></span>
<span data-ttu-id="10f89-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10f89-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10f89-148">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10f89-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10f89-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="10f89-149">INPUTS</span></span>

### <span data-ttu-id="10f89-150">System. String</span><span class="sxs-lookup"><span data-stu-id="10f89-150">System.String</span></span>

## <span data-ttu-id="10f89-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10f89-151">OUTPUTS</span></span>

### <span data-ttu-id="10f89-152">Microsoft. Azure. Commands. NotificationHubs. Models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="10f89-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="10f89-153">Note</span><span class="sxs-lookup"><span data-stu-id="10f89-153">NOTES</span></span>

## <span data-ttu-id="10f89-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10f89-154">RELATED LINKS</span></span>

[<span data-ttu-id="10f89-155">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="10f89-155">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="10f89-156">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="10f89-156">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="10f89-157">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="10f89-157">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)



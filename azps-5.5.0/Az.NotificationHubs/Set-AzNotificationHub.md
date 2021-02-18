---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: 7083c6872981cefaa12dc01612f3eb27cc7676ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206395"
---
# <span data-ttu-id="5add4-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="5add4-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="5add4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5add4-102">SYNOPSIS</span></span>
<span data-ttu-id="5add4-103">Imposta i valori di proprietà per un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5add4-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="5add4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5add4-104">SYNTAX</span></span>

### <span data-ttu-id="5add4-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="5add4-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5add4-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="5add4-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5add4-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5add4-107">DESCRIPTION</span></span>
<span data-ttu-id="5add4-108">Il cmdlet **Set-AzNotificationHub** modifica i valori di proprietà di un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5add4-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="5add4-109">È possibile modificare il valore della proprietà di un hub di notifica in due modi.</span><span class="sxs-lookup"><span data-stu-id="5add4-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="5add4-110">Per un oggetto è possibile creare un'istanza dell'oggetto **NotificationHubAttributes** e quindi configurarlo con i valori delle proprietà che si vuole che il nuovo hub possieda.</span><span class="sxs-lookup"><span data-stu-id="5add4-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="5add4-111">Questa operazione può essere eseguita con .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="5add4-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="5add4-112">È quindi possibile copiare i valori delle proprietà nell'hub tramite il *parametro NotificationHubObj.*</span><span class="sxs-lookup"><span data-stu-id="5add4-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="5add4-113">In alternativa, è possibile creare un file JSON (JavaScript Object Notation) contenente i valori di configurazione pertinenti e quindi applicarlo tramite il *parametro InputFile.*</span><span class="sxs-lookup"><span data-stu-id="5add4-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="5add4-114">Un file JSON è un file di testo che usa una sintassi simile alla seguente: {</span><span class="sxs-lookup"><span data-stu-id="5add4-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="5add4-115">"Name": "ContosoNotificationHub",</span><span class="sxs-lookup"><span data-stu-id="5add4-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="5add4-116">"Luogo": "Stati Uniti occidentali",</span><span class="sxs-lookup"><span data-stu-id="5add4-116">"Location": "West US",</span></span>  
<span data-ttu-id="5add4-117">} Se usato insieme al cmdlet **Set-AzNotificationHub,** l'esempio JSON precedente imposta il valore Location di un hub di notifica denominato ContosoNotificationHub negli Stati Uniti occidentali.</span><span class="sxs-lookup"><span data-stu-id="5add4-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="5add4-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5add4-118">EXAMPLES</span></span>

### <span data-ttu-id="5add4-119">Esempio 1: Modificare i valori delle proprietà per un hub di notifica</span><span class="sxs-lookup"><span data-stu-id="5add4-119">Example 1: Modify the property values for a notification hub</span></span>
```powershell
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="5add4-120">Questo comando modifica i valori delle proprietà per un hub di notifica trovato nello spazio dei nomi ContosoProperty e lo ha assegnato al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="5add4-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="5add4-121">I valori delle proprietà e il nome dell'hub da modificare non sono specificati nel comando.</span><span class="sxs-lookup"><span data-stu-id="5add4-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="5add4-122">Queste informazioni, invece, sono contenute nel file C:\Configuration\Hubs.jsdi input.</span><span class="sxs-lookup"><span data-stu-id="5add4-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

### <span data-ttu-id="5add4-123">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5add4-123">Example 2</span></span>

<span data-ttu-id="5add4-124">Imposta i valori di proprietà per un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5add4-124">Sets property values for a notification hub.</span></span> <span data-ttu-id="5add4-125">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="5add4-125">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHubObj <NotificationHubAttributes> -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="5add4-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5add4-126">PARAMETERS</span></span>

### <span data-ttu-id="5add4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5add4-127">-DefaultProfile</span></span>
<span data-ttu-id="5add4-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="5add4-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5add4-129">-Force</span><span class="sxs-lookup"><span data-stu-id="5add4-129">-Force</span></span>
<span data-ttu-id="5add4-130">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="5add4-130">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5add4-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="5add4-131">-InputFile</span></span>
<span data-ttu-id="5add4-132">Specifica il percorso di un file JSON che contiene informazioni di configurazione per l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5add4-132">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

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

### <span data-ttu-id="5add4-133">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5add4-133">-Namespace</span></span>
<span data-ttu-id="5add4-134">Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5add4-134">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="5add4-135">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5add4-135">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="5add4-136">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="5add4-136">-NotificationHubObj</span></span>
<span data-ttu-id="5add4-137">Specifica **l'oggetto NotificationHubAttributes** che contiene informazioni di configurazione per l'hub modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5add4-137">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5add4-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5add4-138">-ResourceGroup</span></span>
<span data-ttu-id="5add4-139">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="5add4-139">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="5add4-140">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che consentono semplicemente la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5add4-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="5add4-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5add4-141">-Confirm</span></span>
<span data-ttu-id="5add4-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5add4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5add4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5add4-143">-WhatIf</span></span>
<span data-ttu-id="5add4-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5add4-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5add4-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5add4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5add4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5add4-146">CommonParameters</span></span>
<span data-ttu-id="5add4-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5add4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5add4-148">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5add4-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5add4-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="5add4-149">INPUTS</span></span>

### <span data-ttu-id="5add4-150">System.String</span><span class="sxs-lookup"><span data-stu-id="5add4-150">System.String</span></span>

## <span data-ttu-id="5add4-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5add4-151">OUTPUTS</span></span>

### <span data-ttu-id="5add4-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="5add4-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="5add4-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="5add4-153">NOTES</span></span>

## <span data-ttu-id="5add4-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5add4-154">RELATED LINKS</span></span>

[<span data-ttu-id="5add4-155">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="5add4-155">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="5add4-156">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="5add4-156">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="5add4-157">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="5add4-157">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)



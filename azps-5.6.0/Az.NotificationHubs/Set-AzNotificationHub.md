---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: F7BBEF57-0DC2-4EFF-9AA2-119B3BD19AE6
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/set-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHub.md
ms.openlocfilehash: 7f0732225389f5174c2097cea57ed38d9ea2be0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951118"
---
# <span data-ttu-id="36926-101">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="36926-101">Set-AzNotificationHub</span></span>

## <span data-ttu-id="36926-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36926-102">SYNOPSIS</span></span>
<span data-ttu-id="36926-103">Imposta i valori delle proprietà per un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="36926-103">Sets property values for a notification hub.</span></span>

## <span data-ttu-id="36926-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36926-104">SYNTAX</span></span>

### <span data-ttu-id="36926-105">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="36926-105">InputFileParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36926-106">NotificationHubParameterSet</span><span class="sxs-lookup"><span data-stu-id="36926-106">NotificationHubParameterSet</span></span>
```
Set-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36926-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="36926-107">DESCRIPTION</span></span>
<span data-ttu-id="36926-108">Il cmdlet **Set-AzNotificationHub** modifica i valori di proprietà di un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="36926-108">The **Set-AzNotificationHub** cmdlet modifies the property values of a notification hub.</span></span>
<span data-ttu-id="36926-109">È possibile modificare il valore della proprietà di un hub di notifica in due modi.</span><span class="sxs-lookup"><span data-stu-id="36926-109">You can modify a notification hub property value in two ways.</span></span>
<span data-ttu-id="36926-110">Per un oggetto è possibile creare un'istanza dell'oggetto **NotificationHubAttributes** e quindi configurarlo con i valori delle proprietà che si vuole che il nuovo hub possieda.</span><span class="sxs-lookup"><span data-stu-id="36926-110">For one, you can create an instance of the **NotificationHubAttributes** object and then configure that object with the property values you want the new hub to possess.</span></span>
<span data-ttu-id="36926-111">Questa operazione può essere eseguita tramite la .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="36926-111">This can be done through the .NET Framework.</span></span>
<span data-ttu-id="36926-112">È quindi possibile copiare i valori delle proprietà nell'hub tramite il parametro *NotificationHubObj.*</span><span class="sxs-lookup"><span data-stu-id="36926-112">You can then copy those property values to your hub by through the *NotificationHubObj* parameter.</span></span>
<span data-ttu-id="36926-113">In alternativa, è possibile creare un file JSON (JavaScript Object Notation) contenente i valori di configurazione pertinenti e quindi applicarlo tramite il *parametro InputFile.*</span><span class="sxs-lookup"><span data-stu-id="36926-113">Alternatively, you can create a JSON (JavaScript Object Notation) file that contains the relevant configuration values, then apply those values by through the *InputFile* parameter.</span></span>
<span data-ttu-id="36926-114">Un file JSON è un file di testo che usa una sintassi simile alla seguente: {</span><span class="sxs-lookup"><span data-stu-id="36926-114">A JSON file is a text file that uses syntax similar to the following: {</span></span>  
    <span data-ttu-id="36926-115">"Name": "ContosoNotificationHub",</span><span class="sxs-lookup"><span data-stu-id="36926-115">"Name": "ContosoNotificationHub",</span></span>  
    <span data-ttu-id="36926-116">"Luogo": "Stati Uniti occidentali",</span><span class="sxs-lookup"><span data-stu-id="36926-116">"Location": "West US",</span></span>  
<span data-ttu-id="36926-117">} Se usato insieme al cmdlet **Set-AzNotificationHub,** l'esempio JSON precedente imposta il valore Location di un hub di notifica denominato ContosoNotificationHub negli Stati Uniti occidentali.</span><span class="sxs-lookup"><span data-stu-id="36926-117">} When used in conjunction with the **Set-AzNotificationHub** cmdlet, the preceding JSON sample sets the Location value of a notification hub named ContosoNotificationHub to West US.</span></span>

## <span data-ttu-id="36926-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36926-118">EXAMPLES</span></span>

### <span data-ttu-id="36926-119">Esempio 1: Modificare i valori delle proprietà per un hub di notifica</span><span class="sxs-lookup"><span data-stu-id="36926-119">Example 1: Modify the property values for a notification hub</span></span>
```powershell
PS C:\>Set-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\Hubs.json"
```

<span data-ttu-id="36926-120">Questo comando modifica i valori delle proprietà per un hub di notifica trovato nello spazio dei nomi ContosoProperty e lo ha assegnato al gruppo di risorse ContosoNotificationsGroup.</span><span class="sxs-lookup"><span data-stu-id="36926-120">This command modifies the property values for a notification hub found in the ContosoNamespace namespace and assigned it to the resource group ContosoNotificationsGroup.</span></span>
<span data-ttu-id="36926-121">I valori delle proprietà e il nome dell'hub da modificare non sono specificati nel comando.</span><span class="sxs-lookup"><span data-stu-id="36926-121">The property values, as well as the name of the hub to be modified, are not specified in the command.</span></span>
<span data-ttu-id="36926-122">Queste informazioni, invece, sono contenute nel file C:\Configuration\Hubs.jsdi input.</span><span class="sxs-lookup"><span data-stu-id="36926-122">Instead, that information is contained in the input file C:\Configuration\Hubs.json.</span></span>

### <span data-ttu-id="36926-123">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="36926-123">Example 2</span></span>

<span data-ttu-id="36926-124">Imposta i valori delle proprietà per un hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="36926-124">Sets property values for a notification hub.</span></span> <span data-ttu-id="36926-125">(autogenerati)</span><span class="sxs-lookup"><span data-stu-id="36926-125">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHubObj <NotificationHubAttributes> -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="36926-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36926-126">PARAMETERS</span></span>

### <span data-ttu-id="36926-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36926-127">-DefaultProfile</span></span>
<span data-ttu-id="36926-128">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="36926-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36926-129">-Force</span><span class="sxs-lookup"><span data-stu-id="36926-129">-Force</span></span>
<span data-ttu-id="36926-130">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="36926-130">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="36926-131">-InputFile</span><span class="sxs-lookup"><span data-stu-id="36926-131">-InputFile</span></span>
<span data-ttu-id="36926-132">Specifica il percorso di un file JSON che contiene informazioni di configurazione per l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="36926-132">Specifies the path to a JSON file that contains configuration information for the notification hub.</span></span>

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

### <span data-ttu-id="36926-133">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="36926-133">-Namespace</span></span>
<span data-ttu-id="36926-134">Specifica lo spazio dei nomi a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="36926-134">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="36926-135">Gli spazi dei nomi consentono di raggruppare e categorizzare gli hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="36926-135">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="36926-136">-NotificationHubObj</span><span class="sxs-lookup"><span data-stu-id="36926-136">-NotificationHubObj</span></span>
<span data-ttu-id="36926-137">Specifica **l'oggetto NotificationHubAttributes** che contiene informazioni di configurazione per l'hub modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36926-137">Specifies the **NotificationHubAttributes** object that contains configuration information for the hub that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="36926-138">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="36926-138">-ResourceGroup</span></span>
<span data-ttu-id="36926-139">Specifica il gruppo di risorse a cui è assegnato l'hub di notifica.</span><span class="sxs-lookup"><span data-stu-id="36926-139">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="36926-140">I gruppi di risorse organizzano elementi come gli spazi dei nomi, gli hub di notifica e le regole di autorizzazione in modi che consentono semplicemente la gestione dell'inventario e l'amministrazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="36926-140">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="36926-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36926-141">-Confirm</span></span>
<span data-ttu-id="36926-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36926-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36926-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36926-143">-WhatIf</span></span>
<span data-ttu-id="36926-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36926-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36926-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36926-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36926-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36926-146">CommonParameters</span></span>
<span data-ttu-id="36926-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36926-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36926-148">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36926-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36926-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="36926-149">INPUTS</span></span>

### <span data-ttu-id="36926-150">System.String</span><span class="sxs-lookup"><span data-stu-id="36926-150">System.String</span></span>

## <span data-ttu-id="36926-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36926-151">OUTPUTS</span></span>

### <span data-ttu-id="36926-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="36926-152">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="36926-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="36926-153">NOTES</span></span>

## <span data-ttu-id="36926-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36926-154">RELATED LINKS</span></span>

[<span data-ttu-id="36926-155">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="36926-155">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="36926-156">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="36926-156">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="36926-157">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="36926-157">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)



---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F92D18AC-B716-42CA-9C2D-1AB5A599F73E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2fdd1063450615b729fade77c7edb51ad93bec77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029558"
---
# <span data-ttu-id="68370-101">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="68370-101">Remove-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="68370-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68370-102">SYNOPSIS</span></span>
<span data-ttu-id="68370-103">Elimina un record di controllo di Access dalla configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="68370-103">Deletes an access control record from the service configuration.</span></span>

## <span data-ttu-id="68370-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68370-104">SYNTAX</span></span>

### <span data-ttu-id="68370-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="68370-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleAccessControlRecord -ACRName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="68370-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="68370-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleAccessControlRecord -ACR <AccessControlRecord> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="68370-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68370-107">DESCRIPTION</span></span>
<span data-ttu-id="68370-108">Il cmdlet **Remove-AzureStorSimpleAccessControlRecord** Elimina un record di controllo di Access dalla configurazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="68370-108">The **Remove-AzureStorSimpleAccessControlRecord** cmdlet deletes an access control record from the service configuration.</span></span>

## <span data-ttu-id="68370-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68370-109">EXAMPLES</span></span>

### <span data-ttu-id="68370-110">Esempio 1: rimuovere un controllo di AccessoRecord di Access Controlaccess Control</span><span class="sxs-lookup"><span data-stu-id="68370-110">Example 1: Remove an Access Controlaccess control recordaccess control</span></span>
```
PS C:\>Remove-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -WaitForComplete -Force
VERBOSE: ClientRequestId: 574aeb7f-fbc9-46d5-bc68-1bfe4487bd8b_PS
VERBOSE: ClientRequestId: 985afe84-ef95-47cb-8c8f-df094530334b_PS
VERBOSE: About to run a job to remove your ACR! 
VERBOSE: ClientRequestId: 7eb7e1a0-2288-44da-b64c-5bf86a6b9aaf_PS


JobId        : f7934db5-8363-4152-b38e-b9a5d91f97b9
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your delete operation has completed successfully.
```

<span data-ttu-id="68370-111">Questo comando Elimina il record di controllo di accesso denominato Acr10.</span><span class="sxs-lookup"><span data-stu-id="68370-111">This command deletes the access control record named Acr10.</span></span>
<span data-ttu-id="68370-112">Questo comando specifica il parametro *WaitForComplete* e, di conseguenza, il comando attende fino al completamento dell'operazione e quindi restituisce un oggetto **TaskStatusInfo** .</span><span class="sxs-lookup"><span data-stu-id="68370-112">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="68370-113">Esempio 2: rimuovere un record di controllo di Controlaccess di Access usando il controllo Controlaccess Controlaccess pipelineAccess</span><span class="sxs-lookup"><span data-stu-id="68370-113">Example 2: Remove an Access Controlaccess control record by using the pipelineAccess Controlaccess controlaccess control</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr10" | Remove-AzureStorSimpleAccessControlRecord -Force 
VERBOSE: ClientRequestId: ff8d8bd6-4c92-4ab6-8fde-e9344a253da3_PS
VERBOSE: ClientRequestId: f71c74f3-33b9-40d1-b8d5-12363e98412f_PS
VERBOSE: ClientRequestId: d5d809d0-ec22-4e45-97ee-a56edc41e503_PS
VERBOSE: About to create a job to remove your ACR! 
VERBOSE: ClientRequestId: 6ffa6bc8-37b3-49ff-bafc-721b360f09cb_PS
294a0208-a43f-4d80-b824-2319cd77c5e6
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
294a0208-a43f-4d80-b824-2319cd77c5e6 for tracking the task's status
```

<span data-ttu-id="68370-114">Questo comando USA **Get-AzureStorSimpleAccessControlRecord** per ottenere il **AccessControlRecord** denominato Acr10 e quindi passa tale oggetto al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="68370-114">This command uses the **Get-AzureStorSimpleAccessControlRecord** to get the **AccessControlRecord** named Acr10, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="68370-115">Il comando avvia l'operazione che rimuove l'oggetto **AccessControlRecord** e quindi restituisce un oggetto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="68370-115">The command starts the operation that removes the **AccessControlRecord** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="68370-116">Per visualizzare lo stato dell'attività, usa il cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="68370-116">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="68370-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68370-117">PARAMETERS</span></span>

### <span data-ttu-id="68370-118">-ACR</span><span class="sxs-lookup"><span data-stu-id="68370-118">-ACR</span></span>
<span data-ttu-id="68370-119">Specifica un oggetto **AccessControlRecord** da eliminare.</span><span class="sxs-lookup"><span data-stu-id="68370-119">Specifies an **AccessControlRecord** object to delete.</span></span>
<span data-ttu-id="68370-120">Per ottenere un oggetto **AccessControlRecord** , usa il cmdlet **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="68370-120">To obtain an **AccessControlRecord** object, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>

```yaml
Type: AccessControlRecord
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68370-121">-ACRName</span><span class="sxs-lookup"><span data-stu-id="68370-121">-ACRName</span></span>
<span data-ttu-id="68370-122">Specifica un nome del record di controllo di Access da eliminare.</span><span class="sxs-lookup"><span data-stu-id="68370-122">Specifies a name of the access control record to delete.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68370-123">-Force</span><span class="sxs-lookup"><span data-stu-id="68370-123">-Force</span></span>
<span data-ttu-id="68370-124">Indica che questo cmdlet non richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="68370-124">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="68370-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="68370-125">-Profile</span></span>
<span data-ttu-id="68370-126">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="68370-126">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68370-127">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="68370-127">-WaitForComplete</span></span>
<span data-ttu-id="68370-128">Indica che questo cmdlet attende che l'operazione venga completata prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="68370-128">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="68370-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68370-129">CommonParameters</span></span>
<span data-ttu-id="68370-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68370-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68370-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68370-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68370-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68370-132">INPUTS</span></span>

### <span data-ttu-id="68370-133">AccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="68370-133">AccessControlRecord</span></span>
<span data-ttu-id="68370-134">Questo cmdlet accetta un oggetto **AccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="68370-134">This cmdlet accepts an **AccessControlRecord** object.</span></span>
<span data-ttu-id="68370-135">Un oggetto **AccessControlRecord** contiene i campi seguenti:</span><span class="sxs-lookup"><span data-stu-id="68370-135">An **AccessControlRecord** object contains the following fields:</span></span> 

- <span data-ttu-id="68370-136">**GlobalId** ( **stringa** )</span><span class="sxs-lookup"><span data-stu-id="68370-136">**GlobalId** ( **String** )</span></span> 
- <span data-ttu-id="68370-137">**Initiatorname** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="68370-137">**InitiatorName** ( **String** )</span></span> 
- <span data-ttu-id="68370-138">**InstanceID** ( **String** )</span><span class="sxs-lookup"><span data-stu-id="68370-138">**InstanceId** ( **String** )</span></span> 
- <span data-ttu-id="68370-139">**Nome** ( **stringa** )</span><span class="sxs-lookup"><span data-stu-id="68370-139">**Name** ( **String** )</span></span> 
- <span data-ttu-id="68370-140">**OperationInProgress** ( **OperationInProgress** )</span><span class="sxs-lookup"><span data-stu-id="68370-140">**OperationInProgress** ( **OperationInProgress** )</span></span> 
- <span data-ttu-id="68370-141">**VolumeCount** ( **int** )</span><span class="sxs-lookup"><span data-stu-id="68370-141">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="68370-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68370-142">OUTPUTS</span></span>

### <span data-ttu-id="68370-143">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="68370-143">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="68370-144">Questo cmdlet restituisce un oggetto **TaskStatusInfo** se specifichi il parametro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="68370-144">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="68370-145">Se non specifichi tale parametro, restituisce un oggetto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="68370-145">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="68370-146">Note</span><span class="sxs-lookup"><span data-stu-id="68370-146">NOTES</span></span>

## <span data-ttu-id="68370-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68370-147">RELATED LINKS</span></span>

[<span data-ttu-id="68370-148">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="68370-148">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="68370-149">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="68370-149">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="68370-150">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="68370-150">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="68370-151">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="68370-151">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)



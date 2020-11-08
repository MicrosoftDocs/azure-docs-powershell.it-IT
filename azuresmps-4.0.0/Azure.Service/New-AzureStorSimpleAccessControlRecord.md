---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: ED6CDEA3-0A5D-47E6-B9D7-47D1862212DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: b907627200ec2463d997ebb4faa834e2821b1c7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029672"
---
# <span data-ttu-id="9cef0-101">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="9cef0-101">New-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="9cef0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9cef0-102">SYNOPSIS</span></span>
<span data-ttu-id="9cef0-103">Crea un record di controllo di Access.</span><span class="sxs-lookup"><span data-stu-id="9cef0-103">Creates an access control record.</span></span>

## <span data-ttu-id="9cef0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9cef0-104">SYNTAX</span></span>

```
New-AzureStorSimpleAccessControlRecord -ACRName <String> -IQNInitiatorName <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9cef0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9cef0-105">DESCRIPTION</span></span>
<span data-ttu-id="9cef0-106">Il cmdlet **New-AzureStorSimpleAccessControlRecord** crea un record di controllo di Access.</span><span class="sxs-lookup"><span data-stu-id="9cef0-106">The **New-AzureStorSimpleAccessControlRecord** cmdlet creates an access control record.</span></span>
<span data-ttu-id="9cef0-107">Puoi usare un oggetto **AccessControlRecord** per configurare i volumi.</span><span class="sxs-lookup"><span data-stu-id="9cef0-107">You can use an **AccessControlRecord** object to configure volumes.</span></span>

## <span data-ttu-id="9cef0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9cef0-108">EXAMPLES</span></span>

### <span data-ttu-id="9cef0-109">Esempio 1: creare un record di controllo di Controlaccess di Access e attendere il controllo resultaccess</span><span class="sxs-lookup"><span data-stu-id="9cef0-109">Example 1: Create an Access Controlaccess control record and wait for the resultaccess control</span></span>
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -IQNInitiatorName "Iqn10" -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 08719243-3a76-43a5-a88b-e5f2b63ed3d9
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e12362c2c06615108ba8436cf85fcd40
```

<span data-ttu-id="9cef0-110">Questo comando crea un record di controllo di Access denominato Acr10 per l'iniziatore iSCSI denominato Iqn10.</span><span class="sxs-lookup"><span data-stu-id="9cef0-110">This command creates an access control record named Acr10 for the iSCSI initiator named Iqn10.</span></span>
<span data-ttu-id="9cef0-111">Questo comando specifica il parametro *WaitForComplete* e, di conseguenza, il comando attende fino al completamento dell'operazione e quindi restituisce un oggetto **TaskStatusInfo** .</span><span class="sxs-lookup"><span data-stu-id="9cef0-111">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="9cef0-112">Esempio 2: creare un controllo di controllo AccessoRecord di Access Controlaccess</span><span class="sxs-lookup"><span data-stu-id="9cef0-112">Example 2: Create an Access Controlaccess control recordaccess control</span></span>
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr11" -IQNInitiatorName "Iqn11"
VERBOSE: The create job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
2bd56fbb-4b95-4f2c-b99f-6321231a018d for tracking the job status
```

<span data-ttu-id="9cef0-113">Questo comando crea un record di controllo di Access denominato Acr11 per l'iniziatore iSCSI denominato Iqn11.</span><span class="sxs-lookup"><span data-stu-id="9cef0-113">This command creates an access control record named Acr11 for the iSCSI initiator named Iqn11.</span></span>
<span data-ttu-id="9cef0-114">Questo comando non specifica il parametro *WaitForComplete* e quindi il comando avvia l'attività e quindi restituisce un oggetto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="9cef0-114">This command does not specify the *WaitForComplete* parameter, and, therefore, the command starts the task, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="9cef0-115">Per visualizzare lo stato dell'attività, usa il cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="9cef0-115">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="9cef0-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9cef0-116">PARAMETERS</span></span>

### <span data-ttu-id="9cef0-117">-ACRName</span><span class="sxs-lookup"><span data-stu-id="9cef0-117">-ACRName</span></span>
<span data-ttu-id="9cef0-118">Specifica un nome per il record di controllo di Access.</span><span class="sxs-lookup"><span data-stu-id="9cef0-118">Specifies a name for the access control record.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cef0-119">-IQNInitiatorName</span><span class="sxs-lookup"><span data-stu-id="9cef0-119">-IQNInitiatorName</span></span>
<span data-ttu-id="9cef0-120">Specifica il nome completo iSCSI (IQN) dell'iniziatore iSCSI a cui questo cmdlet fornisce l'accesso per il volume.</span><span class="sxs-lookup"><span data-stu-id="9cef0-120">Specifies the iSCSI qualified name (IQN) of the iSCSI initiator to which this cmdlet provides access for the volume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IQN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cef0-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="9cef0-121">-Profile</span></span>
<span data-ttu-id="9cef0-122">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="9cef0-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="9cef0-123">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="9cef0-123">-WaitForComplete</span></span>
<span data-ttu-id="9cef0-124">Indica che questo cmdlet attende che l'operazione venga completata prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9cef0-124">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="9cef0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cef0-125">CommonParameters</span></span>
<span data-ttu-id="9cef0-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cef0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cef0-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cef0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cef0-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9cef0-128">INPUTS</span></span>

### <span data-ttu-id="9cef0-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9cef0-129">None</span></span>

## <span data-ttu-id="9cef0-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9cef0-130">OUTPUTS</span></span>

### <span data-ttu-id="9cef0-131">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="9cef0-131">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="9cef0-132">Questo cmdlet restituisce un oggetto **TaskStatusInfo** se specifichi il parametro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="9cef0-132">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="9cef0-133">Se non specifichi tale parametro, restituisce un oggetto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="9cef0-133">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="9cef0-134">Note</span><span class="sxs-lookup"><span data-stu-id="9cef0-134">NOTES</span></span>

## <span data-ttu-id="9cef0-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9cef0-135">RELATED LINKS</span></span>

[<span data-ttu-id="9cef0-136">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="9cef0-136">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="9cef0-137">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="9cef0-137">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="9cef0-138">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="9cef0-138">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="9cef0-139">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="9cef0-139">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)



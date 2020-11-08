---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71CFCA9D-198E-481A-BB85-159477F25322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c050ea91cc85a89702fb6cf62f05779db7155e4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023816"
---
# <span data-ttu-id="8c2ed-101">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="8c2ed-101">Set-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="8c2ed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8c2ed-102">SYNOPSIS</span></span>
<span data-ttu-id="8c2ed-103">Aggiorna la IQN di un record di controllo di Access.</span><span class="sxs-lookup"><span data-stu-id="8c2ed-103">Updates the IQN of an access control record.</span></span>

## <span data-ttu-id="8c2ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c2ed-104">SYNTAX</span></span>

```
Set-AzureStorSimpleAccessControlRecord -ACRName <String> -IQNInitiatorName <String> [-WaitForComplete]
 [-NewName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8c2ed-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c2ed-105">DESCRIPTION</span></span>
<span data-ttu-id="8c2ed-106">Il cmdlet **set-AzureStorSimpleAccessControlRecord** aggiorna il nome completo iSCSI (IQN) di un record di controllo di Access esistente.</span><span class="sxs-lookup"><span data-stu-id="8c2ed-106">The **Set-AzureStorSimpleAccessControlRecord** cmdlet updates the iSCSI qualified name (IQN) of an existing access control record.</span></span>

## <span data-ttu-id="8c2ed-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c2ed-107">EXAMPLES</span></span>

### <span data-ttu-id="8c2ed-108">Esempio 1: aggiornare un record di controllo di Access</span><span class="sxs-lookup"><span data-stu-id="8c2ed-108">Example 1: Update an access control record</span></span>
```
PS C:\>Set-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -IQNInitiatorName "IqnUpdated" -WaitForComplete
VERBOSE: ClientRequestId: e4766335-f302-40e0-93bf-fad7aa488ae6_PS
VERBOSE: ClientRequestId: cfdbbd67-6ba5-4238-b743-b88f604079b9_PS
VERBOSE: About to run a task to update your Access Control Record! 
VERBOSE: ClientRequestId: d5cf2793-0ab5-40ff-ab6f-43e21bc4c0a4_PS


JobId        : 89502523-52fc-4ce2-b2d4-cb8c6692fb60
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: cbd47519-3a3c-4365-b097-0fb7551c48ee_PS
GlobalId            : 
InitiatorName       : IqnUpdated
InstanceId          : 9bcfbc83-e196-4688-9016-827f51515c24
Name                : Acr10
OperationInProgress : None
VolumeCount         : 0
```

<span data-ttu-id="8c2ed-109">Questo comando Aggiorna il record di controllo di accesso denominato Acr10 per l'iniziatore iSCSI denominato IqnUpdated.</span><span class="sxs-lookup"><span data-stu-id="8c2ed-109">This command updates the access control record named Acr10 for the iSCSI initiator named IqnUpdated.</span></span>
<span data-ttu-id="8c2ed-110">Questo comando specifica il parametro *WaitForComplete* e, di conseguenza, il comando attende fino al completamento dell'operazione e quindi restituisce un oggetto **TaskStatusInfo** .</span><span class="sxs-lookup"><span data-stu-id="8c2ed-110">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

## <span data-ttu-id="8c2ed-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8c2ed-111">PARAMETERS</span></span>

### <span data-ttu-id="8c2ed-112">-ACRName</span><span class="sxs-lookup"><span data-stu-id="8c2ed-112">-ACRName</span></span>
<span data-ttu-id="8c2ed-113">Specifica un nome del record di controllo di Access da modificare.</span><span class="sxs-lookup"><span data-stu-id="8c2ed-113">Specifies a name of the access control record to modify.</span></span>

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

### <span data-ttu-id="8c2ed-114">-IQNInitiatorName</span><span class="sxs-lookup"><span data-stu-id="8c2ed-114">-IQNInitiatorName</span></span>
<span data-ttu-id="8c2ed-115">Specifica il IQN dell'initiator iSCSI a cui questo cmdlet fornisce l'accesso per il volume.</span><span class="sxs-lookup"><span data-stu-id="8c2ed-115">Specifies the IQN of the iSCSI initiator to which this cmdlet provides access for the volume.</span></span>

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

### <span data-ttu-id="8c2ed-116">-NewName</span><span class="sxs-lookup"><span data-stu-id="8c2ed-116">-NewName</span></span>
<span data-ttu-id="8c2ed-117">Specifica un nuovo nome per il record di controllo di Access.</span><span class="sxs-lookup"><span data-stu-id="8c2ed-117">Specifies a new name for access control record.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c2ed-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="8c2ed-118">-Profile</span></span>
<span data-ttu-id="8c2ed-119">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="8c2ed-119">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="8c2ed-120">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="8c2ed-120">-WaitForComplete</span></span>
<span data-ttu-id="8c2ed-121">Indica che questo cmdlet attende che l'operazione venga completata prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8c2ed-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="8c2ed-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c2ed-122">CommonParameters</span></span>
<span data-ttu-id="8c2ed-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c2ed-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c2ed-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c2ed-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c2ed-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8c2ed-125">INPUTS</span></span>

### <span data-ttu-id="8c2ed-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8c2ed-126">None</span></span>

## <span data-ttu-id="8c2ed-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c2ed-127">OUTPUTS</span></span>

### <span data-ttu-id="8c2ed-128">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="8c2ed-128">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="8c2ed-129">Questo cmdlet restituisce un oggetto **TaskStatusInfo** se specifichi il parametro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="8c2ed-129">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="8c2ed-130">Se non specifichi tale parametro, restituisce un oggetto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="8c2ed-130">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="8c2ed-131">Note</span><span class="sxs-lookup"><span data-stu-id="8c2ed-131">NOTES</span></span>

## <span data-ttu-id="8c2ed-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c2ed-132">RELATED LINKS</span></span>

[<span data-ttu-id="8c2ed-133">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="8c2ed-133">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="8c2ed-134">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="8c2ed-134">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="8c2ed-135">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="8c2ed-135">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)



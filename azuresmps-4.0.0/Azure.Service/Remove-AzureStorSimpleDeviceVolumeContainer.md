---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: C50959BB-7481-4898-BF4B-C5ABF8758473
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2c06455004afbd15235f59164034abc2147964b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029915"
---
# <span data-ttu-id="8e1d1-101">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="8e1d1-101">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="8e1d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8e1d1-102">SYNOPSIS</span></span>
<span data-ttu-id="8e1d1-103">Rimuove un contenitore di volumi da un dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="8e1d1-103">Removes a volume container from a StorSimple device.</span></span>

## <span data-ttu-id="8e1d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e1d1-104">SYNTAX</span></span>

```
Remove-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainer <DataContainer>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8e1d1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8e1d1-105">DESCRIPTION</span></span>
<span data-ttu-id="8e1d1-106">Il cmdlet **Remove-AzureStorSimpleDeviceVolumeContainer** rimuove un oggetto contenitore di volumi da un dispositivo StorSimple.</span><span class="sxs-lookup"><span data-stu-id="8e1d1-106">The **Remove-AzureStorSimpleDeviceVolumeContainer** cmdlet removes a volume container object from a StorSimple device.</span></span>
<span data-ttu-id="8e1d1-107">Questo cmdlet richiede la conferma a meno che non specifichi il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="8e1d1-107">This cmdlet prompts you for confirmation unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="8e1d1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e1d1-108">EXAMPLES</span></span>

### <span data-ttu-id="8e1d1-109">Esempio 1: rimuovere un contenitore tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="8e1d1-109">Example 1: Remove a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" | Remove-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -Force
VERBOSE: ClientRequestId: 0efbb4fc-ceb0-4311-bc49-0e08161d0a37_PS
VERBOSE: ClientRequestId: bf5b615f-47e3-4868-91b6-f2d12217a302_PS
VERBOSE: ClientRequestId: 5590c87e-0602-4197-b6c3-cf58b0e7a7b3_PS
VERBOSE: ClientRequestId: b33c71ac-c345-44ff-8213-d7fdf9f8480a_PS
VERBOSE: ClientRequestId: 903d42ef-58f4-4e89-ba7f-5f234262356d_PS
VERBOSE: About to create a job to remove your Volume container! 
VERBOSE: ClientRequestId: 2279575f-5115-4344-9c6f-9ef599bd203e_PS
e9ddec89-67ac-4e2e-a2ed-820de3547bb0
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
e9ddec89-67ac-4e2e-a2ed-820de3547bb0 for tracking the task's status
VERBOSE: Volume container with name: Container08 is found.
```

<span data-ttu-id="8e1d1-110">Questo comando ottiene il contenitore del volume denominato Container08 nel dispositivo denominato Contoso63-AppVm usando il cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="8e1d1-110">This command gets the volume container named Container08 on the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="8e1d1-111">Il comando passa il contenitore del volume al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e1d1-111">The command passes the volume container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8e1d1-112">Questo comando avvia l'attività per rimuovere il contenitore e quindi restituisce un oggetto **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="8e1d1-112">This command starts the task to remove the container, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="8e1d1-113">Per visualizzare lo stato dell'attività, usa il cmdlet **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="8e1d1-113">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>
<span data-ttu-id="8e1d1-114">Questo comando specifica il parametro *Force* , quindi non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="8e1d1-114">This command specifies the *Force* parameter, so it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8e1d1-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8e1d1-115">PARAMETERS</span></span>

### <span data-ttu-id="8e1d1-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8e1d1-116">-DeviceName</span></span>
<span data-ttu-id="8e1d1-117">Specifica il nome del dispositivo StorSimple in cui il contenitore di volumi da rimuovere esiste.</span><span class="sxs-lookup"><span data-stu-id="8e1d1-117">Specifies the name of the StorSimple device on which to the volume container to remove exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e1d1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8e1d1-118">-Force</span></span>
<span data-ttu-id="8e1d1-119">Indica che questo cmdlet non richiede la conferma.</span><span class="sxs-lookup"><span data-stu-id="8e1d1-119">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="8e1d1-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="8e1d1-120">-Profile</span></span>
<span data-ttu-id="8e1d1-121">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="8e1d1-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="8e1d1-122">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="8e1d1-122">-VolumeContainer</span></span>
<span data-ttu-id="8e1d1-123">Specifica il contenitore del volume da rimuovere, come oggetto **DataContainer** .</span><span class="sxs-lookup"><span data-stu-id="8e1d1-123">Specifies the volume container to remove, as a **DataContainer** object.</span></span>
<span data-ttu-id="8e1d1-124">Per ottenere un oggetto **DataContainer** , usa il cmdlet **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="8e1d1-124">To obtain a **DataContainer** object, use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e1d1-125">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="8e1d1-125">-WaitForComplete</span></span>
<span data-ttu-id="8e1d1-126">Indica che questo cmdlet attende che l'operazione venga completata prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8e1d1-126">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="8e1d1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e1d1-127">CommonParameters</span></span>
<span data-ttu-id="8e1d1-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e1d1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e1d1-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e1d1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e1d1-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8e1d1-130">INPUTS</span></span>

### <span data-ttu-id="8e1d1-131">DataContainer</span><span class="sxs-lookup"><span data-stu-id="8e1d1-131">DataContainer</span></span>
<span data-ttu-id="8e1d1-132">Questo cmdlet accetta un oggetto **DataContainer** da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8e1d1-132">This cmdlet accepts a **DataContainer** object to remove.</span></span>

## <span data-ttu-id="8e1d1-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e1d1-133">OUTPUTS</span></span>

### <span data-ttu-id="8e1d1-134">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="8e1d1-134">TaskStatusInfo</span></span>
<span data-ttu-id="8e1d1-135">Questo cmdlet restituisce un oggetto **TaskStatusInfo** , se specifichi il parametro *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="8e1d1-135">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="8e1d1-136">Note</span><span class="sxs-lookup"><span data-stu-id="8e1d1-136">NOTES</span></span>

## <span data-ttu-id="8e1d1-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e1d1-137">RELATED LINKS</span></span>

[<span data-ttu-id="8e1d1-138">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="8e1d1-138">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="8e1d1-139">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="8e1d1-139">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)



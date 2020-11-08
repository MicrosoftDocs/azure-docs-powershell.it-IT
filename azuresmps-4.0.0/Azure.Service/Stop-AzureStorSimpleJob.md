---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A1E143A8-70F2-4158-9A10-F2082AD62A73
online version: ''
schema: 2.0.0
ms.openlocfilehash: 371291f4bd33809bc2f5880e4380c448219ed37a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029474"
---
# <span data-ttu-id="3d6f3-101">Stop-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="3d6f3-101">Stop-AzureStorSimpleJob</span></span>

## <span data-ttu-id="3d6f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3d6f3-102">SYNOPSIS</span></span>
<span data-ttu-id="3d6f3-103">Interrompe un processo di StorSimple.</span><span class="sxs-lookup"><span data-stu-id="3d6f3-103">Stops a StorSimple job.</span></span>

## <span data-ttu-id="3d6f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d6f3-104">SYNTAX</span></span>

```
Stop-AzureStorSimpleJob -InstanceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3d6f3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d6f3-105">DESCRIPTION</span></span>
<span data-ttu-id="3d6f3-106">Il cmdlet **Stop-AzureStorSimpleJob** arresta un processo StorSimple in corso.</span><span class="sxs-lookup"><span data-stu-id="3d6f3-106">The **Stop-AzureStorSimpleJob** cmdlet stops an on-going StorSimple job.</span></span>
<span data-ttu-id="3d6f3-107">Puoi specificare i processi fornendo un ID istanza o un nome processo.</span><span class="sxs-lookup"><span data-stu-id="3d6f3-107">You can specify a jobs by supplying an instance ID or a job name.</span></span>

## <span data-ttu-id="3d6f3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d6f3-108">EXAMPLES</span></span>

### <span data-ttu-id="3d6f3-109">Esempio 1: arrestare i processi per un dispositivo</span><span class="sxs-lookup"><span data-stu-id="3d6f3-109">Example 1: Stop jobs for a device</span></span>
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" | Stop-AzureStorSimpleJob -Force
```

<span data-ttu-id="3d6f3-110">Questo comando ottiene i processi per il dispositivo denominato Device07, usando il cmdlet **Get-AzureStorSimpleJob** .</span><span class="sxs-lookup"><span data-stu-id="3d6f3-110">This command gets the jobs for the device named Device07, by using the **Get-AzureStorSimpleJob** cmdlet.</span></span>
<span data-ttu-id="3d6f3-111">Il comando passa i processi al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="3d6f3-111">The command passes the jobs to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3d6f3-112">Il cmdlet corrente interrompe i processi passati al comando.</span><span class="sxs-lookup"><span data-stu-id="3d6f3-112">The current cmdlet stops any jobs that the command passes to it.</span></span>
<span data-ttu-id="3d6f3-113">Il comando specifica il parametro *Force* e quindi non chiede conferma prima di arrestare un processo.</span><span class="sxs-lookup"><span data-stu-id="3d6f3-113">The command specifies the *Force* parameter, and, so, it does not prompt you for confirmation before it stops a job.</span></span>

### <span data-ttu-id="3d6f3-114">Esempio 2: interrompere un processo specifico</span><span class="sxs-lookup"><span data-stu-id="3d6f3-114">Example 2: Stop a specific job</span></span>
```
PS C:\>Stop-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d" -Force
```

<span data-ttu-id="3d6f3-115">Questo comando interrompe il processo con l'ID istanza specificato.</span><span class="sxs-lookup"><span data-stu-id="3d6f3-115">This command stops the job that has the specified instance ID.</span></span>

## <span data-ttu-id="3d6f3-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3d6f3-116">PARAMETERS</span></span>

### <span data-ttu-id="3d6f3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3d6f3-117">-Force</span></span>
<span data-ttu-id="3d6f3-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3d6f3-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3d6f3-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="3d6f3-119">-InstanceId</span></span>
<span data-ttu-id="3d6f3-120">Specifica l'ID del processo del dispositivo da interrompere.</span><span class="sxs-lookup"><span data-stu-id="3d6f3-120">Specifies the ID of the device job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d6f3-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="3d6f3-121">-Profile</span></span>
<span data-ttu-id="3d6f3-122">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="3d6f3-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="3d6f3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d6f3-123">CommonParameters</span></span>
<span data-ttu-id="3d6f3-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d6f3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d6f3-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d6f3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d6f3-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3d6f3-126">INPUTS</span></span>

### <span data-ttu-id="3d6f3-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3d6f3-127">None</span></span>

## <span data-ttu-id="3d6f3-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d6f3-128">OUTPUTS</span></span>

### <span data-ttu-id="3d6f3-129">DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="3d6f3-129">DeviceJobDetails</span></span>
<span data-ttu-id="3d6f3-130">Questo cmdlet ottiene i dettagli della **DeviceJob** che questo cmdlet si arresta.</span><span class="sxs-lookup"><span data-stu-id="3d6f3-130">This cmdlet gets details of the **DeviceJob** that this cmdlet stops.</span></span>

## <span data-ttu-id="3d6f3-131">Note</span><span class="sxs-lookup"><span data-stu-id="3d6f3-131">NOTES</span></span>

## <span data-ttu-id="3d6f3-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d6f3-132">RELATED LINKS</span></span>

[<span data-ttu-id="3d6f3-133">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="3d6f3-133">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)



---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 5d56c0523077ee8a45b2a41175ca54c5a0e10907
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521505"
---
# <span data-ttu-id="3dc0a-101">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3dc0a-101">New-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="3dc0a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3dc0a-102">SYNOPSIS</span></span>
<span data-ttu-id="3dc0a-103">Crea o aggiorna un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-103">Creates or updates a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dc0a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3dc0a-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dc0a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dc0a-105">DESCRIPTION</span></span>
<span data-ttu-id="3dc0a-106">Il cmdlet **New-AzureRmStreamAnalyticsJob** crea un nuovo processo di analisi del flusso in Azure o aggiorna la definizione di un processo specificato esistente.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-106">The **New-AzureRmStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="3dc0a-107">Il nome del processo può essere specificato in. File JSON o nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="3dc0a-108">Se entrambi sono specificati, la riga di comando nome deve corrispondere al nome nel file.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="3dc0a-109">Se si specifica un nome di processo già esistente e non si specifica il parametro *Force* , il cmdlet chiederà se sostituire o meno il processo esistente.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>

<span data-ttu-id="3dc0a-110">Se specifichi il parametro *Force* e specifichi un nome lavoro esistente, la definizione del processo verrà sostituita senza conferma.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="3dc0a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3dc0a-111">EXAMPLES</span></span>

### <span data-ttu-id="3dc0a-112">ESEMPIO 1: creare un processo</span><span class="sxs-lookup"><span data-stu-id="3dc0a-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="3dc0a-113">Questo comando crea un processo dalla definizione in JobDefinition.jsattivata.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="3dc0a-114">Se un processo esistente con il nome specificato nel file di definizione del processo è già definito, il cmdlet chiederà se sostituirlo o meno.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="3dc0a-115">ESEMPIO 2: sostituire una definizione di processo</span><span class="sxs-lookup"><span data-stu-id="3dc0a-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="3dc0a-116">Questo comando sostituisce la definizione del processo per StreamingJob senza conferma.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="3dc0a-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3dc0a-117">PARAMETERS</span></span>

### <span data-ttu-id="3dc0a-118">-File</span><span class="sxs-lookup"><span data-stu-id="3dc0a-118">-File</span></span>
<span data-ttu-id="3dc0a-119">Specifica il percorso di un file JSON che contiene la rappresentazione JSON del processo di analisi di Azure Stream da creare.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-119">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc0a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3dc0a-120">-Force</span></span>
<span data-ttu-id="3dc0a-121">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3dc0a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3dc0a-122">-Name</span></span>
<span data-ttu-id="3dc0a-123">Specifica il nome del processo di analisi di Azure Stream da creare.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-123">Specifies the name of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dc0a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dc0a-124">-ResourceGroupName</span></span>
<span data-ttu-id="3dc0a-125">Specifica il nome del gruppo di risorse a cui deve appartenere il processo di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-125">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

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

### <span data-ttu-id="3dc0a-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3dc0a-126">-Confirm</span></span>
<span data-ttu-id="3dc0a-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc0a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dc0a-128">-WhatIf</span></span>
<span data-ttu-id="3dc0a-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dc0a-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc0a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dc0a-131">-DefaultProfile</span></span>
<span data-ttu-id="3dc0a-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dc0a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dc0a-133">CommonParameters</span></span>
<span data-ttu-id="3dc0a-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dc0a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dc0a-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dc0a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dc0a-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3dc0a-136">INPUTS</span></span>

## <span data-ttu-id="3dc0a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3dc0a-137">OUTPUTS</span></span>

### <span data-ttu-id="3dc0a-138">Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob</span><span class="sxs-lookup"><span data-stu-id="3dc0a-138">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="3dc0a-139">Note</span><span class="sxs-lookup"><span data-stu-id="3dc0a-139">NOTES</span></span>

## <span data-ttu-id="3dc0a-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3dc0a-140">RELATED LINKS</span></span>

[<span data-ttu-id="3dc0a-141">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3dc0a-141">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="3dc0a-142">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3dc0a-142">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="3dc0a-143">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3dc0a-143">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="3dc0a-144">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3dc0a-144">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="3dc0a-145">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="3dc0a-145">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)



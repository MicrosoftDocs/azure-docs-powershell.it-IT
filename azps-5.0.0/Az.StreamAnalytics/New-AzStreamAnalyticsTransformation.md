---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: 017c084e98d8983343ae1f8c19464cc254b26e2e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199634"
---
# <span data-ttu-id="2e241-101">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="2e241-101">New-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="2e241-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2e241-102">SYNOPSIS</span></span>
<span data-ttu-id="2e241-103">Crea o aggiorna una trasformazione all'interno di un processo.</span><span class="sxs-lookup"><span data-stu-id="2e241-103">Creates or updates a transformation within a job.</span></span>

## <span data-ttu-id="2e241-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e241-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e241-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e241-105">DESCRIPTION</span></span>
<span data-ttu-id="2e241-106">Il cmdlet **New-AzStreamAnalyticsTransformation** crea una trasformazione in un processo di analisi del flusso o aggiorna la trasformazione esistente.</span><span class="sxs-lookup"><span data-stu-id="2e241-106">The **New-AzStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="2e241-107">Il nome della trasformazione può essere specificato in. File JSON o nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="2e241-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="2e241-108">Se entrambi sono specificati, la riga di comando nome deve corrispondere al nome nel file.</span><span class="sxs-lookup"><span data-stu-id="2e241-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="2e241-109">Se si specifica una trasformazione che esiste già e non si specifica il parametro Force, il cmdlet chiederà se sostituire o meno la trasformazione esistente.</span><span class="sxs-lookup"><span data-stu-id="2e241-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>
<span data-ttu-id="2e241-110">Se specifichi il parametro *Force* e specifichi un nome di trasformazione esistente, la trasformazione verrà sostituita senza conferma.</span><span class="sxs-lookup"><span data-stu-id="2e241-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="2e241-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e241-111">EXAMPLES</span></span>

### <span data-ttu-id="2e241-112">Esempio 1: creare o sostituire una trasformazione in un processo</span><span class="sxs-lookup"><span data-stu-id="2e241-112">Example 1: Create or replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="2e241-113">Questo comando crea una trasformazione denominata StreamingJobTransform nel processo denominato StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="2e241-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="2e241-114">Se una trasformazione esistente è già definita con quel nome, il cmdlet chiederà se sostituirla o meno.</span><span class="sxs-lookup"><span data-stu-id="2e241-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="2e241-115">Esempio 2: sostituire una trasformazione in un processo</span><span class="sxs-lookup"><span data-stu-id="2e241-115">Example 2: Replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="2e241-116">Questo comando sostituisce la definizione di StreamingJobTransform nel processo StreamingJob senza conferma.</span><span class="sxs-lookup"><span data-stu-id="2e241-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="2e241-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2e241-117">PARAMETERS</span></span>

### <span data-ttu-id="2e241-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e241-118">-DefaultProfile</span></span>
<span data-ttu-id="2e241-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e241-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e241-120">-File</span><span class="sxs-lookup"><span data-stu-id="2e241-120">-File</span></span>
<span data-ttu-id="2e241-121">Specifica il percorso di un file JSON che contiene la rappresentazione JSON della trasformazione di analisi di Azure Stream da creare.</span><span class="sxs-lookup"><span data-stu-id="2e241-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e241-122">-Force</span><span class="sxs-lookup"><span data-stu-id="2e241-122">-Force</span></span>
<span data-ttu-id="2e241-123">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2e241-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2e241-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="2e241-124">-JobName</span></span>
<span data-ttu-id="2e241-125">Specifica il nome del processo di analisi di Azure Stream in cui creare la trasformazione di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="2e241-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="2e241-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e241-126">-Name</span></span>
<span data-ttu-id="2e241-127">Specifica il nome della trasformazione di analisi di Azure Stream da creare.</span><span class="sxs-lookup"><span data-stu-id="2e241-127">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e241-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e241-128">-ResourceGroupName</span></span>
<span data-ttu-id="2e241-129">Specifica il nome del gruppo di risorse in cui creare la trasformazione analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="2e241-129">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="2e241-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2e241-130">-Confirm</span></span>
<span data-ttu-id="2e241-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e241-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e241-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e241-132">-WhatIf</span></span>
<span data-ttu-id="2e241-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e241-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e241-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e241-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e241-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e241-135">CommonParameters</span></span>
<span data-ttu-id="2e241-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e241-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e241-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e241-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e241-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2e241-138">INPUTS</span></span>

### <span data-ttu-id="2e241-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2e241-139">System.String</span></span>

## <span data-ttu-id="2e241-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e241-140">OUTPUTS</span></span>

### <span data-ttu-id="2e241-141">Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="2e241-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="2e241-142">Note</span><span class="sxs-lookup"><span data-stu-id="2e241-142">NOTES</span></span>

## <span data-ttu-id="2e241-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e241-143">RELATED LINKS</span></span>

[<span data-ttu-id="2e241-144">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="2e241-144">Get-AzStreamAnalyticsTransformation</span></span>](./Get-AzStreamAnalyticsTransformation.md)



---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: eb9f8b82e8ff8a0f60931953f2a3b4349e7b4a4f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512791"
---
# <span data-ttu-id="c586d-101">New-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="c586d-101">New-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="c586d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c586d-102">SYNOPSIS</span></span>
<span data-ttu-id="c586d-103">Crea o aggiorna una trasformazione all'interno di un processo.</span><span class="sxs-lookup"><span data-stu-id="c586d-103">Creates or updates a transformation within a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c586d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c586d-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c586d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c586d-105">DESCRIPTION</span></span>
<span data-ttu-id="c586d-106">Il cmdlet **New-AzureRmStreamAnalyticsTransformation** crea una trasformazione in un processo di analisi del flusso o aggiorna la trasformazione esistente.</span><span class="sxs-lookup"><span data-stu-id="c586d-106">The **New-AzureRmStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="c586d-107">Il nome della trasformazione può essere specificato in. File JSON o nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="c586d-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="c586d-108">Se entrambi sono specificati, la riga di comando nome deve corrispondere al nome nel file.</span><span class="sxs-lookup"><span data-stu-id="c586d-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="c586d-109">Se si specifica una trasformazione che esiste già e non si specifica il parametro Force, il cmdlet chiederà se sostituire o meno la trasformazione esistente.</span><span class="sxs-lookup"><span data-stu-id="c586d-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>

<span data-ttu-id="c586d-110">Se specifichi il parametro *Force* e specifichi un nome di trasformazione esistente, la trasformazione verrà sostituita senza conferma.</span><span class="sxs-lookup"><span data-stu-id="c586d-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="c586d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c586d-111">EXAMPLES</span></span>

### <span data-ttu-id="c586d-112">ESEMPIO 1: creare o sostituire una trasformazione in un processo</span><span class="sxs-lookup"><span data-stu-id="c586d-112">EXAMPLE 1: Create or replace a transformation in a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="c586d-113">Questo comando crea una trasformazione denominata StreamingJobTransform nel processo denominato StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="c586d-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="c586d-114">Se una trasformazione esistente è già definita con quel nome, il cmdlet chiederà se sostituirla o meno.</span><span class="sxs-lookup"><span data-stu-id="c586d-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="c586d-115">ESEMPIO 2: sostituire una trasformazione in un processo</span><span class="sxs-lookup"><span data-stu-id="c586d-115">EXAMPLE 2: Replace a transformation in a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="c586d-116">Questo comando sostituisce la definizione di StreamingJobTransform nel processo StreamingJob senza conferma.</span><span class="sxs-lookup"><span data-stu-id="c586d-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="c586d-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c586d-117">PARAMETERS</span></span>

### <span data-ttu-id="c586d-118">-File</span><span class="sxs-lookup"><span data-stu-id="c586d-118">-File</span></span>
<span data-ttu-id="c586d-119">Specifica il percorso di un file JSON che contiene la rappresentazione JSON della trasformazione di analisi di Azure Stream da creare.</span><span class="sxs-lookup"><span data-stu-id="c586d-119">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="c586d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c586d-120">-Force</span></span>
<span data-ttu-id="c586d-121">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c586d-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c586d-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="c586d-122">-JobName</span></span>
<span data-ttu-id="c586d-123">Specifica il nome del processo di analisi di Azure Stream in cui creare la trasformazione di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="c586d-123">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="c586d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c586d-124">-Name</span></span>
<span data-ttu-id="c586d-125">Specifica il nome della trasformazione di analisi di Azure Stream da creare.</span><span class="sxs-lookup"><span data-stu-id="c586d-125">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="c586d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c586d-126">-ResourceGroupName</span></span>
<span data-ttu-id="c586d-127">Specifica il nome del gruppo di risorse in cui creare la trasformazione analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="c586d-127">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="c586d-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c586d-128">-Confirm</span></span>
<span data-ttu-id="c586d-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c586d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c586d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c586d-130">-WhatIf</span></span>
<span data-ttu-id="c586d-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c586d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c586d-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c586d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c586d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c586d-133">-DefaultProfile</span></span>
<span data-ttu-id="c586d-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c586d-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c586d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c586d-135">CommonParameters</span></span>
<span data-ttu-id="c586d-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c586d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c586d-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c586d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c586d-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c586d-138">INPUTS</span></span>

## <span data-ttu-id="c586d-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c586d-139">OUTPUTS</span></span>

### <span data-ttu-id="c586d-140">Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="c586d-140">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="c586d-141">Note</span><span class="sxs-lookup"><span data-stu-id="c586d-141">NOTES</span></span>

## <span data-ttu-id="c586d-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c586d-142">RELATED LINKS</span></span>

[<span data-ttu-id="c586d-143">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="c586d-143">Get-AzureRmStreamAnalyticsTransformation</span></span>](./Get-AzureRmStreamAnalyticsTransformation.md)



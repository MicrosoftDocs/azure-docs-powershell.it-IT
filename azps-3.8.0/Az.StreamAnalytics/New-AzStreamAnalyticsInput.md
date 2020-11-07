---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
ms.openlocfilehash: 6b9fb63bfeba8d7708389a8730ec4bcdfab55f6d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864573"
---
# <span data-ttu-id="f77af-101">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="f77af-101">New-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="f77af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f77af-102">SYNOPSIS</span></span>
<span data-ttu-id="f77af-103">Crea o aggiorna un input di processo.</span><span class="sxs-lookup"><span data-stu-id="f77af-103">Creates or updates a job input.</span></span>

## <span data-ttu-id="f77af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f77af-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f77af-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f77af-105">DESCRIPTION</span></span>
<span data-ttu-id="f77af-106">Il cmdlet **New-AzStreamAnalyticsInput** crea un input all'interno di un processo di analisi del flusso o aggiorna un input esistente.</span><span class="sxs-lookup"><span data-stu-id="f77af-106">The **New-AzStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="f77af-107">Il nome dell'input può essere specificato nel file JSON o nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="f77af-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="f77af-108">Se entrambi sono specificati, la riga di comando nome deve corrispondere al nome nel file.</span><span class="sxs-lookup"><span data-stu-id="f77af-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="f77af-109">Se specifichi un input già esistente e non specifichi il parametro *Force* , il cmdlet richiederà se sostituire o meno l'input esistente.</span><span class="sxs-lookup"><span data-stu-id="f77af-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>
<span data-ttu-id="f77af-110">Se specifichi il parametro *Force* e specifichi un nome di input esistente, l'input verrà sostituito senza conferma.</span><span class="sxs-lookup"><span data-stu-id="f77af-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="f77af-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f77af-111">EXAMPLES</span></span>

### <span data-ttu-id="f77af-112">ESEMPIO 1: creare un input di processo con una definizione da un file</span><span class="sxs-lookup"><span data-stu-id="f77af-112">EXAMPLE 1: Create a job input with a definition from a file</span></span>
```
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="f77af-113">Questo comando crea un input dal file Input.jsattivato.</span><span class="sxs-lookup"><span data-stu-id="f77af-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="f77af-114">Se è già stato definito un input esistente con il nome specificato nel file di definizione di input, il cmdlet chiederà se sostituirlo o meno.</span><span class="sxs-lookup"><span data-stu-id="f77af-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="f77af-115">ESEMPIO 2: creare un input di processo</span><span class="sxs-lookup"><span data-stu-id="f77af-115">EXAMPLE 2: Create a job input</span></span>
```
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="f77af-116">Questo comando crea un nuovo input nel processo denominato EntryStream.</span><span class="sxs-lookup"><span data-stu-id="f77af-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="f77af-117">Se un input esistente con questo nome è già definito, il cmdlet chiederà se sostituirlo o meno.</span><span class="sxs-lookup"><span data-stu-id="f77af-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="f77af-118">ESEMPIO 3: sostituire un input di processo con una definizione da un file</span><span class="sxs-lookup"><span data-stu-id="f77af-118">EXAMPLE 3: Replace a job input with a definition from a file</span></span>
```
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="f77af-119">Questo comando sostituisce la definizione dell'origine di input esistente denominata EntryStream con la definizione da file senza conferma.</span><span class="sxs-lookup"><span data-stu-id="f77af-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="f77af-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f77af-120">PARAMETERS</span></span>

### <span data-ttu-id="f77af-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f77af-121">-DefaultProfile</span></span>
<span data-ttu-id="f77af-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f77af-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f77af-123">-File</span><span class="sxs-lookup"><span data-stu-id="f77af-123">-File</span></span>
<span data-ttu-id="f77af-124">Specifica il percorso di un file JSON che contiene la rappresentazione JSON dell'input di analisi di Azure Stream da creare.</span><span class="sxs-lookup"><span data-stu-id="f77af-124">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="f77af-125">-Force</span><span class="sxs-lookup"><span data-stu-id="f77af-125">-Force</span></span>
<span data-ttu-id="f77af-126">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f77af-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f77af-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="f77af-127">-JobName</span></span>
<span data-ttu-id="f77af-128">Specifica il nome del processo di analisi di Azure Stream in cui creare l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="f77af-128">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

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

### <span data-ttu-id="f77af-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="f77af-129">-Name</span></span>
<span data-ttu-id="f77af-130">Specifica il nome dell'input di analisi di Azure Stream da creare.</span><span class="sxs-lookup"><span data-stu-id="f77af-130">Specifies the name of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="f77af-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f77af-131">-ResourceGroupName</span></span>
<span data-ttu-id="f77af-132">Specifica il nome del gruppo di risorse in cui creare l'input di Azure streaming.</span><span class="sxs-lookup"><span data-stu-id="f77af-132">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

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

### <span data-ttu-id="f77af-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f77af-133">-Confirm</span></span>
<span data-ttu-id="f77af-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f77af-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f77af-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f77af-135">-WhatIf</span></span>
<span data-ttu-id="f77af-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f77af-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f77af-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f77af-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f77af-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f77af-138">CommonParameters</span></span>
<span data-ttu-id="f77af-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f77af-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f77af-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f77af-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f77af-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f77af-141">INPUTS</span></span>

### <span data-ttu-id="f77af-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f77af-142">System.String</span></span>

## <span data-ttu-id="f77af-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f77af-143">OUTPUTS</span></span>

### <span data-ttu-id="f77af-144">Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="f77af-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="f77af-145">Note</span><span class="sxs-lookup"><span data-stu-id="f77af-145">NOTES</span></span>

## <span data-ttu-id="f77af-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f77af-146">RELATED LINKS</span></span>

[<span data-ttu-id="f77af-147">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="f77af-147">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="f77af-148">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="f77af-148">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="f77af-149">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="f77af-149">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)



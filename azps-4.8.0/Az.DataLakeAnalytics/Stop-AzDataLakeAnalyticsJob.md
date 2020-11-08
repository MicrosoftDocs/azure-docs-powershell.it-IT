---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/stop-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Stop-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 6825dc4a66e160590f420bf1c21b0dab0cd29d55
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189103"
---
# <span data-ttu-id="b0900-101">Stop-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b0900-101">Stop-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="b0900-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0900-102">SYNOPSIS</span></span>
<span data-ttu-id="b0900-103">Annulla un processo.</span><span class="sxs-lookup"><span data-stu-id="b0900-103">Cancels a job.</span></span>

## <span data-ttu-id="b0900-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0900-104">SYNTAX</span></span>

```
Stop-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0900-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0900-105">DESCRIPTION</span></span>
<span data-ttu-id="b0900-106">Il cmdlet **Stop-AzDataLakeAnalyticsJob** Annulla un processo di analisi del Lago di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="b0900-106">The **Stop-AzDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="b0900-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0900-107">EXAMPLES</span></span>

### <span data-ttu-id="b0900-108">Esempio 1: annullamento di un processo</span><span class="sxs-lookup"><span data-stu-id="b0900-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="b0900-109">Questo comando Annulla il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="b0900-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="b0900-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0900-110">PARAMETERS</span></span>

### <span data-ttu-id="b0900-111">-Account</span><span class="sxs-lookup"><span data-stu-id="b0900-111">-Account</span></span>
<span data-ttu-id="b0900-112">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="b0900-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0900-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0900-113">-DefaultProfile</span></span>
<span data-ttu-id="b0900-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b0900-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0900-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b0900-115">-Force</span></span>
<span data-ttu-id="b0900-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b0900-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0900-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="b0900-117">-JobId</span></span>
<span data-ttu-id="b0900-118">Specifica l'ID del processo da annullare.</span><span class="sxs-lookup"><span data-stu-id="b0900-118">Specifies the ID of the job to cancel.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0900-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0900-119">-PassThru</span></span>
<span data-ttu-id="b0900-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="b0900-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b0900-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b0900-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0900-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b0900-122">-Confirm</span></span>
<span data-ttu-id="b0900-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0900-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0900-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0900-124">-WhatIf</span></span>
<span data-ttu-id="b0900-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0900-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0900-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0900-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0900-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0900-127">CommonParameters</span></span>
<span data-ttu-id="b0900-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0900-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0900-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0900-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0900-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0900-130">INPUTS</span></span>

### <span data-ttu-id="b0900-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b0900-131">System.String</span></span>

### <span data-ttu-id="b0900-132">System. Guid</span><span class="sxs-lookup"><span data-stu-id="b0900-132">System.Guid</span></span>

### <span data-ttu-id="b0900-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b0900-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b0900-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0900-134">OUTPUTS</span></span>

### <span data-ttu-id="b0900-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b0900-135">System.Boolean</span></span>

## <span data-ttu-id="b0900-136">Note</span><span class="sxs-lookup"><span data-stu-id="b0900-136">NOTES</span></span>

## <span data-ttu-id="b0900-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0900-137">RELATED LINKS</span></span>

[<span data-ttu-id="b0900-138">Get-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b0900-138">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="b0900-139">Invia-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b0900-139">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="b0900-140">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b0900-140">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


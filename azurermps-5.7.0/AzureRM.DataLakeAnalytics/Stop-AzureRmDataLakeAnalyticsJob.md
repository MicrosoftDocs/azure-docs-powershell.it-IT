---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/stop-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 956e263f402a3b6cb78631f8337d46fc1effdd98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514379"
---
# <span data-ttu-id="087b4-101">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="087b4-101">Stop-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="087b4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="087b4-102">SYNOPSIS</span></span>
<span data-ttu-id="087b4-103">Annulla un processo.</span><span class="sxs-lookup"><span data-stu-id="087b4-103">Cancels a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="087b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="087b4-104">SYNTAX</span></span>

```
Stop-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="087b4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="087b4-105">DESCRIPTION</span></span>
<span data-ttu-id="087b4-106">Il cmdlet **Stop-AzureRmDataLakeAnalyticsJob** Annulla un processo di analisi del Lago di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="087b4-106">The **Stop-AzureRmDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="087b4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="087b4-107">EXAMPLES</span></span>

### <span data-ttu-id="087b4-108">Esempio 1: annullamento di un processo</span><span class="sxs-lookup"><span data-stu-id="087b4-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="087b4-109">Questo comando Annulla il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="087b4-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="087b4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="087b4-110">PARAMETERS</span></span>

### <span data-ttu-id="087b4-111">-Account</span><span class="sxs-lookup"><span data-stu-id="087b4-111">-Account</span></span>
<span data-ttu-id="087b4-112">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="087b4-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="087b4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="087b4-113">-DefaultProfile</span></span>
<span data-ttu-id="087b4-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="087b4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="087b4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="087b4-115">-Force</span></span>
<span data-ttu-id="087b4-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="087b4-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="087b4-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="087b4-117">-JobId</span></span>
<span data-ttu-id="087b4-118">Specifica l'ID del processo da annullare.</span><span class="sxs-lookup"><span data-stu-id="087b4-118">Specifies the ID of the job to cancel.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="087b4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="087b4-119">-PassThru</span></span>
<span data-ttu-id="087b4-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="087b4-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="087b4-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="087b4-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="087b4-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="087b4-122">-Confirm</span></span>
<span data-ttu-id="087b4-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="087b4-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="087b4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="087b4-124">-WhatIf</span></span>
<span data-ttu-id="087b4-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="087b4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="087b4-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="087b4-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="087b4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="087b4-127">CommonParameters</span></span>
<span data-ttu-id="087b4-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="087b4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="087b4-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="087b4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="087b4-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="087b4-130">INPUTS</span></span>

### <span data-ttu-id="087b4-131">GUID</span><span class="sxs-lookup"><span data-stu-id="087b4-131">Guid</span></span>
<span data-ttu-id="087b4-132">Il parametro "JobId" accetta il valore di tipo "GUID" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="087b4-132">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="087b4-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="087b4-133">OUTPUTS</span></span>

### <span data-ttu-id="087b4-134">bool</span><span class="sxs-lookup"><span data-stu-id="087b4-134">bool</span></span>
<span data-ttu-id="087b4-135">Se PassThru è specificato, restituisce vero al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="087b4-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="087b4-136">Note</span><span class="sxs-lookup"><span data-stu-id="087b4-136">NOTES</span></span>

## <span data-ttu-id="087b4-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="087b4-137">RELATED LINKS</span></span>

[<span data-ttu-id="087b4-138">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="087b4-138">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="087b4-139">Invia-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="087b4-139">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="087b4-140">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="087b4-140">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)



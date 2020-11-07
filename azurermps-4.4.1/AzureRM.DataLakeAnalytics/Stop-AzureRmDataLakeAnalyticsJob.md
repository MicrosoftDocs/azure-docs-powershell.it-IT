---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: a0848ffc888b4812a28198749417d0b0894a5d98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688027"
---
# <span data-ttu-id="381b0-101">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="381b0-101">Stop-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="381b0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="381b0-102">SYNOPSIS</span></span>
<span data-ttu-id="381b0-103">Annulla un processo.</span><span class="sxs-lookup"><span data-stu-id="381b0-103">Cancels a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="381b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="381b0-104">SYNTAX</span></span>

```
Stop-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="381b0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="381b0-105">DESCRIPTION</span></span>
<span data-ttu-id="381b0-106">Il cmdlet **Stop-AzureRmDataLakeAnalyticsJob** Annulla un processo di analisi del Lago di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="381b0-106">The **Stop-AzureRmDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="381b0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="381b0-107">EXAMPLES</span></span>

### <span data-ttu-id="381b0-108">Esempio 1: annullamento di un processo</span><span class="sxs-lookup"><span data-stu-id="381b0-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="381b0-109">Questo comando Annulla il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="381b0-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="381b0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="381b0-110">PARAMETERS</span></span>

### <span data-ttu-id="381b0-111">-Account</span><span class="sxs-lookup"><span data-stu-id="381b0-111">-Account</span></span>
<span data-ttu-id="381b0-112">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="381b0-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="381b0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="381b0-113">-Force</span></span>
<span data-ttu-id="381b0-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="381b0-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="381b0-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="381b0-115">-JobId</span></span>
<span data-ttu-id="381b0-116">Specifica l'ID del processo da annullare.</span><span class="sxs-lookup"><span data-stu-id="381b0-116">Specifies the ID of the job to cancel.</span></span>

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

### <span data-ttu-id="381b0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="381b0-117">-PassThru</span></span>
<span data-ttu-id="381b0-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="381b0-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="381b0-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="381b0-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="381b0-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="381b0-120">-Confirm</span></span>
<span data-ttu-id="381b0-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="381b0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="381b0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="381b0-122">-WhatIf</span></span>
<span data-ttu-id="381b0-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="381b0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="381b0-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="381b0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="381b0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="381b0-125">-DefaultProfile</span></span>
<span data-ttu-id="381b0-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="381b0-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="381b0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="381b0-127">CommonParameters</span></span>
<span data-ttu-id="381b0-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="381b0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="381b0-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="381b0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="381b0-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="381b0-130">INPUTS</span></span>

### <span data-ttu-id="381b0-131">GUID</span><span class="sxs-lookup"><span data-stu-id="381b0-131">Guid</span></span>
<span data-ttu-id="381b0-132">Il parametro "JobId" accetta il valore di tipo "GUID" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="381b0-132">Parameter 'JobId' accepts value of type 'Guid' from the pipeline</span></span>

## <span data-ttu-id="381b0-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="381b0-133">OUTPUTS</span></span>

### <span data-ttu-id="381b0-134">bool</span><span class="sxs-lookup"><span data-stu-id="381b0-134">bool</span></span>
<span data-ttu-id="381b0-135">Se PassThru è specificato, restituisce vero al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="381b0-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="381b0-136">Note</span><span class="sxs-lookup"><span data-stu-id="381b0-136">NOTES</span></span>

## <span data-ttu-id="381b0-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="381b0-137">RELATED LINKS</span></span>

[<span data-ttu-id="381b0-138">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="381b0-138">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="381b0-139">Invia-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="381b0-139">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="381b0-140">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="381b0-140">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)



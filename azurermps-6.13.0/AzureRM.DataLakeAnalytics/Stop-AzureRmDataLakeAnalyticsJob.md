---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 5EB9E134-C789-47A5-9AF8-CD4A475559C2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/stop-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Stop-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 4fc5c20cf43fbafb89007328307c69d4820b2127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686424"
---
# <span data-ttu-id="98567-101">Stop-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="98567-101">Stop-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="98567-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="98567-102">SYNOPSIS</span></span>
<span data-ttu-id="98567-103">Annulla un processo.</span><span class="sxs-lookup"><span data-stu-id="98567-103">Cancels a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98567-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98567-104">SYNTAX</span></span>

```
Stop-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98567-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98567-105">DESCRIPTION</span></span>
<span data-ttu-id="98567-106">Il cmdlet **Stop-AzureRmDataLakeAnalyticsJob** Annulla un processo di analisi del Lago di dati di Azure.</span><span class="sxs-lookup"><span data-stu-id="98567-106">The **Stop-AzureRmDataLakeAnalyticsJob** cmdlet cancels an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="98567-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98567-107">EXAMPLES</span></span>

### <span data-ttu-id="98567-108">Esempio 1: annullamento di un processo</span><span class="sxs-lookup"><span data-stu-id="98567-108">Example 1: Cancel a job</span></span>
```
PS C:\>Stop-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccout" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="98567-109">Questo comando Annulla il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="98567-109">This command cancels the job with the specified ID.</span></span>

## <span data-ttu-id="98567-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="98567-110">PARAMETERS</span></span>

### <span data-ttu-id="98567-111">-Account</span><span class="sxs-lookup"><span data-stu-id="98567-111">-Account</span></span>
<span data-ttu-id="98567-112">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="98567-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="98567-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98567-113">-DefaultProfile</span></span>
<span data-ttu-id="98567-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="98567-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98567-115">-Force</span><span class="sxs-lookup"><span data-stu-id="98567-115">-Force</span></span>
<span data-ttu-id="98567-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="98567-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="98567-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="98567-117">-JobId</span></span>
<span data-ttu-id="98567-118">Specifica l'ID del processo da annullare.</span><span class="sxs-lookup"><span data-stu-id="98567-118">Specifies the ID of the job to cancel.</span></span>

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

### <span data-ttu-id="98567-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98567-119">-PassThru</span></span>
<span data-ttu-id="98567-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="98567-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="98567-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="98567-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="98567-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="98567-122">-Confirm</span></span>
<span data-ttu-id="98567-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98567-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98567-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98567-124">-WhatIf</span></span>
<span data-ttu-id="98567-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98567-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98567-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98567-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98567-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98567-127">CommonParameters</span></span>
<span data-ttu-id="98567-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98567-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98567-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98567-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98567-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="98567-130">INPUTS</span></span>

### <span data-ttu-id="98567-131">System. String</span><span class="sxs-lookup"><span data-stu-id="98567-131">System.String</span></span>

### <span data-ttu-id="98567-132">System. Guid</span><span class="sxs-lookup"><span data-stu-id="98567-132">System.Guid</span></span>

### <span data-ttu-id="98567-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="98567-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="98567-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98567-134">OUTPUTS</span></span>

### <span data-ttu-id="98567-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="98567-135">System.Boolean</span></span>

## <span data-ttu-id="98567-136">Note</span><span class="sxs-lookup"><span data-stu-id="98567-136">NOTES</span></span>

## <span data-ttu-id="98567-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98567-137">RELATED LINKS</span></span>

[<span data-ttu-id="98567-138">Get-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="98567-138">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="98567-139">Invia-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="98567-139">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="98567-140">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="98567-140">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)



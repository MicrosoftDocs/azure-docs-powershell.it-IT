---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
ms.openlocfilehash: 18551d6d839991cf0eb9e020c62fa0a24207d1e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516920"
---
# <span data-ttu-id="1f12f-101">Get-AzureRmAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="1f12f-101">Get-AzureRmAutomationJobOutputRecord</span></span>

## <span data-ttu-id="1f12f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f12f-102">SYNOPSIS</span></span>
<span data-ttu-id="1f12f-103">Ottiene l'output completo di un record di output processo di automazione.</span><span class="sxs-lookup"><span data-stu-id="1f12f-103">Gets the full output of an Automation job output record.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f12f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f12f-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f12f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f12f-105">DESCRIPTION</span></span>
<span data-ttu-id="1f12f-106">Il cmdlet **Get-AzureRmAutomationJobOutputRecord** Ottiene l'output completo di un record di output processo di automazione.</span><span class="sxs-lookup"><span data-stu-id="1f12f-106">The **Get-AzureRmAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>

<span data-ttu-id="1f12f-107">Anche se il cmdlet **Get-AzureRmAutomationJobOutput** elenca uno o più record di output del processo, restituisce solo un riepilogo, come stringa, del valore di qualsiasi record di output.</span><span class="sxs-lookup"><span data-stu-id="1f12f-107">Although the **Get-AzureRmAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="1f12f-108">Non restituisce il valore completo del valore di output del record in uscita nel tipo originale.</span><span class="sxs-lookup"><span data-stu-id="1f12f-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="1f12f-109">Inoltre, il riepilogo ha una lunghezza massima, che può superare il valore completo restituito da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f12f-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>
<span data-ttu-id="1f12f-110">A differenza di **Get-AzureRmAutomationJobOutput** , questo cmdlet restituisce il valore completo nel relativo tipo originalmente outputd, per il valore in uscita del record.</span><span class="sxs-lookup"><span data-stu-id="1f12f-110">Unlike **Get-AzureRmAutomationJobOutput** , this cmdlet returns the full value in its originally outputted type, for any output record's outputted value.</span></span>

## <span data-ttu-id="1f12f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f12f-111">EXAMPLES</span></span>

### <span data-ttu-id="1f12f-112">Esempio 1: ottenere l'output completo di un processo di automazione</span><span class="sxs-lookup"><span data-stu-id="1f12f-112">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzureRmAutomationJobOutputRecord
```

<span data-ttu-id="1f12f-113">Questo comando ottiene l'output completo del processo con l'ID processo specificato.</span><span class="sxs-lookup"><span data-stu-id="1f12f-113">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="1f12f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f12f-114">PARAMETERS</span></span>

### <span data-ttu-id="1f12f-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1f12f-115">-AutomationAccountName</span></span>
<span data-ttu-id="1f12f-116">Specifica il nome di un account di automazione per il quale questo cmdlet ottiene un record di output del processo.</span><span class="sxs-lookup"><span data-stu-id="1f12f-116">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f12f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f12f-117">-DefaultProfile</span></span>
<span data-ttu-id="1f12f-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1f12f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f12f-119">-ID</span><span class="sxs-lookup"><span data-stu-id="1f12f-119">-Id</span></span>
<span data-ttu-id="1f12f-120">Specifica l'ID di un record di output processo per il cmdlet da recuperare.</span><span class="sxs-lookup"><span data-stu-id="1f12f-120">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StreamRecordId

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f12f-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="1f12f-121">-JobId</span></span>
<span data-ttu-id="1f12f-122">Specifica l'ID di un processo per il quale questo cmdlet ottiene un record di output.</span><span class="sxs-lookup"><span data-stu-id="1f12f-122">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f12f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f12f-123">-ResourceGroupName</span></span>
<span data-ttu-id="1f12f-124">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene un record di output del processo.</span><span class="sxs-lookup"><span data-stu-id="1f12f-124">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f12f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f12f-125">CommonParameters</span></span>
<span data-ttu-id="1f12f-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f12f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f12f-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f12f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f12f-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f12f-128">INPUTS</span></span>

### <span data-ttu-id="1f12f-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1f12f-129">None</span></span>
<span data-ttu-id="1f12f-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="1f12f-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f12f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f12f-131">OUTPUTS</span></span>

### <span data-ttu-id="1f12f-132">Microsoft. Azure. Commands. Automation. Model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="1f12f-132">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="1f12f-133">Note</span><span class="sxs-lookup"><span data-stu-id="1f12f-133">NOTES</span></span>

## <span data-ttu-id="1f12f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f12f-134">RELATED LINKS</span></span>

[<span data-ttu-id="1f12f-135">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="1f12f-135">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)



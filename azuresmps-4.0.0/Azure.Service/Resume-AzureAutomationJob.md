---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 5E5B8102-9E7E-4128-8160-3AA3803B118F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ff0831e6458a9d587b508acfa2e09948d81d87e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023420"
---
# <span data-ttu-id="c2cdf-101">Resume-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c2cdf-101">Resume-AzureAutomationJob</span></span>

## <span data-ttu-id="c2cdf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2cdf-102">SYNOPSIS</span></span>

<span data-ttu-id="c2cdf-103">Riprende un processo di automazione sospesa.</span><span class="sxs-lookup"><span data-stu-id="c2cdf-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="c2cdf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2cdf-104">SYNTAX</span></span>

```
Resume-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2cdf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2cdf-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="c2cdf-106">Il cmdlet **Resume-AzureAutomationJob** riprende un processo di automazione di Microsoft Azure sospeso.</span><span class="sxs-lookup"><span data-stu-id="c2cdf-106">The **Resume-AzureAutomationJob** cmdlet resumes a suspended Microsoft Azure Automation job.</span></span>
<span data-ttu-id="c2cdf-107">Usa il parametro *ID* per specificare il processo sospeso.</span><span class="sxs-lookup"><span data-stu-id="c2cdf-107">Use the *Id* parameter to specify the suspended job.</span></span>

<span data-ttu-id="c2cdf-108">Per sospendere un processo, usare il cmdlet Suspend-AzureAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="c2cdf-108">To suspend a job, use the Suspend-AzureAutomationJob cmdlet.</span></span>

## <span data-ttu-id="c2cdf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2cdf-109">EXAMPLES</span></span>

### <span data-ttu-id="c2cdf-110">Esempio 1: riprendere un processo sospeso</span><span class="sxs-lookup"><span data-stu-id="c2cdf-110">Example 1: Resume a suspended job</span></span>
```
PS C:\> Resume-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="c2cdf-111">Questo comando riprende il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="c2cdf-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="c2cdf-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2cdf-112">PARAMETERS</span></span>

### <span data-ttu-id="c2cdf-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c2cdf-113">-AutomationAccountName</span></span>
<span data-ttu-id="c2cdf-114">Specifica il nome di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="c2cdf-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="c2cdf-115">-ID</span><span class="sxs-lookup"><span data-stu-id="c2cdf-115">-Id</span></span>
<span data-ttu-id="c2cdf-116">Specifica l'ID di un processo.</span><span class="sxs-lookup"><span data-stu-id="c2cdf-116">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2cdf-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="c2cdf-117">-Profile</span></span>
<span data-ttu-id="c2cdf-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2cdf-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c2cdf-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c2cdf-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c2cdf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2cdf-120">CommonParameters</span></span>
<span data-ttu-id="c2cdf-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2cdf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2cdf-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2cdf-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2cdf-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2cdf-123">INPUTS</span></span>

## <span data-ttu-id="c2cdf-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2cdf-124">OUTPUTS</span></span>

## <span data-ttu-id="c2cdf-125">Note</span><span class="sxs-lookup"><span data-stu-id="c2cdf-125">NOTES</span></span>

## <span data-ttu-id="c2cdf-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2cdf-126">RELATED LINKS</span></span>

[<span data-ttu-id="c2cdf-127">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c2cdf-127">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="c2cdf-128">Stop-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c2cdf-128">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="c2cdf-129">Suspend-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c2cdf-129">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)



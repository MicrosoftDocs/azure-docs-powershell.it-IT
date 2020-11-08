---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: CE04DEE6-28AE-43A3-A8DE-98AC0A57E575
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1c2d9a3aa53cb8efd2924f24aa80db2c7fd07fea
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023717"
---
# <span data-ttu-id="83b89-101">Suspend-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="83b89-101">Suspend-AzureAutomationJob</span></span>

## <span data-ttu-id="83b89-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83b89-102">SYNOPSIS</span></span>

<span data-ttu-id="83b89-103">Sospende un processo di automazione.</span><span class="sxs-lookup"><span data-stu-id="83b89-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="83b89-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83b89-104">SYNTAX</span></span>

```
Suspend-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="83b89-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83b89-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="83b89-106">Il cmdlet **Suspend-AzureAutomationJob** sospende un processo di automazione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="83b89-106">The **Suspend-AzureAutomationJob** cmdlet suspends a Microsoft Azure Automation job.</span></span>
<span data-ttu-id="83b89-107">Specificare un processo di automazione in corso.</span><span class="sxs-lookup"><span data-stu-id="83b89-107">Specify a running Automation job.</span></span>

<span data-ttu-id="83b89-108">Per riprendere un processo sospeso, usare il cmdlet **Resume-AzureAutomationJob** .</span><span class="sxs-lookup"><span data-stu-id="83b89-108">To resume a suspended job, use the **Resume-AzureAutomationJob** cmdlet.</span></span>

## <span data-ttu-id="83b89-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83b89-109">EXAMPLES</span></span>

### <span data-ttu-id="83b89-110">Esempio 1: sospendere un processo</span><span class="sxs-lookup"><span data-stu-id="83b89-110">Example 1: Suspend a job</span></span>
```
PS C:\> Suspend-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="83b89-111">Questo comando sospende il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="83b89-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="83b89-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83b89-112">PARAMETERS</span></span>

### <span data-ttu-id="83b89-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="83b89-113">-AutomationAccountName</span></span>
<span data-ttu-id="83b89-114">Specifica il nome di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="83b89-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="83b89-115">-ID</span><span class="sxs-lookup"><span data-stu-id="83b89-115">-Id</span></span>
<span data-ttu-id="83b89-116">Specifica l'ID di un processo.</span><span class="sxs-lookup"><span data-stu-id="83b89-116">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="83b89-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="83b89-117">-Profile</span></span>
<span data-ttu-id="83b89-118">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83b89-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="83b89-119">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="83b89-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="83b89-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b89-120">CommonParameters</span></span>
<span data-ttu-id="83b89-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83b89-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b89-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83b89-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b89-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83b89-123">INPUTS</span></span>

## <span data-ttu-id="83b89-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83b89-124">OUTPUTS</span></span>

## <span data-ttu-id="83b89-125">Note</span><span class="sxs-lookup"><span data-stu-id="83b89-125">NOTES</span></span>

## <span data-ttu-id="83b89-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83b89-126">RELATED LINKS</span></span>

[<span data-ttu-id="83b89-127">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="83b89-127">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="83b89-128">Curriculum vitae-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="83b89-128">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="83b89-129">Stop-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="83b89-129">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)



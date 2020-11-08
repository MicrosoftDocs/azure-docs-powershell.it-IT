---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2E363D6B-7A05-4C54-B005-68FDBA49A105
online version: ''
schema: 2.0.0
ms.openlocfilehash: cda64b916635d3b46ffb7e8b4170330810a95b5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023900"
---
# <span data-ttu-id="5c13f-101">Stop-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5c13f-101">Stop-AzureAutomationJob</span></span>

## <span data-ttu-id="5c13f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5c13f-102">SYNOPSIS</span></span>

<span data-ttu-id="5c13f-103">Interrompe un processo di automazione.</span><span class="sxs-lookup"><span data-stu-id="5c13f-103">Stops an Automation job.</span></span>

## <span data-ttu-id="5c13f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c13f-104">SYNTAX</span></span>

```
Stop-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c13f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c13f-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="5c13f-106">Il cmdlet **Stop-AzureAutomationJob** interrompe un processo di automazione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5c13f-106">The **Stop-AzureAutomationJob** cmdlet stops a Microsoft Azure Automation job.</span></span>
<span data-ttu-id="5c13f-107">Specificare un processo di automazione in corso.</span><span class="sxs-lookup"><span data-stu-id="5c13f-107">Specify a running automation job.</span></span>

## <span data-ttu-id="5c13f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c13f-108">EXAMPLES</span></span>

### <span data-ttu-id="5c13f-109">Esempio 1: arrestare un processo</span><span class="sxs-lookup"><span data-stu-id="5c13f-109">Example 1: Stop a job</span></span>
```
PS C:\> Stop-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="5c13f-110">Questo comando Arresta il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="5c13f-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="5c13f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5c13f-111">PARAMETERS</span></span>

### <span data-ttu-id="5c13f-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5c13f-112">-AutomationAccountName</span></span>
<span data-ttu-id="5c13f-113">Specifica il nome di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="5c13f-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="5c13f-114">-ID</span><span class="sxs-lookup"><span data-stu-id="5c13f-114">-Id</span></span>
<span data-ttu-id="5c13f-115">Specifica l'ID di un processo.</span><span class="sxs-lookup"><span data-stu-id="5c13f-115">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="5c13f-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="5c13f-116">-Profile</span></span>
<span data-ttu-id="5c13f-117">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c13f-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5c13f-118">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="5c13f-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5c13f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c13f-119">CommonParameters</span></span>
<span data-ttu-id="5c13f-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c13f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c13f-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c13f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c13f-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5c13f-122">INPUTS</span></span>

## <span data-ttu-id="5c13f-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c13f-123">OUTPUTS</span></span>

## <span data-ttu-id="5c13f-124">Note</span><span class="sxs-lookup"><span data-stu-id="5c13f-124">NOTES</span></span>

## <span data-ttu-id="5c13f-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c13f-125">RELATED LINKS</span></span>

[<span data-ttu-id="5c13f-126">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5c13f-126">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="5c13f-127">Curriculum vitae-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5c13f-127">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="5c13f-128">Suspend-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="5c13f-128">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)



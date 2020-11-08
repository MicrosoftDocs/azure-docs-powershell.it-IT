---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 410A58A3-CB0E-43FE-B490-B1520BD1CCEC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c445e2b42738f288de960f30f4c98d909c71784
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023569"
---
# <span data-ttu-id="34d01-101">Get-AzureSchedulerLocation</span><span class="sxs-lookup"><span data-stu-id="34d01-101">Get-AzureSchedulerLocation</span></span>

## <span data-ttu-id="34d01-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34d01-102">SYNOPSIS</span></span>
<span data-ttu-id="34d01-103">Ottiene le posizioni dell'utilità di pianificazione disponibili.</span><span class="sxs-lookup"><span data-stu-id="34d01-103">Gets available scheduler locations.</span></span>

## <span data-ttu-id="34d01-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34d01-104">SYNTAX</span></span>

```
Get-AzureSchedulerLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="34d01-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34d01-105">DESCRIPTION</span></span>
<span data-ttu-id="34d01-106">Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="34d01-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="34d01-107">Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="34d01-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="34d01-108">Il cmdlet **Get-AzureSchedulerLocation** ottiene le posizioni di pianificazione disponibili.</span><span class="sxs-lookup"><span data-stu-id="34d01-108">The **Get-AzureSchedulerLocation** cmdlet gets available scheduler locations.</span></span>

## <span data-ttu-id="34d01-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34d01-109">EXAMPLES</span></span>

### <span data-ttu-id="34d01-110">Esempio 1: ottenere le posizioni degli utilità di pianificazione disponibili</span><span class="sxs-lookup"><span data-stu-id="34d01-110">Example 1: Get available scheduler locations</span></span>
```
PS C:\> Get-AzureSchedulerLocation
```

<span data-ttu-id="34d01-111">Questo comando consente di ottenere le posizioni di Scheduler disponibili.</span><span class="sxs-lookup"><span data-stu-id="34d01-111">This command gets available scheduler locations.</span></span>

## <span data-ttu-id="34d01-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34d01-112">PARAMETERS</span></span>

### <span data-ttu-id="34d01-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="34d01-113">-Profile</span></span>
<span data-ttu-id="34d01-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34d01-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="34d01-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="34d01-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="34d01-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34d01-116">CommonParameters</span></span>
<span data-ttu-id="34d01-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34d01-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34d01-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34d01-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34d01-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34d01-119">INPUTS</span></span>

## <span data-ttu-id="34d01-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34d01-120">OUTPUTS</span></span>

## <span data-ttu-id="34d01-121">Note</span><span class="sxs-lookup"><span data-stu-id="34d01-121">NOTES</span></span>

## <span data-ttu-id="34d01-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34d01-122">RELATED LINKS</span></span>

[<span data-ttu-id="34d01-123">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="34d01-123">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)

[<span data-ttu-id="34d01-124">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="34d01-124">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="34d01-125">Get-AzureSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="34d01-125">Get-AzureSchedulerJobHistory</span></span>](./Get-AzureSchedulerJobHistory.md)



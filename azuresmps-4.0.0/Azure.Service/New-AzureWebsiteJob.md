---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1254A28B-F670-44B2-BB0E-BD41B9483E3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1910a0da546bdc4d5b167d82685608669b7565c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029645"
---
# <span data-ttu-id="be5c8-101">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="be5c8-101">New-AzureWebsiteJob</span></span>

## <span data-ttu-id="be5c8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="be5c8-102">SYNOPSIS</span></span>
<span data-ttu-id="be5c8-103">Crea un processo Web per un sito Web.</span><span class="sxs-lookup"><span data-stu-id="be5c8-103">Creates a web job for a website.</span></span>

## <span data-ttu-id="be5c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be5c8-104">SYNTAX</span></span>

```
New-AzureWebsiteJob -JobName <String> -JobType <WebJobType> -JobFile <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="be5c8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be5c8-105">DESCRIPTION</span></span>
<span data-ttu-id="be5c8-106">Il cmdlet **New-AzureWebsiteJob** crea un processo Web per un sito Web.</span><span class="sxs-lookup"><span data-stu-id="be5c8-106">The **New-AzureWebsiteJob** cmdlet creates a web job for a website.</span></span>

## <span data-ttu-id="be5c8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be5c8-107">EXAMPLES</span></span>

### <span data-ttu-id="be5c8-108">Esempio 1: creare un nuovo processo Web per un sito Web</span><span class="sxs-lookup"><span data-stu-id="be5c8-108">Example 1: Create new web job for a website</span></span>
```
PS C:\> New-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous -JobFile job.bat
```

<span data-ttu-id="be5c8-109">Crea un processo continuo per chiamare job.bat nel sito Web di website.</span><span class="sxs-lookup"><span data-stu-id="be5c8-109">Creates a continuous job to call job.bat on website MyWebsite.</span></span>

## <span data-ttu-id="be5c8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="be5c8-110">PARAMETERS</span></span>

### <span data-ttu-id="be5c8-111">-JobFile</span><span class="sxs-lookup"><span data-stu-id="be5c8-111">-JobFile</span></span>
<span data-ttu-id="be5c8-112">Il file del processo Web.</span><span class="sxs-lookup"><span data-stu-id="be5c8-112">The web job file.</span></span>

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

### <span data-ttu-id="be5c8-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="be5c8-113">-JobName</span></span>
<span data-ttu-id="be5c8-114">Il nome del processo Web.</span><span class="sxs-lookup"><span data-stu-id="be5c8-114">The web job name.</span></span>

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

### <span data-ttu-id="be5c8-115">-JobType</span><span class="sxs-lookup"><span data-stu-id="be5c8-115">-JobType</span></span>
<span data-ttu-id="be5c8-116">Tipo di processo Web.</span><span class="sxs-lookup"><span data-stu-id="be5c8-116">The web job type.</span></span>
<span data-ttu-id="be5c8-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="be5c8-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="be5c8-118">Attivata</span><span class="sxs-lookup"><span data-stu-id="be5c8-118">Triggered</span></span> 
- <span data-ttu-id="be5c8-119">Continua</span><span class="sxs-lookup"><span data-stu-id="be5c8-119">Continuous</span></span>

```yaml
Type: WebJobType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5c8-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="be5c8-120">-Name</span></span>
<span data-ttu-id="be5c8-121">Il nome del sito Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="be5c8-121">The name of the Azure website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5c8-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="be5c8-122">-Profile</span></span>
<span data-ttu-id="be5c8-123">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be5c8-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="be5c8-124">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="be5c8-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="be5c8-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="be5c8-125">-Slot</span></span>
<span data-ttu-id="be5c8-126">Nome dello slot del sito Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="be5c8-126">The slot name of the Azure website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be5c8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be5c8-127">CommonParameters</span></span>
<span data-ttu-id="be5c8-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be5c8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be5c8-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be5c8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be5c8-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="be5c8-130">INPUTS</span></span>

## <span data-ttu-id="be5c8-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be5c8-131">OUTPUTS</span></span>

## <span data-ttu-id="be5c8-132">Note</span><span class="sxs-lookup"><span data-stu-id="be5c8-132">NOTES</span></span>

## <span data-ttu-id="be5c8-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be5c8-133">RELATED LINKS</span></span>

[<span data-ttu-id="be5c8-134">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="be5c8-134">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="be5c8-135">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="be5c8-135">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="be5c8-136">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="be5c8-136">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="be5c8-137">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="be5c8-137">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="be5c8-138">Stop-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="be5c8-138">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)



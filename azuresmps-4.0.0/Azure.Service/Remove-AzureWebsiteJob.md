---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 545CAB1C-F08C-4472-A41A-1FE900D2EDA5
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc8ae51b2f239fd9ec7f09fe27e08ccdaa41c4bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023440"
---
# <span data-ttu-id="1f592-101">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="1f592-101">Remove-AzureWebsiteJob</span></span>

## <span data-ttu-id="1f592-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f592-102">SYNOPSIS</span></span>
<span data-ttu-id="1f592-103">Rimuove un processo Web esistente per un sito Web.</span><span class="sxs-lookup"><span data-stu-id="1f592-103">Removes an existing web job for a website.</span></span>

## <span data-ttu-id="1f592-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f592-104">SYNTAX</span></span>

```
Remove-AzureWebsiteJob -JobName <String> -JobType <WebJobType> [-Force] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1f592-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f592-105">DESCRIPTION</span></span>
<span data-ttu-id="1f592-106">Rimuove un processo Web esistente per un sito Web.</span><span class="sxs-lookup"><span data-stu-id="1f592-106">Removes an existing web job for a website.</span></span>

## <span data-ttu-id="1f592-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f592-107">EXAMPLES</span></span>

### <span data-ttu-id="1f592-108">Esempio 1: rimuovere un processo Web esistente per un sito Web</span><span class="sxs-lookup"><span data-stu-id="1f592-108">Example 1: Remove an existing web job for a website</span></span>
```
PS C:\> Remove-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous
```

<span data-ttu-id="1f592-109">Rimuove un processo Web denominato MyWebJob per sito Web.</span><span class="sxs-lookup"><span data-stu-id="1f592-109">Removes a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="1f592-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f592-110">PARAMETERS</span></span>

### <span data-ttu-id="1f592-111">-Force</span><span class="sxs-lookup"><span data-stu-id="1f592-111">-Force</span></span>
<span data-ttu-id="1f592-112">Indica che questo cmdlet rimuove il processo Web senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="1f592-112">Indicates that this cmdlet removes the web job without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f592-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="1f592-113">-JobName</span></span>
<span data-ttu-id="1f592-114">Il nome del processo Web.</span><span class="sxs-lookup"><span data-stu-id="1f592-114">The web job name.</span></span>

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

### <span data-ttu-id="1f592-115">-JobType</span><span class="sxs-lookup"><span data-stu-id="1f592-115">-JobType</span></span>
<span data-ttu-id="1f592-116">Tipo di processo Web.</span><span class="sxs-lookup"><span data-stu-id="1f592-116">The web job type.</span></span>
<span data-ttu-id="1f592-117">Può essere attivato o continuo.</span><span class="sxs-lookup"><span data-stu-id="1f592-117">Can be triggered or continuous.</span></span>

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

### <span data-ttu-id="1f592-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f592-118">-Name</span></span>
<span data-ttu-id="1f592-119">Il nome del sito Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f592-119">The name of the Azure website.</span></span>

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

### <span data-ttu-id="1f592-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="1f592-120">-Profile</span></span>
<span data-ttu-id="1f592-121">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f592-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1f592-122">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="1f592-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1f592-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="1f592-123">-Slot</span></span>
<span data-ttu-id="1f592-124">Nome dello slot del sito Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f592-124">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="1f592-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f592-125">CommonParameters</span></span>
<span data-ttu-id="1f592-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f592-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f592-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f592-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f592-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f592-128">INPUTS</span></span>

## <span data-ttu-id="1f592-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f592-129">OUTPUTS</span></span>

## <span data-ttu-id="1f592-130">Note</span><span class="sxs-lookup"><span data-stu-id="1f592-130">NOTES</span></span>

## <span data-ttu-id="1f592-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f592-131">RELATED LINKS</span></span>

[<span data-ttu-id="1f592-132">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="1f592-132">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="1f592-133">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="1f592-133">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="1f592-134">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="1f592-134">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="1f592-135">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="1f592-135">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="1f592-136">Stop-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="1f592-136">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)



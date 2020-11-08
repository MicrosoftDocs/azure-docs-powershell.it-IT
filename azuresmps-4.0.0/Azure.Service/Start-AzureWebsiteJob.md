---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A66ADA39-56D9-421B-BC69-996253352236
online version: ''
schema: 2.0.0
ms.openlocfilehash: b5b2cfaea544b5a8575715ec89735b5b9a1ad28f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023725"
---
# <span data-ttu-id="ce89f-101">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="ce89f-101">Start-AzureWebsiteJob</span></span>

## <span data-ttu-id="ce89f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce89f-102">SYNOPSIS</span></span>
<span data-ttu-id="ce89f-103">Avvia un processo Web per un sito Web.</span><span class="sxs-lookup"><span data-stu-id="ce89f-103">Starts a web job for a website.</span></span>

## <span data-ttu-id="ce89f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce89f-104">SYNTAX</span></span>

```
Start-AzureWebsiteJob -JobName <String> -JobType <WebJobType> [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ce89f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce89f-105">DESCRIPTION</span></span>
<span data-ttu-id="ce89f-106">Il cmdlet **Start-AzureWebsiteJob** avvia un processo Web per un sito Web.</span><span class="sxs-lookup"><span data-stu-id="ce89f-106">The **Start-AzureWebsiteJob** cmdlet starts a web job for a website.</span></span>

## <span data-ttu-id="ce89f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce89f-107">EXAMPLES</span></span>

### <span data-ttu-id="ce89f-108">Esempio 1: avviare un processo Web per un sito Web</span><span class="sxs-lookup"><span data-stu-id="ce89f-108">Example 1: Start a web job for a website</span></span>
```
PS C:\> Start-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous
```

<span data-ttu-id="ce89f-109">Avvia un processo Web denominato MyWebJob per sito Web.</span><span class="sxs-lookup"><span data-stu-id="ce89f-109">Starts a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="ce89f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce89f-110">PARAMETERS</span></span>

### <span data-ttu-id="ce89f-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="ce89f-111">-JobName</span></span>
<span data-ttu-id="ce89f-112">Il nome del processo Web.</span><span class="sxs-lookup"><span data-stu-id="ce89f-112">The web job name.</span></span>

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

### <span data-ttu-id="ce89f-113">-JobType</span><span class="sxs-lookup"><span data-stu-id="ce89f-113">-JobType</span></span>
<span data-ttu-id="ce89f-114">Tipo di processo Web.</span><span class="sxs-lookup"><span data-stu-id="ce89f-114">The web job type.</span></span>
<span data-ttu-id="ce89f-115">Può essere attivato o continuo.</span><span class="sxs-lookup"><span data-stu-id="ce89f-115">Can be triggered or continuous.</span></span>

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

### <span data-ttu-id="ce89f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce89f-116">-Name</span></span>
<span data-ttu-id="ce89f-117">Il nome del sito Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="ce89f-117">The name of the Azure website.</span></span>

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

### <span data-ttu-id="ce89f-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce89f-118">-PassThru</span></span>
<span data-ttu-id="ce89f-119">Restituisce un valore booleano che indica che il processo è stato avviato correttamente.</span><span class="sxs-lookup"><span data-stu-id="ce89f-119">Returns a boolean value indicating that the job started successfully.</span></span>
<span data-ttu-id="ce89f-120">Per impostazione predefinita, questo cmdlet non restituisce alcun output.</span><span class="sxs-lookup"><span data-stu-id="ce89f-120">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="ce89f-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="ce89f-121">-Profile</span></span>
<span data-ttu-id="ce89f-122">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce89f-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ce89f-123">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="ce89f-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ce89f-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="ce89f-124">-Slot</span></span>
<span data-ttu-id="ce89f-125">Nome dello slot del sito Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="ce89f-125">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="ce89f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce89f-126">CommonParameters</span></span>
<span data-ttu-id="ce89f-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce89f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce89f-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce89f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce89f-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce89f-129">INPUTS</span></span>

## <span data-ttu-id="ce89f-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce89f-130">OUTPUTS</span></span>

## <span data-ttu-id="ce89f-131">Note</span><span class="sxs-lookup"><span data-stu-id="ce89f-131">NOTES</span></span>

## <span data-ttu-id="ce89f-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce89f-132">RELATED LINKS</span></span>

[<span data-ttu-id="ce89f-133">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ce89f-133">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="ce89f-134">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="ce89f-134">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="ce89f-135">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="ce89f-135">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="ce89f-136">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="ce89f-136">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="ce89f-137">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="ce89f-137">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)



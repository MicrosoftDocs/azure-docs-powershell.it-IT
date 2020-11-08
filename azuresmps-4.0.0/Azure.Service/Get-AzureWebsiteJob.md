---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6B406310-287F-4BD3-BA38-A9C97E8EDC45
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9f68ca1667e7b028c7646bf5a569e4e467c1b03
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029735"
---
# <span data-ttu-id="2fa69-101">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="2fa69-101">Get-AzureWebsiteJob</span></span>

## <span data-ttu-id="2fa69-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2fa69-102">SYNOPSIS</span></span>
<span data-ttu-id="2fa69-103">Ottiene i processi Web associati a un sito Web.</span><span class="sxs-lookup"><span data-stu-id="2fa69-103">Gets the web jobs associated with a website.</span></span>

## <span data-ttu-id="2fa69-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fa69-104">SYNTAX</span></span>

```
Get-AzureWebsiteJob [-JobName <String>] [-JobType <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2fa69-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fa69-105">DESCRIPTION</span></span>
<span data-ttu-id="2fa69-106">Ottiene i processi Web associati a un sito Web.</span><span class="sxs-lookup"><span data-stu-id="2fa69-106">Gets the web jobs associated with a website.</span></span>

## <span data-ttu-id="2fa69-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fa69-107">EXAMPLES</span></span>

### <span data-ttu-id="2fa69-108">Esempio 1: ottenere informazioni specifiche sul processo Web</span><span class="sxs-lookup"><span data-stu-id="2fa69-108">Example 1: Get specific web job info</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="2fa69-109">Ottiene un processo Web denominato MyWebJob dallo slot di produzione sito Web.</span><span class="sxs-lookup"><span data-stu-id="2fa69-109">Gets a web job called MyWebJob from MyWebsite production slot.</span></span>

### <span data-ttu-id="2fa69-110">Esempio 2: ottenere tutti i processi Web per un sito Web</span><span class="sxs-lookup"><span data-stu-id="2fa69-110">Example 2: Get all web jobs for a website</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite
```

<span data-ttu-id="2fa69-111">Ottiene tutti i processi Web associati allo slot di produzione sito Web.</span><span class="sxs-lookup"><span data-stu-id="2fa69-111">Gets all web jobs associated with MyWebsite production slot.</span></span>

### <span data-ttu-id="2fa69-112">Esempio 3: ottenere tutti i processi Web attivati</span><span class="sxs-lookup"><span data-stu-id="2fa69-112">Example 3: Get all triggered web jobs</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -Slot staging -Type Triggered
```

<span data-ttu-id="2fa69-113">Ottiene tutti i processi Web attivati dallo slot di staging di sito Web.</span><span class="sxs-lookup"><span data-stu-id="2fa69-113">Gets all triggered web jobs from staging slot of MyWebsite.</span></span>

## <span data-ttu-id="2fa69-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2fa69-114">PARAMETERS</span></span>

### <span data-ttu-id="2fa69-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="2fa69-115">-JobName</span></span>
<span data-ttu-id="2fa69-116">Il nome del processo Web</span><span class="sxs-lookup"><span data-stu-id="2fa69-116">The web job name</span></span>

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

### <span data-ttu-id="2fa69-117">-JobType</span><span class="sxs-lookup"><span data-stu-id="2fa69-117">-JobType</span></span>
<span data-ttu-id="2fa69-118">Tipo di processo Web.</span><span class="sxs-lookup"><span data-stu-id="2fa69-118">The web job type.</span></span>
<span data-ttu-id="2fa69-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2fa69-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2fa69-120">Attivata</span><span class="sxs-lookup"><span data-stu-id="2fa69-120">Triggered</span></span>
- <span data-ttu-id="2fa69-121">Continua</span><span class="sxs-lookup"><span data-stu-id="2fa69-121">Continuous</span></span>

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

### <span data-ttu-id="2fa69-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2fa69-122">-Name</span></span>
<span data-ttu-id="2fa69-123">Il nome del sito Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="2fa69-123">The name of the Azure website.</span></span>

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

### <span data-ttu-id="2fa69-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="2fa69-124">-Profile</span></span>
<span data-ttu-id="2fa69-125">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fa69-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2fa69-126">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="2fa69-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2fa69-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="2fa69-127">-Slot</span></span>
<span data-ttu-id="2fa69-128">Nome dello slot del sito Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="2fa69-128">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="2fa69-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fa69-129">CommonParameters</span></span>
<span data-ttu-id="2fa69-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fa69-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fa69-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fa69-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fa69-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2fa69-132">INPUTS</span></span>

## <span data-ttu-id="2fa69-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fa69-133">OUTPUTS</span></span>

## <span data-ttu-id="2fa69-134">Note</span><span class="sxs-lookup"><span data-stu-id="2fa69-134">NOTES</span></span>

## <span data-ttu-id="2fa69-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fa69-135">RELATED LINKS</span></span>

[<span data-ttu-id="2fa69-136">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="2fa69-136">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="2fa69-137">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="2fa69-137">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="2fa69-138">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="2fa69-138">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="2fa69-139">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="2fa69-139">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="2fa69-140">Stop-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="2fa69-140">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)



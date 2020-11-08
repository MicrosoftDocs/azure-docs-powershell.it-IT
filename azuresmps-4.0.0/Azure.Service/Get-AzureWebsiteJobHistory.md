---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A2CBF963-1FAE-41B0-964E-EFF52076AB32
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c4bb84111b8ec22b1b529622e61ca476cf6081b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029969"
---
# <span data-ttu-id="5de44-101">Get-AzureWebsiteJobHistory</span><span class="sxs-lookup"><span data-stu-id="5de44-101">Get-AzureWebsiteJobHistory</span></span>

## <span data-ttu-id="5de44-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5de44-102">SYNOPSIS</span></span>
<span data-ttu-id="5de44-103">Ottiene una cronologia del processo Web.</span><span class="sxs-lookup"><span data-stu-id="5de44-103">Gets a web job history.</span></span>

## <span data-ttu-id="5de44-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5de44-104">SYNTAX</span></span>

### <span data-ttu-id="5de44-105">HistoryParameterSetName</span><span class="sxs-lookup"><span data-stu-id="5de44-105">HistoryParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="5de44-106">RunIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="5de44-106">RunIdParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> -RunId <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5de44-107">LatestParameterSetName</span><span class="sxs-lookup"><span data-stu-id="5de44-107">LatestParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> [-Latest] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5de44-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5de44-108">DESCRIPTION</span></span>
<span data-ttu-id="5de44-109">Ottiene una cronologia del processo Web.</span><span class="sxs-lookup"><span data-stu-id="5de44-109">Gets a web job history.</span></span>

## <span data-ttu-id="5de44-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5de44-110">EXAMPLES</span></span>

### <span data-ttu-id="5de44-111">Esempio 1: ottenere la cronologia completa per un processo Web</span><span class="sxs-lookup"><span data-stu-id="5de44-111">Example 1: Get complete history for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="5de44-112">Ottiene la cronologia completa per MyWebJob.</span><span class="sxs-lookup"><span data-stu-id="5de44-112">Gets complete history for MyWebJob.</span></span>

### <span data-ttu-id="5de44-113">Esempio 2: ottenere l'ultima esecuzione per un processo Web</span><span class="sxs-lookup"><span data-stu-id="5de44-113">Example 2: Get latest run for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob -Latest
```

<span data-ttu-id="5de44-114">Ottiene le informazioni di esecuzione più recenti per MyWebJob.</span><span class="sxs-lookup"><span data-stu-id="5de44-114">Gets latest run info for MyWebJob.</span></span>

### <span data-ttu-id="5de44-115">Esempio 3: ottenere una specifica esecuzione per un processo Web</span><span class="sxs-lookup"><span data-stu-id="5de44-115">Example 3: Get specific run for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob -RunId 10
```

<span data-ttu-id="5de44-116">Ottiene tutte le informazioni su Run con ID 10 per MyWebJob.</span><span class="sxs-lookup"><span data-stu-id="5de44-116">Gets all info about run with id 10 for MyWebJob.</span></span>

## <span data-ttu-id="5de44-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5de44-117">PARAMETERS</span></span>

### <span data-ttu-id="5de44-118">-JobName</span><span class="sxs-lookup"><span data-stu-id="5de44-118">-JobName</span></span>
<span data-ttu-id="5de44-119">Il nome del processo Web.</span><span class="sxs-lookup"><span data-stu-id="5de44-119">The web job name.</span></span>

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

### <span data-ttu-id="5de44-120">-Ultimi</span><span class="sxs-lookup"><span data-stu-id="5de44-120">-Latest</span></span>
<span data-ttu-id="5de44-121">Se specificato, restituire la cronologia di esecuzione più recente.</span><span class="sxs-lookup"><span data-stu-id="5de44-121">If specified, return the latest run history.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LatestParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5de44-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="5de44-122">-Name</span></span>
<span data-ttu-id="5de44-123">Il nome del sito Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="5de44-123">The name of the Azure website.</span></span>

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

### <span data-ttu-id="5de44-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="5de44-124">-Profile</span></span>
<span data-ttu-id="5de44-125">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5de44-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5de44-126">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="5de44-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5de44-127">-RunId</span><span class="sxs-lookup"><span data-stu-id="5de44-127">-RunId</span></span>
<span data-ttu-id="5de44-128">Specifica l'ID della cronologia di esecuzione che vuoi visualizzare.</span><span class="sxs-lookup"><span data-stu-id="5de44-128">Specifies the ID of the run history you want to see.</span></span>

```yaml
Type: String
Parameter Sets: RunIdParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5de44-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="5de44-129">-Slot</span></span>
<span data-ttu-id="5de44-130">Nome dello slot del sito Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="5de44-130">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="5de44-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5de44-131">CommonParameters</span></span>
<span data-ttu-id="5de44-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5de44-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5de44-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5de44-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5de44-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5de44-134">INPUTS</span></span>

## <span data-ttu-id="5de44-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5de44-135">OUTPUTS</span></span>

## <span data-ttu-id="5de44-136">Note</span><span class="sxs-lookup"><span data-stu-id="5de44-136">NOTES</span></span>

## <span data-ttu-id="5de44-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5de44-137">RELATED LINKS</span></span>

[<span data-ttu-id="5de44-138">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5de44-138">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="5de44-139">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5de44-139">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="5de44-140">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="5de44-140">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="5de44-141">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="5de44-141">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="5de44-142">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="5de44-142">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)



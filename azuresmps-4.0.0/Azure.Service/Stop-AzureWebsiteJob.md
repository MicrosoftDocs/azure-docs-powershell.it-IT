---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7D39F4C9-F37A-4BBE-BF02-1F036A9FC5E8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0ec095393d68bb6764fa463941f1cd2b9644092f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023796"
---
# <span data-ttu-id="4fc74-101">Stop-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="4fc74-101">Stop-AzureWebsiteJob</span></span>

## <span data-ttu-id="4fc74-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4fc74-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc74-103">Arresta un processo Web per un sito Web.</span><span class="sxs-lookup"><span data-stu-id="4fc74-103">Stops a web job for a website.</span></span>

## <span data-ttu-id="4fc74-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4fc74-104">SYNTAX</span></span>

```
Stop-AzureWebsiteJob -JobName <String> [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4fc74-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fc74-105">DESCRIPTION</span></span>
<span data-ttu-id="4fc74-106">Il cmdlet **Stop-AzureWebsiteJob** arresta un processo Web per un sito Web.</span><span class="sxs-lookup"><span data-stu-id="4fc74-106">The **Stop-AzureWebsiteJob** cmdlet stops a web job for a website.</span></span>

## <span data-ttu-id="4fc74-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4fc74-107">EXAMPLES</span></span>

### <span data-ttu-id="4fc74-108">Esempio 1: arrestare un processo Web per un sito Web</span><span class="sxs-lookup"><span data-stu-id="4fc74-108">Example 1: Stop a web job for a website</span></span>
```
PS C:\> Stop-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="4fc74-109">Interrompe un processo Web denominato MyWebJob per sito Web.</span><span class="sxs-lookup"><span data-stu-id="4fc74-109">Stops a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="4fc74-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4fc74-110">PARAMETERS</span></span>

### <span data-ttu-id="4fc74-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="4fc74-111">-JobName</span></span>
<span data-ttu-id="4fc74-112">Il nome del processo Web.</span><span class="sxs-lookup"><span data-stu-id="4fc74-112">The web job name.</span></span>

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

### <span data-ttu-id="4fc74-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4fc74-113">-Name</span></span>
<span data-ttu-id="4fc74-114">Il nome del sito Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="4fc74-114">The name of the Azure website.</span></span>

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

### <span data-ttu-id="4fc74-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fc74-115">-PassThru</span></span>
<span data-ttu-id="4fc74-116">Restituisce un valore booleano che indica che il processo è stato interrotto correttamente.</span><span class="sxs-lookup"><span data-stu-id="4fc74-116">Returns a boolean value indicating that the job stopped successfully.</span></span>
<span data-ttu-id="4fc74-117">Per impostazione predefinita, questo cmdlet non restituisce alcun output.</span><span class="sxs-lookup"><span data-stu-id="4fc74-117">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="4fc74-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="4fc74-118">-Profile</span></span>
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

### <span data-ttu-id="4fc74-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="4fc74-119">-Slot</span></span>
<span data-ttu-id="4fc74-120">Nome dello slot del sito Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="4fc74-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="4fc74-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc74-121">CommonParameters</span></span>
<span data-ttu-id="4fc74-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fc74-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc74-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fc74-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc74-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4fc74-124">INPUTS</span></span>

## <span data-ttu-id="4fc74-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4fc74-125">OUTPUTS</span></span>

## <span data-ttu-id="4fc74-126">Note</span><span class="sxs-lookup"><span data-stu-id="4fc74-126">NOTES</span></span>

## <span data-ttu-id="4fc74-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4fc74-127">RELATED LINKS</span></span>

[<span data-ttu-id="4fc74-128">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="4fc74-128">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)

[<span data-ttu-id="4fc74-129">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="4fc74-129">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="4fc74-130">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="4fc74-130">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="4fc74-131">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="4fc74-131">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="4fc74-132">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="4fc74-132">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)



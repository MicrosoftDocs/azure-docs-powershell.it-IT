---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountapiproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
ms.openlocfilehash: 97cf393d0d95dbc9ecfec06f53795713f59aecbd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205042"
---
# <span data-ttu-id="aeed0-101">New-AzCognitiveServicesAccountApiProperty</span><span class="sxs-lookup"><span data-stu-id="aeed0-101">New-AzCognitiveServicesAccountApiProperty</span></span>

## <span data-ttu-id="aeed0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aeed0-102">SYNOPSIS</span></span>
<span data-ttu-id="aeed0-103">Generare una nuova istanza dell'account di Servizi cognitivi ApiProperties</span><span class="sxs-lookup"><span data-stu-id="aeed0-103">Generate a new instance of Cognitive Services Account ApiProperties</span></span>

## <span data-ttu-id="aeed0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aeed0-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountApiProperty [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aeed0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aeed0-105">DESCRIPTION</span></span>
<span data-ttu-id="aeed0-106">Generare una nuova istanza dell'account di Servizi cognitivi ApiProperties.</span><span class="sxs-lookup"><span data-stu-id="aeed0-106">Generate a new instance of Cognitive Services Account ApiProperties.</span></span>
<span data-ttu-id="aeed0-107">ApiProperties può essere usata quando si crea un nuovo account o si aggiorna un account esistente.</span><span class="sxs-lookup"><span data-stu-id="aeed0-107">ApiProperties can be used when creating a new account or updating an existing account.</span></span>
<span data-ttu-id="aeed0-108">ApiProperties è necessaria per alcuni tipi di account.</span><span class="sxs-lookup"><span data-stu-id="aeed0-108">ApiProperties is required by certain account types.</span></span>

## <span data-ttu-id="aeed0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aeed0-109">EXAMPLES</span></span>

### <span data-ttu-id="aeed0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aeed0-110">Example 1</span></span>
```powershell
PS C:\> $apiProperties = New-AzCognitiveServicesAccountApiProperty
PS C:\> $apiProperties.QnaRuntimeEndpoint = "https://qnamaker.azurewebsites.net"
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name qnamaker -Type QnAMaker -SkuName S0 -Locatio WestUS -ApiProperty $apiProperties
```

<span data-ttu-id="aeed0-111">L'esempio precedente crea un account QnAMaker, con la proprietà API "QnaRuntimeEndpoint".</span><span class="sxs-lookup"><span data-stu-id="aeed0-111">Above example will create an QnAMaker account, with API property "QnaRuntimeEndpoint".</span></span>


## <span data-ttu-id="aeed0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aeed0-112">PARAMETERS</span></span>

### <span data-ttu-id="aeed0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeed0-113">-DefaultProfile</span></span>
<span data-ttu-id="aeed0-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aeed0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeed0-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aeed0-115">-Confirm</span></span>
<span data-ttu-id="aeed0-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aeed0-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeed0-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aeed0-117">-WhatIf</span></span>
<span data-ttu-id="aeed0-118">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aeed0-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aeed0-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aeed0-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aeed0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeed0-120">CommonParameters</span></span>
<span data-ttu-id="aeed0-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeed0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeed0-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aeed0-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeed0-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="aeed0-123">INPUTS</span></span>

### <span data-ttu-id="aeed0-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="aeed0-124">None</span></span>

## <span data-ttu-id="aeed0-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aeed0-125">OUTPUTS</span></span>

### <span data-ttu-id="aeed0-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span><span class="sxs-lookup"><span data-stu-id="aeed0-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span></span>

## <span data-ttu-id="aeed0-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="aeed0-127">NOTES</span></span>

## <span data-ttu-id="aeed0-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aeed0-128">RELATED LINKS</span></span>

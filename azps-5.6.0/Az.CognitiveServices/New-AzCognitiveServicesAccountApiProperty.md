---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountapiproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
ms.openlocfilehash: 50e62158d4b24282753c726845e7dd88d492843c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981197"
---
# <span data-ttu-id="2deda-101">New-AzCognitiveServicesAccountApiProperty</span><span class="sxs-lookup"><span data-stu-id="2deda-101">New-AzCognitiveServicesAccountApiProperty</span></span>

## <span data-ttu-id="2deda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2deda-102">SYNOPSIS</span></span>
<span data-ttu-id="2deda-103">Generare una nuova istanza di Account ApiProperties di Servizi cognitivi</span><span class="sxs-lookup"><span data-stu-id="2deda-103">Generate a new instance of Cognitive Services Account ApiProperties</span></span>

## <span data-ttu-id="2deda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2deda-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountApiProperty [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2deda-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2deda-105">DESCRIPTION</span></span>
<span data-ttu-id="2deda-106">Generare una nuova istanza di Account ApiProperties di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="2deda-106">Generate a new instance of Cognitive Services Account ApiProperties.</span></span>
<span data-ttu-id="2deda-107">ApiProperties può essere usata quando si crea un nuovo account o si aggiorna un account esistente.</span><span class="sxs-lookup"><span data-stu-id="2deda-107">ApiProperties can be used when creating a new account or updating an existing account.</span></span>
<span data-ttu-id="2deda-108">ApiProperties è necessaria per alcuni tipi di account.</span><span class="sxs-lookup"><span data-stu-id="2deda-108">ApiProperties is required by certain account types.</span></span>

## <span data-ttu-id="2deda-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2deda-109">EXAMPLES</span></span>

### <span data-ttu-id="2deda-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2deda-110">Example 1</span></span>
```powershell
PS C:\> $apiProperties = New-AzCognitiveServicesAccountApiProperty
PS C:\> $apiProperties.QnaRuntimeEndpoint = "https://qnamaker.azurewebsites.net"
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name qnamaker -Type QnAMaker -SkuName S0 -Locatio WestUS -ApiProperty $apiProperties
```

<span data-ttu-id="2deda-111">In questo esempio verrà creato un account QnAMaker con la proprietà API "QnaRuntimeEndpoint".</span><span class="sxs-lookup"><span data-stu-id="2deda-111">Above example will create an QnAMaker account, with API property "QnaRuntimeEndpoint".</span></span>


## <span data-ttu-id="2deda-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2deda-112">PARAMETERS</span></span>

### <span data-ttu-id="2deda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2deda-113">-DefaultProfile</span></span>
<span data-ttu-id="2deda-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2deda-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2deda-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2deda-115">-Confirm</span></span>
<span data-ttu-id="2deda-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2deda-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2deda-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2deda-117">-WhatIf</span></span>
<span data-ttu-id="2deda-118">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2deda-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2deda-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2deda-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2deda-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2deda-120">CommonParameters</span></span>
<span data-ttu-id="2deda-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2deda-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2deda-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2deda-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2deda-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="2deda-123">INPUTS</span></span>

### <span data-ttu-id="2deda-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2deda-124">None</span></span>

## <span data-ttu-id="2deda-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2deda-125">OUTPUTS</span></span>

### <span data-ttu-id="2deda-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span><span class="sxs-lookup"><span data-stu-id="2deda-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span></span>

## <span data-ttu-id="2deda-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="2deda-127">NOTES</span></span>

## <span data-ttu-id="2deda-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2deda-128">RELATED LINKS</span></span>

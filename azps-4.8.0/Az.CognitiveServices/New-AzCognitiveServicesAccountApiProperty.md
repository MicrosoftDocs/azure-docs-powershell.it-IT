---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountapiproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
ms.openlocfilehash: 97cf393d0d95dbc9ecfec06f53795713f59aecbd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191642"
---
# <span data-ttu-id="5ddff-101">New-AzCognitiveServicesAccountApiProperty</span><span class="sxs-lookup"><span data-stu-id="5ddff-101">New-AzCognitiveServicesAccountApiProperty</span></span>

## <span data-ttu-id="5ddff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ddff-102">SYNOPSIS</span></span>
<span data-ttu-id="5ddff-103">Generare una nuova istanza di account dei servizi cognitivi ApiProperties</span><span class="sxs-lookup"><span data-stu-id="5ddff-103">Generate a new instance of Cognitive Services Account ApiProperties</span></span>

## <span data-ttu-id="5ddff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ddff-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountApiProperty [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ddff-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ddff-105">DESCRIPTION</span></span>
<span data-ttu-id="5ddff-106">Genera una nuova istanza di ApiProperties account dei servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="5ddff-106">Generate a new instance of Cognitive Services Account ApiProperties.</span></span>
<span data-ttu-id="5ddff-107">ApiProperties può essere usato quando si crea un nuovo account o si aggiorna un account esistente.</span><span class="sxs-lookup"><span data-stu-id="5ddff-107">ApiProperties can be used when creating a new account or updating an existing account.</span></span>
<span data-ttu-id="5ddff-108">ApiProperties è richiesto da determinati tipi di account.</span><span class="sxs-lookup"><span data-stu-id="5ddff-108">ApiProperties is required by certain account types.</span></span>

## <span data-ttu-id="5ddff-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ddff-109">EXAMPLES</span></span>

### <span data-ttu-id="5ddff-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5ddff-110">Example 1</span></span>
```powershell
PS C:\> $apiProperties = New-AzCognitiveServicesAccountApiProperty
PS C:\> $apiProperties.QnaRuntimeEndpoint = "https://qnamaker.azurewebsites.net"
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name qnamaker -Type QnAMaker -SkuName S0 -Locatio WestUS -ApiProperty $apiProperties
```

<span data-ttu-id="5ddff-111">Sopra l'esempio verrà creato un account QnAMaker con la proprietà API "QnaRuntimeEndpoint".</span><span class="sxs-lookup"><span data-stu-id="5ddff-111">Above example will create an QnAMaker account, with API property "QnaRuntimeEndpoint".</span></span>


## <span data-ttu-id="5ddff-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ddff-112">PARAMETERS</span></span>

### <span data-ttu-id="5ddff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ddff-113">-DefaultProfile</span></span>
<span data-ttu-id="5ddff-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ddff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ddff-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5ddff-115">-Confirm</span></span>
<span data-ttu-id="5ddff-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ddff-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ddff-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ddff-117">-WhatIf</span></span>
<span data-ttu-id="5ddff-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ddff-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ddff-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ddff-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ddff-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ddff-120">CommonParameters</span></span>
<span data-ttu-id="5ddff-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ddff-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ddff-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ddff-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ddff-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ddff-123">INPUTS</span></span>

### <span data-ttu-id="5ddff-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5ddff-124">None</span></span>

## <span data-ttu-id="5ddff-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ddff-125">OUTPUTS</span></span>

### <span data-ttu-id="5ddff-126">Microsoft. Azure. Management. CognitiveServices. Models. CognitiveServicesAccountApiProperties</span><span class="sxs-lookup"><span data-stu-id="5ddff-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span></span>

## <span data-ttu-id="5ddff-127">Note</span><span class="sxs-lookup"><span data-stu-id="5ddff-127">NOTES</span></span>

## <span data-ttu-id="5ddff-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ddff-128">RELATED LINKS</span></span>
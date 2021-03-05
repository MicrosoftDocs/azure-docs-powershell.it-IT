---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
ms.openlocfilehash: 5bf841e055c81293d6f2f9c5811ad4e1aa1a2f95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005758"
---
# <span data-ttu-id="e4d8d-101">Set-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="e4d8d-101">Set-AzSecurityAssessment</span></span>

## <span data-ttu-id="e4d8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="e4d8d-103">Creare o aggiornare un risultato della valutazione della sicurezza per una risorsa</span><span class="sxs-lookup"><span data-stu-id="e4d8d-103">Create or update a security assessment result on a resource</span></span>

## <span data-ttu-id="e4d8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4d8d-104">SYNTAX</span></span>

### <span data-ttu-id="e4d8d-105">SubscriptionLevelResource (Default)</span><span class="sxs-lookup"><span data-stu-id="e4d8d-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAssessment -Name <String> [-StatusCode <String>] [-StatusCause <String>]
 [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4d8d-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="e4d8d-106">ResourceIdLevelResource</span></span>
```
Set-AzSecurityAssessment -Name <String> -AssessedResourceId <String> -StatusCode <String>
 [-StatusCause <String>] [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4d8d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e4d8d-107">DESCRIPTION</span></span>
<span data-ttu-id="e4d8d-108">Creare o aggiornare un risultato della valutazione della sicurezza per una risorsa, può essere usato per modificare lo stato di un risultato esistente o aggiungere altri dati.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-108">Create or update a security assessment result on a resource, can be used to change the status of an existing result or add additional data.</span></span>
<span data-ttu-id="e4d8d-109">può essere usato solo per i tipi di valutazione "CustomerManaged" e solo dopo aver creato i metadati della valutazione corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-109">can only be used for "CustomerManaged" assessment types and only after the matched assessment metadata is created.</span></span>

## <span data-ttu-id="e4d8d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4d8d-110">EXAMPLES</span></span>

### <span data-ttu-id="e4d8d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e4d8d-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D -StatusCode "Unhealthy"
```

<span data-ttu-id="e4d8d-112">Contrassegna il risultato della sottoscrizione come "Non integro" per la valutazione del tipo "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D". Ulteriori dettagli sul tipo di valutazione sono disponibili sotto il tipo di strumento di valutazione</span><span class="sxs-lookup"><span data-stu-id="e4d8d-112">Marks the subscription result as "Unhealthy" for assessment of type "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" - more details about the assessment type will be found under the assessmentMetadata type</span></span>

## <span data-ttu-id="e4d8d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4d8d-113">PARAMETERS</span></span>

### <span data-ttu-id="e4d8d-114">-AdditionalData</span><span class="sxs-lookup"><span data-stu-id="e4d8d-114">-AdditionalData</span></span>
<span data-ttu-id="e4d8d-115">Dati associati al risultato della valutazione per migliorare le indagini o una maggiore chiarezza dello stato.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-115">Data that is attached to the assessment result for better investigations or status clarity.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d8d-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="e4d8d-116">-AssessedResourceId</span></span>
<span data-ttu-id="e4d8d-117">ID risorsa completo della risorsa su cui viene calcolata la valutazione.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d8d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4d8d-118">-DefaultProfile</span></span>
<span data-ttu-id="e4d8d-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4d8d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e4d8d-120">-Name</span></span>
<span data-ttu-id="e4d8d-121">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d8d-122">-StatusCause</span><span class="sxs-lookup"><span data-stu-id="e4d8d-122">-StatusCause</span></span>
<span data-ttu-id="e4d8d-123">Codice progremmatico per la causa del risultato della valutazione.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-123">Progremmatic code for the cause of the assessment's result.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d8d-124">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="e4d8d-124">-StatusCode</span></span>
<span data-ttu-id="e4d8d-125">Codice progremmatico per il risultato della valutazione.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-125">Progremmatic code for the result of the assessment.</span></span>
<span data-ttu-id="e4d8d-126">può essere "Integro", "Non integro" o "Nonapplicabile"</span><span class="sxs-lookup"><span data-stu-id="e4d8d-126">can be "Healthy", "Unhealthy" or "NotApplicable"</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d8d-127">-StatusDescription</span><span class="sxs-lookup"><span data-stu-id="e4d8d-127">-StatusDescription</span></span>
<span data-ttu-id="e4d8d-128">Descrizione leggibile e umana della causa del risultato della valutazione.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-128">Human readable description of the cause of the assessment's result.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4d8d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4d8d-129">-Confirm</span></span>
<span data-ttu-id="e4d8d-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4d8d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4d8d-131">-WhatIf</span></span>
<span data-ttu-id="e4d8d-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4d8d-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4d8d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4d8d-134">CommonParameters</span></span>
<span data-ttu-id="e4d8d-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4d8d-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e4d8d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4d8d-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="e4d8d-137">INPUTS</span></span>

### <span data-ttu-id="e4d8d-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e4d8d-138">None</span></span>

## <span data-ttu-id="e4d8d-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4d8d-139">OUTPUTS</span></span>

### <span data-ttu-id="e4d8d-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="e4d8d-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="e4d8d-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="e4d8d-141">NOTES</span></span>

## <span data-ttu-id="e4d8d-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4d8d-142">RELATED LINKS</span></span>

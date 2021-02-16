---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: d65cd0a5f29f15d2d82227aad6520df34fd4357f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208226"
---
# <span data-ttu-id="ed18c-101">Set-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="ed18c-101">Set-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="ed18c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed18c-102">SYNOPSIS</span></span>
<span data-ttu-id="ed18c-103">Crea o aggiorna un tipo di valutazione della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="ed18c-103">Creates or updates a security assessment type.</span></span>

## <span data-ttu-id="ed18c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed18c-104">SYNTAX</span></span>

```
Set-AzSecurityAssessmentMetadata -Name <String> -DisplayName <String> [-Description <String>]
 [-RemediationDescription <String>] [-Severity <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed18c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ed18c-105">DESCRIPTION</span></span>
<span data-ttu-id="ed18c-106">Crea o aggiorna i metadati della valutazione della sicurezza e può essere usato per creare e gestire varie proprietà della valutazione.</span><span class="sxs-lookup"><span data-stu-id="ed18c-106">Creates or updates a security assessment metadata, can be used to create and manage various assessment properties.</span></span>
<span data-ttu-id="ed18c-107">Dopo questa azione sarà possibile segnalare i risultati della valutazione per qualsiasi risorsa della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ed18c-107">After this action you will be able to report assessment results on any resource in this subscription.</span></span>

## <span data-ttu-id="ed18c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed18c-108">EXAMPLES</span></span>

### <span data-ttu-id="ed18c-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ed18c-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessmentMetadata -Name $assessmentGuid -DisplayName "Resource should be secured" -Severity "High" -Description "The resource should be secured according to my company's security policy"
```

<span data-ttu-id="ed18c-110">Creare un nuovo tipo di valutazione in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ed18c-110">Create a new assessment type in a subscription.</span></span>

## <span data-ttu-id="ed18c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed18c-111">PARAMETERS</span></span>

### <span data-ttu-id="ed18c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed18c-112">-DefaultProfile</span></span>
<span data-ttu-id="ed18c-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed18c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed18c-114">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed18c-114">-Description</span></span>
<span data-ttu-id="ed18c-115">Stringa dettagliata che consente agli utenti di comprendere il significato di questa valutazione e la modalità di calcolo.</span><span class="sxs-lookup"><span data-stu-id="ed18c-115">Detailed string that will help users to understand the meaning of this assessment and how it was calculated.</span></span>

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

### <span data-ttu-id="ed18c-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ed18c-116">-DisplayName</span></span>
<span data-ttu-id="ed18c-117">Titolo leggibile e leggibile per questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="ed18c-117">Human readable title for this object.</span></span>

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

### <span data-ttu-id="ed18c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ed18c-118">-Name</span></span>
<span data-ttu-id="ed18c-119">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ed18c-119">Resource name.</span></span>

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

### <span data-ttu-id="ed18c-120">-RemediationDescription</span><span class="sxs-lookup"><span data-stu-id="ed18c-120">-RemediationDescription</span></span>
<span data-ttu-id="ed18c-121">Stringa dettagliata che consente agli utenti di comprendere i diversi modi per attenuare o risolvere il problema di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="ed18c-121">Detailed string that will help users to understand the different ways to mitigate or fix the security issue.</span></span>

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

### <span data-ttu-id="ed18c-122">-Gravità</span><span class="sxs-lookup"><span data-stu-id="ed18c-122">-Severity</span></span>
<span data-ttu-id="ed18c-123">Indica l'importanza del rischio di sicurezza se la valutazione non è integra.</span><span class="sxs-lookup"><span data-stu-id="ed18c-123">Indicates the importance of the security risk if the assessment is unhealthy.</span></span>

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

### <span data-ttu-id="ed18c-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed18c-124">-Confirm</span></span>
<span data-ttu-id="ed18c-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed18c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed18c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed18c-126">-WhatIf</span></span>
<span data-ttu-id="ed18c-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed18c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed18c-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed18c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed18c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed18c-129">CommonParameters</span></span>
<span data-ttu-id="ed18c-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed18c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed18c-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ed18c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed18c-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="ed18c-132">INPUTS</span></span>

### <span data-ttu-id="ed18c-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ed18c-133">None</span></span>

## <span data-ttu-id="ed18c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed18c-134">OUTPUTS</span></span>

### <span data-ttu-id="ed18c-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="ed18c-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="ed18c-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="ed18c-136">NOTES</span></span>

## <span data-ttu-id="ed18c-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed18c-137">RELATED LINKS</span></span>

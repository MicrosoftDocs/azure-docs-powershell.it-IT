---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: d65cd0a5f29f15d2d82227aad6520df34fd4357f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201464"
---
# <span data-ttu-id="309d7-101">Set-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="309d7-101">Set-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="309d7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="309d7-102">SYNOPSIS</span></span>
<span data-ttu-id="309d7-103">Crea o aggiorna un tipo di valutazione della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="309d7-103">Creates or updates a security assessment type.</span></span>

## <span data-ttu-id="309d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="309d7-104">SYNTAX</span></span>

```
Set-AzSecurityAssessmentMetadata -Name <String> -DisplayName <String> [-Description <String>]
 [-RemediationDescription <String>] [-Severity <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="309d7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="309d7-105">DESCRIPTION</span></span>
<span data-ttu-id="309d7-106">Crea o aggiorna i metadati di valutazione della sicurezza, può essere usato per creare e gestire varie proprietà di valutazione.</span><span class="sxs-lookup"><span data-stu-id="309d7-106">Creates or updates a security assessment metadata, can be used to create and manage various assessment properties.</span></span>
<span data-ttu-id="309d7-107">Dopo questa azione potrai segnalare i risultati della valutazione in tutte le risorse di questo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="309d7-107">After this action you will be able to report assessment results on any resource in this subscription.</span></span>

## <span data-ttu-id="309d7-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="309d7-108">EXAMPLES</span></span>

### <span data-ttu-id="309d7-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="309d7-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessmentMetadata -Name $assessmentGuid -DisplayName "Resource should be secured" -Severity "High" -Description "The resource should be secured according to my company's security policy"
```

<span data-ttu-id="309d7-110">Creare un nuovo tipo di valutazione in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="309d7-110">Create a new assessment type in a subscription.</span></span>

## <span data-ttu-id="309d7-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="309d7-111">PARAMETERS</span></span>

### <span data-ttu-id="309d7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="309d7-112">-DefaultProfile</span></span>
<span data-ttu-id="309d7-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="309d7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="309d7-114">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="309d7-114">-Description</span></span>
<span data-ttu-id="309d7-115">Stringa dettagliata che consente agli utenti di comprendere il significato di questa valutazione e il modo in cui è stato calcolato.</span><span class="sxs-lookup"><span data-stu-id="309d7-115">Detailed string that will help users to understand the meaning of this assessment and how it was calculated.</span></span>

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

### <span data-ttu-id="309d7-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="309d7-116">-DisplayName</span></span>
<span data-ttu-id="309d7-117">Titolo leggibile per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="309d7-117">Human readable title for this object.</span></span>

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

### <span data-ttu-id="309d7-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="309d7-118">-Name</span></span>
<span data-ttu-id="309d7-119">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="309d7-119">Resource name.</span></span>

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

### <span data-ttu-id="309d7-120">-RemediationDescription</span><span class="sxs-lookup"><span data-stu-id="309d7-120">-RemediationDescription</span></span>
<span data-ttu-id="309d7-121">Stringa dettagliata che consente agli utenti di comprendere i diversi modi per attenuare o correggere il problema di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="309d7-121">Detailed string that will help users to understand the different ways to mitigate or fix the security issue.</span></span>

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

### <span data-ttu-id="309d7-122">-Gravità</span><span class="sxs-lookup"><span data-stu-id="309d7-122">-Severity</span></span>
<span data-ttu-id="309d7-123">Indica l'importanza del rischio di sicurezza se la valutazione non è sana.</span><span class="sxs-lookup"><span data-stu-id="309d7-123">Indicates the importance of the security risk if the assessment is unhealthy.</span></span>

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

### <span data-ttu-id="309d7-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="309d7-124">-Confirm</span></span>
<span data-ttu-id="309d7-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="309d7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="309d7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="309d7-126">-WhatIf</span></span>
<span data-ttu-id="309d7-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="309d7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="309d7-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="309d7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="309d7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="309d7-129">CommonParameters</span></span>
<span data-ttu-id="309d7-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="309d7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="309d7-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="309d7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="309d7-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="309d7-132">INPUTS</span></span>

### <span data-ttu-id="309d7-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="309d7-133">None</span></span>

## <span data-ttu-id="309d7-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="309d7-134">OUTPUTS</span></span>

### <span data-ttu-id="309d7-135">Microsoft. Azure. Commands. Security. Models. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="309d7-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="309d7-136">Note</span><span class="sxs-lookup"><span data-stu-id="309d7-136">NOTES</span></span>

## <span data-ttu-id="309d7-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="309d7-137">RELATED LINKS</span></span>

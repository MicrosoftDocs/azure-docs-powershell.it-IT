---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: b13f09085b571d28f93a55bec5250d6bfa180306
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208282"
---
# <span data-ttu-id="169b4-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="169b4-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="169b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="169b4-102">SYNOPSIS</span></span>
<span data-ttu-id="169b4-103">Elimina i metadati della valutazione della sicurezza da una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="169b4-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="169b4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="169b4-104">SYNTAX</span></span>

### <span data-ttu-id="169b4-105">SubscriptionLevelResource (Default)</span><span class="sxs-lookup"><span data-stu-id="169b4-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="169b4-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="169b4-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="169b4-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="169b4-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="169b4-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="169b4-108">DESCRIPTION</span></span>
<span data-ttu-id="169b4-109">Elimina i metadati della valutazione della sicurezza da una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="169b4-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="169b4-110">Questa azione eliminerà il tipo di valutazione e tutti i risultati della valutazione pertinenti dalla sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="169b4-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="169b4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="169b4-111">EXAMPLES</span></span>

### <span data-ttu-id="169b4-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="169b4-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="169b4-113">Elimina un tipo di valutazione da una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="169b4-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="169b4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="169b4-114">PARAMETERS</span></span>

### <span data-ttu-id="169b4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="169b4-115">-DefaultProfile</span></span>
<span data-ttu-id="169b4-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="169b4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="169b4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="169b4-117">-InputObject</span></span>
<span data-ttu-id="169b4-118">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="169b4-118">Input Object.</span></span>

```yaml
Type: PSSecurityAssessmentMetadata
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="169b4-119">-Name</span><span class="sxs-lookup"><span data-stu-id="169b4-119">-Name</span></span>
<span data-ttu-id="169b4-120">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="169b4-120">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="169b4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="169b4-121">-PassThru</span></span>
<span data-ttu-id="169b4-122">Restituisce se l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="169b4-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="169b4-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="169b4-123">-ResourceId</span></span>
<span data-ttu-id="169b4-124">ID della risorsa di sicurezza su cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="169b4-124">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="169b4-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="169b4-125">-Confirm</span></span>
<span data-ttu-id="169b4-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="169b4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="169b4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="169b4-127">-WhatIf</span></span>
<span data-ttu-id="169b4-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="169b4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="169b4-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="169b4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="169b4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="169b4-130">CommonParameters</span></span>
<span data-ttu-id="169b4-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="169b4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="169b4-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="169b4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="169b4-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="169b4-133">INPUTS</span></span>

### <span data-ttu-id="169b4-134">System.String</span><span class="sxs-lookup"><span data-stu-id="169b4-134">System.String</span></span>

### <span data-ttu-id="169b4-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="169b4-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="169b4-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="169b4-136">OUTPUTS</span></span>

### <span data-ttu-id="169b4-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="169b4-137">System.Boolean</span></span>

## <span data-ttu-id="169b4-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="169b4-138">NOTES</span></span>

## <span data-ttu-id="169b4-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="169b4-139">RELATED LINKS</span></span>

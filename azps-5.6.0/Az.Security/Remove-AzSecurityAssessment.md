---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: ff69cd6296dbd95f959beb48fef6e496866e54f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011693"
---
# <span data-ttu-id="d74b0-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="d74b0-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="d74b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d74b0-102">SYNOPSIS</span></span>
<span data-ttu-id="d74b0-103">Elimina un risultato della valutazione della sicurezza da una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="d74b0-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="d74b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d74b0-104">SYNTAX</span></span>

### <span data-ttu-id="d74b0-105">SubscriptionLevelResource (Default)</span><span class="sxs-lookup"><span data-stu-id="d74b0-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d74b0-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="d74b0-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d74b0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d74b0-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d74b0-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="d74b0-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d74b0-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d74b0-109">DESCRIPTION</span></span>
<span data-ttu-id="d74b0-110">Elimina un risultato della valutazione della sicurezza da una sottoscrizione, in genere usato quando viene eliminata una risorsa o quando la valutazione non è più rilevante per una risorsa specifica</span><span class="sxs-lookup"><span data-stu-id="d74b0-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="d74b0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d74b0-111">EXAMPLES</span></span>

### <span data-ttu-id="d74b0-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d74b0-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="d74b0-113">Elimina un risultato della valutazione in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="d74b0-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="d74b0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d74b0-114">PARAMETERS</span></span>

### <span data-ttu-id="d74b0-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="d74b0-115">-AssessedResourceId</span></span>
<span data-ttu-id="d74b0-116">ID risorsa completo della risorsa su cui viene calcolata la valutazione.</span><span class="sxs-lookup"><span data-stu-id="d74b0-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d74b0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d74b0-117">-DefaultProfile</span></span>
<span data-ttu-id="d74b0-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d74b0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d74b0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d74b0-119">-InputObject</span></span>
<span data-ttu-id="d74b0-120">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="d74b0-120">Input Object.</span></span>

```yaml
Type: PSSecurityAssessment
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d74b0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d74b0-121">-Name</span></span>
<span data-ttu-id="d74b0-122">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d74b0-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d74b0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d74b0-123">-PassThru</span></span>
<span data-ttu-id="d74b0-124">Restituisce se l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="d74b0-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="d74b0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d74b0-125">-ResourceId</span></span>
<span data-ttu-id="d74b0-126">ID della risorsa di sicurezza su cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="d74b0-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="d74b0-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d74b0-127">-Confirm</span></span>
<span data-ttu-id="d74b0-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d74b0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d74b0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d74b0-129">-WhatIf</span></span>
<span data-ttu-id="d74b0-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d74b0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d74b0-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d74b0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d74b0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d74b0-132">CommonParameters</span></span>
<span data-ttu-id="d74b0-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d74b0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d74b0-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d74b0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d74b0-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="d74b0-135">INPUTS</span></span>

### <span data-ttu-id="d74b0-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d74b0-136">System.String</span></span>

### <span data-ttu-id="d74b0-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="d74b0-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="d74b0-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d74b0-138">OUTPUTS</span></span>

### <span data-ttu-id="d74b0-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d74b0-139">System.Boolean</span></span>

## <span data-ttu-id="d74b0-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="d74b0-140">NOTES</span></span>

## <span data-ttu-id="d74b0-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d74b0-141">RELATED LINKS</span></span>

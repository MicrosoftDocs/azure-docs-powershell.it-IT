---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: d24a2a5ef6017942815f1a652e1c769523815b7f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208283"
---
# <span data-ttu-id="8efc3-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="8efc3-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="8efc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8efc3-102">SYNOPSIS</span></span>
<span data-ttu-id="8efc3-103">Elimina un risultato della valutazione della sicurezza da una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8efc3-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="8efc3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8efc3-104">SYNTAX</span></span>

### <span data-ttu-id="8efc3-105">SubscriptionLevelResource (Default)</span><span class="sxs-lookup"><span data-stu-id="8efc3-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8efc3-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="8efc3-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8efc3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8efc3-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8efc3-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="8efc3-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8efc3-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8efc3-109">DESCRIPTION</span></span>
<span data-ttu-id="8efc3-110">Elimina un risultato della valutazione della sicurezza da una sottoscrizione, in genere usato quando viene eliminata una risorsa o quando la valutazione non è più rilevante per una risorsa specifica</span><span class="sxs-lookup"><span data-stu-id="8efc3-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="8efc3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8efc3-111">EXAMPLES</span></span>

### <span data-ttu-id="8efc3-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8efc3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="8efc3-113">Elimina un risultato della valutazione in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="8efc3-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="8efc3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8efc3-114">PARAMETERS</span></span>

### <span data-ttu-id="8efc3-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="8efc3-115">-AssessedResourceId</span></span>
<span data-ttu-id="8efc3-116">ID risorsa completo della risorsa su cui viene calcolata la valutazione.</span><span class="sxs-lookup"><span data-stu-id="8efc3-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="8efc3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8efc3-117">-DefaultProfile</span></span>
<span data-ttu-id="8efc3-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8efc3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8efc3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8efc3-119">-InputObject</span></span>
<span data-ttu-id="8efc3-120">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="8efc3-120">Input Object.</span></span>

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

### <span data-ttu-id="8efc3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8efc3-121">-Name</span></span>
<span data-ttu-id="8efc3-122">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8efc3-122">Resource name.</span></span>

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

### <span data-ttu-id="8efc3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8efc3-123">-PassThru</span></span>
<span data-ttu-id="8efc3-124">Restituisce se l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="8efc3-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="8efc3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8efc3-125">-ResourceId</span></span>
<span data-ttu-id="8efc3-126">ID della risorsa di sicurezza su cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="8efc3-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="8efc3-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8efc3-127">-Confirm</span></span>
<span data-ttu-id="8efc3-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8efc3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8efc3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8efc3-129">-WhatIf</span></span>
<span data-ttu-id="8efc3-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8efc3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8efc3-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8efc3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8efc3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8efc3-132">CommonParameters</span></span>
<span data-ttu-id="8efc3-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8efc3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8efc3-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8efc3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8efc3-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="8efc3-135">INPUTS</span></span>

### <span data-ttu-id="8efc3-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8efc3-136">System.String</span></span>

### <span data-ttu-id="8efc3-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="8efc3-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="8efc3-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8efc3-138">OUTPUTS</span></span>

### <span data-ttu-id="8efc3-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8efc3-139">System.Boolean</span></span>

## <span data-ttu-id="8efc3-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="8efc3-140">NOTES</span></span>

## <span data-ttu-id="8efc3-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8efc3-141">RELATED LINKS</span></span>

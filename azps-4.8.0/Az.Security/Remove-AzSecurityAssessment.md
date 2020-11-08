---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: d24a2a5ef6017942815f1a652e1c769523815b7f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191928"
---
# <span data-ttu-id="fd814-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="fd814-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="fd814-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd814-102">SYNOPSIS</span></span>
<span data-ttu-id="fd814-103">Elimina un risultato di valutazione della sicurezza da un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fd814-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="fd814-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd814-104">SYNTAX</span></span>

### <span data-ttu-id="fd814-105">SubscriptionLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fd814-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd814-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="fd814-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd814-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd814-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd814-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="fd814-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd814-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd814-109">DESCRIPTION</span></span>
<span data-ttu-id="fd814-110">Elimina un risultato della valutazione di sicurezza da un abbonamento, in genere usato quando viene eliminato un resoruce o quando la valutazione non è più pertinente per una risorsa specifica</span><span class="sxs-lookup"><span data-stu-id="fd814-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="fd814-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd814-111">EXAMPLES</span></span>

### <span data-ttu-id="fd814-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fd814-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="fd814-113">Elimina un risultato di valutazione in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="fd814-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="fd814-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd814-114">PARAMETERS</span></span>

### <span data-ttu-id="fd814-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="fd814-115">-AssessedResourceId</span></span>
<span data-ttu-id="fd814-116">ID risorsa completa della risorsa a cui viene calcolata la valutazione.</span><span class="sxs-lookup"><span data-stu-id="fd814-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="fd814-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd814-117">-DefaultProfile</span></span>
<span data-ttu-id="fd814-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fd814-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd814-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd814-119">-InputObject</span></span>
<span data-ttu-id="fd814-120">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="fd814-120">Input Object.</span></span>

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

### <span data-ttu-id="fd814-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd814-121">-Name</span></span>
<span data-ttu-id="fd814-122">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="fd814-122">Resource name.</span></span>

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

### <span data-ttu-id="fd814-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd814-123">-PassThru</span></span>
<span data-ttu-id="fd814-124">Restituirà se l'operazione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="fd814-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="fd814-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd814-125">-ResourceId</span></span>
<span data-ttu-id="fd814-126">ID della risorsa di sicurezza a cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="fd814-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="fd814-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fd814-127">-Confirm</span></span>
<span data-ttu-id="fd814-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd814-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd814-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd814-129">-WhatIf</span></span>
<span data-ttu-id="fd814-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd814-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd814-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd814-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd814-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd814-132">CommonParameters</span></span>
<span data-ttu-id="fd814-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd814-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd814-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd814-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd814-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd814-135">INPUTS</span></span>

### <span data-ttu-id="fd814-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fd814-136">System.String</span></span>

### <span data-ttu-id="fd814-137">Microsoft. Azure. Commands. Security. Models. assessments. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="fd814-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="fd814-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd814-138">OUTPUTS</span></span>

### <span data-ttu-id="fd814-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd814-139">System.Boolean</span></span>

## <span data-ttu-id="fd814-140">Note</span><span class="sxs-lookup"><span data-stu-id="fd814-140">NOTES</span></span>

## <span data-ttu-id="fd814-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd814-141">RELATED LINKS</span></span>

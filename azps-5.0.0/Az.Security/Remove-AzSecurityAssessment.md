---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessment.md
ms.openlocfilehash: d24a2a5ef6017942815f1a652e1c769523815b7f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200191"
---
# <span data-ttu-id="5c539-101">Remove-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="5c539-101">Remove-AzSecurityAssessment</span></span>

## <span data-ttu-id="5c539-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5c539-102">SYNOPSIS</span></span>
<span data-ttu-id="5c539-103">Elimina un risultato di valutazione della sicurezza da un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5c539-103">Deletes a security assessment result from a subscription.</span></span>

## <span data-ttu-id="5c539-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c539-104">SYNTAX</span></span>

### <span data-ttu-id="5c539-105">SubscriptionLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5c539-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c539-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="5c539-106">ResourceIdLevelResource</span></span>
```
Remove-AzSecurityAssessment -Name <String> [-AssessedResourceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c539-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c539-107">ResourceId</span></span>
```
Remove-AzSecurityAssessment -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c539-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="5c539-108">InputObject</span></span>
```
Remove-AzSecurityAssessment -InputObject <PSSecurityAssessment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c539-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c539-109">DESCRIPTION</span></span>
<span data-ttu-id="5c539-110">Elimina un risultato della valutazione di sicurezza da un abbonamento, in genere usato quando viene eliminato un resoruce o quando la valutazione non è più pertinente per una risorsa specifica</span><span class="sxs-lookup"><span data-stu-id="5c539-110">Deletes a security assessment result from a subscription, usually used when a resoruce is deleted or when the assessment is not relevant for a specific resource anymore</span></span>

## <span data-ttu-id="5c539-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c539-111">EXAMPLES</span></span>

### <span data-ttu-id="5c539-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5c539-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="5c539-113">Elimina un risultato di valutazione in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="5c539-113">Deletes an assessment result on a subscription</span></span>

## <span data-ttu-id="5c539-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5c539-114">PARAMETERS</span></span>

### <span data-ttu-id="5c539-115">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="5c539-115">-AssessedResourceId</span></span>
<span data-ttu-id="5c539-116">ID risorsa completa della risorsa a cui viene calcolata la valutazione.</span><span class="sxs-lookup"><span data-stu-id="5c539-116">Full resource ID of the resource that the assessment is calculated on.</span></span>

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

### <span data-ttu-id="5c539-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c539-117">-DefaultProfile</span></span>
<span data-ttu-id="5c539-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5c539-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c539-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c539-119">-InputObject</span></span>
<span data-ttu-id="5c539-120">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="5c539-120">Input Object.</span></span>

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

### <span data-ttu-id="5c539-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c539-121">-Name</span></span>
<span data-ttu-id="5c539-122">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="5c539-122">Resource name.</span></span>

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

### <span data-ttu-id="5c539-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c539-123">-PassThru</span></span>
<span data-ttu-id="5c539-124">Restituirà se l'operazione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="5c539-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="5c539-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c539-125">-ResourceId</span></span>
<span data-ttu-id="5c539-126">ID della risorsa di sicurezza a cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="5c539-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="5c539-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5c539-127">-Confirm</span></span>
<span data-ttu-id="5c539-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c539-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c539-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c539-129">-WhatIf</span></span>
<span data-ttu-id="5c539-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c539-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c539-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c539-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c539-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c539-132">CommonParameters</span></span>
<span data-ttu-id="5c539-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c539-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c539-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c539-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c539-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5c539-135">INPUTS</span></span>

### <span data-ttu-id="5c539-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5c539-136">System.String</span></span>

### <span data-ttu-id="5c539-137">Microsoft. Azure. Commands. Security. Models. assessments. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="5c539-137">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="5c539-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c539-138">OUTPUTS</span></span>

### <span data-ttu-id="5c539-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5c539-139">System.Boolean</span></span>

## <span data-ttu-id="5c539-140">Note</span><span class="sxs-lookup"><span data-stu-id="5c539-140">NOTES</span></span>

## <span data-ttu-id="5c539-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c539-141">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: b13f09085b571d28f93a55bec5250d6bfa180306
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200190"
---
# <span data-ttu-id="976b5-101">Remove-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="976b5-101">Remove-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="976b5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="976b5-102">SYNOPSIS</span></span>
<span data-ttu-id="976b5-103">Elimina i metadati di una valutazione della sicurezza da un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="976b5-103">Deletes a security assessment metadata from a subscription.</span></span>

## <span data-ttu-id="976b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="976b5-104">SYNTAX</span></span>

### <span data-ttu-id="976b5-105">SubscriptionLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="976b5-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityAssessmentMetadata -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="976b5-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="976b5-106">ResourceId</span></span>
```
Remove-AzSecurityAssessmentMetadata -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="976b5-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="976b5-107">InputObject</span></span>
```
Remove-AzSecurityAssessmentMetadata -InputObject <PSSecurityAssessmentMetadata> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="976b5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="976b5-108">DESCRIPTION</span></span>
<span data-ttu-id="976b5-109">Elimina i metadati di una valutazione della sicurezza da un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="976b5-109">Deletes a security assessment metadata from a subscription.</span></span> <span data-ttu-id="976b5-110">Questa azione eliminerà il tipo di valutazione e tutti i risultati di valutazione rilevanti dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="976b5-110">This action will delete the assessment type and all the relevant assessment results from the subscription.</span></span>

## <span data-ttu-id="976b5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="976b5-111">EXAMPLES</span></span>

### <span data-ttu-id="976b5-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="976b5-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityAssessmentMetadata -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D
```

<span data-ttu-id="976b5-113">Elimina un tipo di valutazione da un abbonamento</span><span class="sxs-lookup"><span data-stu-id="976b5-113">Deletes an assessment type from a subscription</span></span>

## <span data-ttu-id="976b5-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="976b5-114">PARAMETERS</span></span>

### <span data-ttu-id="976b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="976b5-115">-DefaultProfile</span></span>
<span data-ttu-id="976b5-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="976b5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="976b5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="976b5-117">-InputObject</span></span>
<span data-ttu-id="976b5-118">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="976b5-118">Input Object.</span></span>

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

### <span data-ttu-id="976b5-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="976b5-119">-Name</span></span>
<span data-ttu-id="976b5-120">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="976b5-120">Resource name.</span></span>

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

### <span data-ttu-id="976b5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="976b5-121">-PassThru</span></span>
<span data-ttu-id="976b5-122">Restituirà se l'operazione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="976b5-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="976b5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="976b5-123">-ResourceId</span></span>
<span data-ttu-id="976b5-124">ID della risorsa di sicurezza a cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="976b5-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="976b5-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="976b5-125">-Confirm</span></span>
<span data-ttu-id="976b5-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="976b5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="976b5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="976b5-127">-WhatIf</span></span>
<span data-ttu-id="976b5-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="976b5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="976b5-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="976b5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="976b5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="976b5-130">CommonParameters</span></span>
<span data-ttu-id="976b5-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="976b5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="976b5-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="976b5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="976b5-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="976b5-133">INPUTS</span></span>

### <span data-ttu-id="976b5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="976b5-134">System.String</span></span>

### <span data-ttu-id="976b5-135">Microsoft. Azure. Commands. Security. Models. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="976b5-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="976b5-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="976b5-136">OUTPUTS</span></span>

### <span data-ttu-id="976b5-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="976b5-137">System.Boolean</span></span>

## <span data-ttu-id="976b5-138">Note</span><span class="sxs-lookup"><span data-stu-id="976b5-138">NOTES</span></span>

## <span data-ttu-id="976b5-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="976b5-139">RELATED LINKS</span></span>

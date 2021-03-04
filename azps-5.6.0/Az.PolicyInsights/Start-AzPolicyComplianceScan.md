---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: db51cfdf499fcf3d6c81f47d977978a6ff4bf8cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989070"
---
# <span data-ttu-id="30f70-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="30f70-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="30f70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30f70-102">SYNOPSIS</span></span>
<span data-ttu-id="30f70-103">Attiva una valutazione di conformità dei criteri per tutte le risorse in una sottoscrizione o un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="30f70-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="30f70-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30f70-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30f70-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="30f70-105">DESCRIPTION</span></span>
<span data-ttu-id="30f70-106">Il cmdlet **Start-AzPolicyComplianceScan avvia** una valutazione di conformità dei criteri per una sottoscrizione o un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="30f70-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="30f70-107">Lo stato di conformità di tutte le risorse all'interno di tale ambito verrà valutato rispetto a tutti i criteri assegnati.</span><span class="sxs-lookup"><span data-stu-id="30f70-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="30f70-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30f70-108">EXAMPLES</span></span>

### <span data-ttu-id="30f70-109">Esempio 1: Avviare un'analisi di conformità nell'ambito della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="30f70-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="30f70-110">Questo comando avvia una valutazione di conformità dei criteri per la sottoscrizione attiva.</span><span class="sxs-lookup"><span data-stu-id="30f70-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="30f70-111">Esempio 2: Avviare un'analisi di conformità nell'ambito del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="30f70-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="30f70-112">Questo comando avvia una valutazione di conformità dei criteri per il gruppo di risorse "myRG" nella sottoscrizione attiva.</span><span class="sxs-lookup"><span data-stu-id="30f70-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="30f70-113">Esempio 3: Avviare un'analisi di conformità e attendere il completamento in background</span><span class="sxs-lookup"><span data-stu-id="30f70-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan -AsJob
PS C:\> $job | Wait-Job
```

<span data-ttu-id="30f70-114">Questo comando avvia una valutazione di conformità dei criteri per la sottoscrizione attiva.</span><span class="sxs-lookup"><span data-stu-id="30f70-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="30f70-115">Attenderà il completamento dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="30f70-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="30f70-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30f70-116">PARAMETERS</span></span>

### <span data-ttu-id="30f70-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30f70-117">-AsJob</span></span>
<span data-ttu-id="30f70-118">Eseguire il cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="30f70-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="30f70-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30f70-119">-DefaultProfile</span></span>
<span data-ttu-id="30f70-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30f70-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30f70-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="30f70-121">-PassThru</span></span>
<span data-ttu-id="30f70-122">Restituisce True se il comando viene completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="30f70-122">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="30f70-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30f70-123">-ResourceGroupName</span></span>
<span data-ttu-id="30f70-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="30f70-124">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30f70-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30f70-125">-Confirm</span></span>
<span data-ttu-id="30f70-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30f70-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30f70-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30f70-127">-WhatIf</span></span>
<span data-ttu-id="30f70-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30f70-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30f70-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30f70-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30f70-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30f70-130">CommonParameters</span></span>
<span data-ttu-id="30f70-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30f70-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30f70-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="30f70-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30f70-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="30f70-133">INPUTS</span></span>

### <span data-ttu-id="30f70-134">System.String</span><span class="sxs-lookup"><span data-stu-id="30f70-134">System.String</span></span>

## <span data-ttu-id="30f70-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30f70-135">OUTPUTS</span></span>

### <span data-ttu-id="30f70-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="30f70-136">System.Boolean</span></span>

## <span data-ttu-id="30f70-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="30f70-137">NOTES</span></span>

## <span data-ttu-id="30f70-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30f70-138">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: 61022603ad34c345274328d47767e90580e54d6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206258"
---
# <span data-ttu-id="22cb1-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="22cb1-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="22cb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="22cb1-103">Attiva una valutazione di conformità dei criteri per tutte le risorse in una sottoscrizione o un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="22cb1-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="22cb1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22cb1-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22cb1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="22cb1-105">DESCRIPTION</span></span>
<span data-ttu-id="22cb1-106">Il cmdlet **Start-AzPolicyComplianceScan avvia** una valutazione di conformità dei criteri per una sottoscrizione o un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="22cb1-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="22cb1-107">Lo stato di conformità di tutte le risorse all'interno di tale ambito verrà valutato rispetto a tutti i criteri assegnati.</span><span class="sxs-lookup"><span data-stu-id="22cb1-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="22cb1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22cb1-108">EXAMPLES</span></span>

### <span data-ttu-id="22cb1-109">Esempio 1: Avviare un'analisi di conformità nell'ambito della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="22cb1-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="22cb1-110">Questo comando avvia una valutazione di conformità dei criteri per la sottoscrizione attiva.</span><span class="sxs-lookup"><span data-stu-id="22cb1-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="22cb1-111">Esempio 2: Avviare un'analisi di conformità nell'ambito del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="22cb1-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="22cb1-112">Questo comando avvia una valutazione di conformità dei criteri per il gruppo di risorse "myRG" nella sottoscrizione attiva.</span><span class="sxs-lookup"><span data-stu-id="22cb1-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="22cb1-113">Esempio 3: Avviare un'analisi di conformità e attendere il completamento in background</span><span class="sxs-lookup"><span data-stu-id="22cb1-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan -AsJob
PS C:\> $job | Wait-Job
```

<span data-ttu-id="22cb1-114">Questo comando avvia una valutazione di conformità dei criteri per la sottoscrizione attiva.</span><span class="sxs-lookup"><span data-stu-id="22cb1-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="22cb1-115">Attenderà il completamento dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="22cb1-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="22cb1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22cb1-116">PARAMETERS</span></span>

### <span data-ttu-id="22cb1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22cb1-117">-AsJob</span></span>
<span data-ttu-id="22cb1-118">Eseguire il cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="22cb1-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="22cb1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22cb1-119">-DefaultProfile</span></span>
<span data-ttu-id="22cb1-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22cb1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22cb1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22cb1-121">-PassThru</span></span>
<span data-ttu-id="22cb1-122">Restituisce True se il comando viene completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="22cb1-122">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="22cb1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22cb1-123">-ResourceGroupName</span></span>
<span data-ttu-id="22cb1-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="22cb1-124">Resource group name.</span></span>

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

### <span data-ttu-id="22cb1-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22cb1-125">-Confirm</span></span>
<span data-ttu-id="22cb1-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22cb1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22cb1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22cb1-127">-WhatIf</span></span>
<span data-ttu-id="22cb1-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22cb1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22cb1-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22cb1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22cb1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22cb1-130">CommonParameters</span></span>
<span data-ttu-id="22cb1-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22cb1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22cb1-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="22cb1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22cb1-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="22cb1-133">INPUTS</span></span>

### <span data-ttu-id="22cb1-134">System.String</span><span class="sxs-lookup"><span data-stu-id="22cb1-134">System.String</span></span>

## <span data-ttu-id="22cb1-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22cb1-135">OUTPUTS</span></span>

### <span data-ttu-id="22cb1-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="22cb1-136">System.Boolean</span></span>

## <span data-ttu-id="22cb1-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="22cb1-137">NOTES</span></span>

## <span data-ttu-id="22cb1-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22cb1-138">RELATED LINKS</span></span>

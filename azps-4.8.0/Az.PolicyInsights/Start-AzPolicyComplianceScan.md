---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: 61022603ad34c345274328d47767e90580e54d6b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192671"
---
# <span data-ttu-id="fe696-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="fe696-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="fe696-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe696-102">SYNOPSIS</span></span>
<span data-ttu-id="fe696-103">Attiva una valutazione della conformità dei criteri per tutte le risorse in un gruppo di abbonamenti o risorse.</span><span class="sxs-lookup"><span data-stu-id="fe696-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="fe696-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe696-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe696-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe696-105">DESCRIPTION</span></span>
<span data-ttu-id="fe696-106">Il cmdlet **Start-AzPolicyComplianceScan** avvia una valutazione della conformità dei criteri per un gruppo di abbonamenti o risorse.</span><span class="sxs-lookup"><span data-stu-id="fe696-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="fe696-107">Tutte le risorse in tale ambito avranno lo stato di conformità valutato in base a tutti i criteri assegnati.</span><span class="sxs-lookup"><span data-stu-id="fe696-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="fe696-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe696-108">EXAMPLES</span></span>

### <span data-ttu-id="fe696-109">Esempio 1: avviare un'analisi della conformità all'ambito dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="fe696-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="fe696-110">Questo comando avvia una valutazione della conformità dei criteri per l'abbonamento attivo.</span><span class="sxs-lookup"><span data-stu-id="fe696-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="fe696-111">Esempio 2: avviare un'analisi della conformità nell'ambito di un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fe696-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="fe696-112">Questo comando avvia una valutazione della conformità dei criteri per il gruppo di risorse "myRG" nell'abbonamento attivo.</span><span class="sxs-lookup"><span data-stu-id="fe696-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="fe696-113">Esempio 3: avviare un'analisi di conformità e attendere che venga completata in background</span><span class="sxs-lookup"><span data-stu-id="fe696-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan -AsJob
PS C:\> $job | Wait-Job
```

<span data-ttu-id="fe696-114">Questo comando avvia una valutazione della conformità dei criteri per l'abbonamento attivo.</span><span class="sxs-lookup"><span data-stu-id="fe696-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="fe696-115">Aspetterà che l'analisi venga completata.</span><span class="sxs-lookup"><span data-stu-id="fe696-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="fe696-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe696-116">PARAMETERS</span></span>

### <span data-ttu-id="fe696-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe696-117">-AsJob</span></span>
<span data-ttu-id="fe696-118">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="fe696-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="fe696-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe696-119">-DefaultProfile</span></span>
<span data-ttu-id="fe696-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fe696-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe696-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe696-121">-PassThru</span></span>
<span data-ttu-id="fe696-122">Restituisce vero se il comando viene completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="fe696-122">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="fe696-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe696-123">-ResourceGroupName</span></span>
<span data-ttu-id="fe696-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fe696-124">Resource group name.</span></span>

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

### <span data-ttu-id="fe696-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fe696-125">-Confirm</span></span>
<span data-ttu-id="fe696-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe696-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe696-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe696-127">-WhatIf</span></span>
<span data-ttu-id="fe696-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe696-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe696-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe696-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe696-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe696-130">CommonParameters</span></span>
<span data-ttu-id="fe696-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe696-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe696-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe696-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe696-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe696-133">INPUTS</span></span>

### <span data-ttu-id="fe696-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fe696-134">System.String</span></span>

## <span data-ttu-id="fe696-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe696-135">OUTPUTS</span></span>

### <span data-ttu-id="fe696-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fe696-136">System.Boolean</span></span>

## <span data-ttu-id="fe696-137">Note</span><span class="sxs-lookup"><span data-stu-id="fe696-137">NOTES</span></span>

## <span data-ttu-id="fe696-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe696-138">RELATED LINKS</span></span>
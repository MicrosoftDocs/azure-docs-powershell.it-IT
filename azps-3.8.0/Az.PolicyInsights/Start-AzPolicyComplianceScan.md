---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: cd173d17b0867fb5c635b77ee6c72847dc845cb7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020929"
---
# <span data-ttu-id="9e218-101">Start-AzPolicyComplianceScan</span><span class="sxs-lookup"><span data-stu-id="9e218-101">Start-AzPolicyComplianceScan</span></span>

## <span data-ttu-id="9e218-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e218-102">SYNOPSIS</span></span>
<span data-ttu-id="9e218-103">Attiva una valutazione della conformità dei criteri per tutte le risorse in un gruppo di abbonamenti o risorse.</span><span class="sxs-lookup"><span data-stu-id="9e218-103">Triggers a policy compliance evaluation for all resources in a subscription or resource group.</span></span>

## <span data-ttu-id="9e218-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e218-104">SYNTAX</span></span>

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e218-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e218-105">DESCRIPTION</span></span>
<span data-ttu-id="9e218-106">Il cmdlet **Start-AzPolicyComplianceScan** avvia una valutazione della conformità dei criteri per un gruppo di abbonamenti o risorse.</span><span class="sxs-lookup"><span data-stu-id="9e218-106">The **Start-AzPolicyComplianceScan** cmdlet starts a policy compliance evaluation for a subscription or resource group.</span></span> <span data-ttu-id="9e218-107">Tutte le risorse in tale ambito avranno lo stato di conformità valutato in base a tutti i criteri assegnati.</span><span class="sxs-lookup"><span data-stu-id="9e218-107">All resources within that scope will have their compliance state evaluated against all assigned policies.</span></span>

## <span data-ttu-id="9e218-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e218-108">EXAMPLES</span></span>

### <span data-ttu-id="9e218-109">Esempio 1: avviare un'analisi della conformità all'ambito dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="9e218-109">Example 1: Start a compliance scan at subscription scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan
```

<span data-ttu-id="9e218-110">Questo comando avvia una valutazione della conformità dei criteri per l'abbonamento attivo.</span><span class="sxs-lookup"><span data-stu-id="9e218-110">This command starts a policy compliance evaluation for the active subscription.</span></span>

### <span data-ttu-id="9e218-111">Esempio 2: avviare un'analisi della conformità nell'ambito di un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="9e218-111">Example 2: Start a compliance scan at resource group scope</span></span>
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

<span data-ttu-id="9e218-112">Questo comando avvia una valutazione della conformità dei criteri per il gruppo di risorse "myRG" nell'abbonamento attivo.</span><span class="sxs-lookup"><span data-stu-id="9e218-112">This command starts a policy compliance evaluation for the "myRG" resource group in the active subscription.</span></span>

### <span data-ttu-id="9e218-113">Esempio 3: avviare un'analisi di conformità e attendere che venga completata in background</span><span class="sxs-lookup"><span data-stu-id="9e218-113">Example 3: Start a compliance scan and wait for it to complete in the background</span></span>
```
PS C:\> $job = Start-AzPolicyComplianceScan
PS C:\> $job | Wait-Job
```

<span data-ttu-id="9e218-114">Questo comando avvia una valutazione della conformità dei criteri per l'abbonamento attivo.</span><span class="sxs-lookup"><span data-stu-id="9e218-114">This command starts a policy compliance evaluation for the active subscription.</span></span> <span data-ttu-id="9e218-115">Aspetterà che l'analisi venga completata.</span><span class="sxs-lookup"><span data-stu-id="9e218-115">It will wait for the scan to complete.</span></span>

## <span data-ttu-id="9e218-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e218-116">PARAMETERS</span></span>

### <span data-ttu-id="9e218-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e218-117">-AsJob</span></span>
<span data-ttu-id="9e218-118">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="9e218-118">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="9e218-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e218-119">-DefaultProfile</span></span>
<span data-ttu-id="9e218-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e218-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e218-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e218-121">-PassThru</span></span>
<span data-ttu-id="9e218-122">Restituisce vero se il comando viene completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="9e218-122">Return True if the command completes successfully.</span></span>

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

### <span data-ttu-id="9e218-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e218-123">-ResourceGroupName</span></span>
<span data-ttu-id="9e218-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9e218-124">Resource group name.</span></span>

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

### <span data-ttu-id="9e218-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9e218-125">-Confirm</span></span>
<span data-ttu-id="9e218-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e218-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e218-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e218-127">-WhatIf</span></span>
<span data-ttu-id="9e218-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e218-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e218-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e218-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e218-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e218-130">CommonParameters</span></span>
<span data-ttu-id="9e218-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e218-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e218-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e218-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e218-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e218-133">INPUTS</span></span>

### <span data-ttu-id="9e218-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9e218-134">System.String</span></span>

## <span data-ttu-id="9e218-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e218-135">OUTPUTS</span></span>

### <span data-ttu-id="9e218-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9e218-136">System.Boolean</span></span>

## <span data-ttu-id="9e218-137">Note</span><span class="sxs-lookup"><span data-stu-id="9e218-137">NOTES</span></span>

## <span data-ttu-id="9e218-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e218-138">RELATED LINKS</span></span>

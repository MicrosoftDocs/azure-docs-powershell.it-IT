---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/restore-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 01354106e3d6ad9fbe33c97f6bcd774c62be7ccf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337576"
---
# <span data-ttu-id="af23f-101">Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="af23f-101">Restore-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="af23f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af23f-102">SYNOPSIS</span></span>
<span data-ttu-id="af23f-103">Ripristinare un'area di lavoro eliminata.</span><span class="sxs-lookup"><span data-stu-id="af23f-103">Restore a deleted workspace.</span></span>

## <span data-ttu-id="af23f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af23f-104">SYNTAX</span></span>

```
Restore-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af23f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af23f-105">DESCRIPTION</span></span>
<span data-ttu-id="af23f-106">Ripristinare un'area di lavoro eliminata.</span><span class="sxs-lookup"><span data-stu-id="af23f-106">Restore a deleted workspace.</span></span>

## <span data-ttu-id="af23f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af23f-107">EXAMPLES</span></span>

### <span data-ttu-id="af23f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="af23f-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> $workspace = Restore-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
```

<span data-ttu-id="af23f-109">Ripristinare l'area di lavoro eliminata.</span><span class="sxs-lookup"><span data-stu-id="af23f-109">Restore deleted workspace.</span></span>

## <span data-ttu-id="af23f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af23f-110">PARAMETERS</span></span>

### <span data-ttu-id="af23f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af23f-111">-DefaultProfile</span></span>
<span data-ttu-id="af23f-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af23f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af23f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="af23f-113">-Force</span></span>
<span data-ttu-id="af23f-114">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="af23f-114">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af23f-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="af23f-115">-Location</span></span>
<span data-ttu-id="af23f-116">Area geografica in cui verrà creata l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="af23f-116">The geographic region that the workspace will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af23f-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="af23f-117">-Name</span></span>
<span data-ttu-id="af23f-118">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="af23f-118">The workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af23f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af23f-119">-ResourceGroupName</span></span>
<span data-ttu-id="af23f-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="af23f-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af23f-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="af23f-121">-Confirm</span></span>
<span data-ttu-id="af23f-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af23f-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af23f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af23f-123">-WhatIf</span></span>
<span data-ttu-id="af23f-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af23f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af23f-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af23f-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af23f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af23f-126">CommonParameters</span></span>
<span data-ttu-id="af23f-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af23f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af23f-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af23f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af23f-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af23f-129">INPUTS</span></span>

### <span data-ttu-id="af23f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="af23f-130">System.String</span></span>

## <span data-ttu-id="af23f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af23f-131">OUTPUTS</span></span>

### <span data-ttu-id="af23f-132">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="af23f-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="af23f-133">Note</span><span class="sxs-lookup"><span data-stu-id="af23f-133">NOTES</span></span>

## <span data-ttu-id="af23f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af23f-134">RELATED LINKS</span></span>

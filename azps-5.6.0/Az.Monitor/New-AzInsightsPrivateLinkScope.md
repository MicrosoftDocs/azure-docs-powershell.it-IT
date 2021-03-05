---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: ec9245c15a0c07da92874daa42c387e4109258c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984519"
---
# <span data-ttu-id="0565c-101">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="0565c-101">New-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="0565c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0565c-102">SYNOPSIS</span></span>
<span data-ttu-id="0565c-103">Creare un ambito di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="0565c-103">create private link scope</span></span>

## <span data-ttu-id="0565c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0565c-104">SYNTAX</span></span>

```
New-AzInsightsPrivateLinkScope -Location <String> -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0565c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0565c-105">DESCRIPTION</span></span>
<span data-ttu-id="0565c-106">Creare un ambito di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="0565c-106">create private link scope</span></span>

## <span data-ttu-id="0565c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0565c-107">EXAMPLES</span></span>

### <span data-ttu-id="0565c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0565c-108">Example 1</span></span>
```powershell
New-AzInsightsPrivateLinkScope -Location "eastus" -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="0565c-109">Creare un ambito di collegamento privato con il nome "scope_name" nel gruppo di risorse "rg_name" nella posizione "eastus"</span><span class="sxs-lookup"><span data-stu-id="0565c-109">create private link scope with name "scope_name" under resource group "rg_name" in location "eastus"</span></span>

## <span data-ttu-id="0565c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0565c-110">PARAMETERS</span></span>

### <span data-ttu-id="0565c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0565c-111">-DefaultProfile</span></span>
<span data-ttu-id="0565c-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0565c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0565c-113">-Location</span><span class="sxs-lookup"><span data-stu-id="0565c-113">-Location</span></span>
<span data-ttu-id="0565c-114">Posizione</span><span class="sxs-lookup"><span data-stu-id="0565c-114">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0565c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0565c-115">-Name</span></span>
<span data-ttu-id="0565c-116">Nome ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="0565c-116">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0565c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0565c-117">-ResourceGroupName</span></span>
<span data-ttu-id="0565c-118">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="0565c-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0565c-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="0565c-119">-Tags</span></span>
<span data-ttu-id="0565c-120">Tag</span><span class="sxs-lookup"><span data-stu-id="0565c-120">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0565c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0565c-121">-Confirm</span></span>
<span data-ttu-id="0565c-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0565c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0565c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0565c-123">-WhatIf</span></span>
<span data-ttu-id="0565c-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0565c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0565c-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0565c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0565c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0565c-126">CommonParameters</span></span>
<span data-ttu-id="0565c-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0565c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0565c-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0565c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0565c-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="0565c-129">INPUTS</span></span>

### <span data-ttu-id="0565c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0565c-130">System.String</span></span>

## <span data-ttu-id="0565c-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0565c-131">OUTPUTS</span></span>

### <span data-ttu-id="0565c-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="0565c-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="0565c-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="0565c-133">NOTES</span></span>

## <span data-ttu-id="0565c-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0565c-134">RELATED LINKS</span></span>

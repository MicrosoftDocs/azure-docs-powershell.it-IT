---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 198d52678bceccfd1045522881dc3a62fdebf752
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192386"
---
# <span data-ttu-id="f5c07-101">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f5c07-101">New-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="f5c07-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f5c07-102">SYNOPSIS</span></span>
<span data-ttu-id="f5c07-103">creare un ambito di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="f5c07-103">create private link scope</span></span>

## <span data-ttu-id="f5c07-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f5c07-104">SYNTAX</span></span>

```
New-AzInsightsPrivateLinkScope -Location <String> -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5c07-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5c07-105">DESCRIPTION</span></span>
<span data-ttu-id="f5c07-106">creare un ambito di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="f5c07-106">create private link scope</span></span>

## <span data-ttu-id="f5c07-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f5c07-107">EXAMPLES</span></span>

### <span data-ttu-id="f5c07-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f5c07-108">Example 1</span></span>
```powershell
New-AzInsightsPrivateLinkScope -Location "eastus" -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="f5c07-109">creare un ambito di collegamento privato con nome "scope_name" in gruppo risorse "rg_name" in posizione "eastus"</span><span class="sxs-lookup"><span data-stu-id="f5c07-109">create private link scope with name "scope_name" under resource group "rg_name" in location "eastus"</span></span>

## <span data-ttu-id="f5c07-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f5c07-110">PARAMETERS</span></span>

### <span data-ttu-id="f5c07-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5c07-111">-DefaultProfile</span></span>
<span data-ttu-id="f5c07-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f5c07-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5c07-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f5c07-113">-Location</span></span>
<span data-ttu-id="f5c07-114">Posizione</span><span class="sxs-lookup"><span data-stu-id="f5c07-114">Location</span></span>

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

### <span data-ttu-id="f5c07-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5c07-115">-Name</span></span>
<span data-ttu-id="f5c07-116">Nome ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="f5c07-116">Private Link Scope Name</span></span>

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

### <span data-ttu-id="f5c07-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5c07-117">-ResourceGroupName</span></span>
<span data-ttu-id="f5c07-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="f5c07-118">Resource Group Name</span></span>

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

### <span data-ttu-id="f5c07-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="f5c07-119">-Tags</span></span>
<span data-ttu-id="f5c07-120">Tag</span><span class="sxs-lookup"><span data-stu-id="f5c07-120">Tags</span></span>

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

### <span data-ttu-id="f5c07-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f5c07-121">-Confirm</span></span>
<span data-ttu-id="f5c07-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5c07-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5c07-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5c07-123">-WhatIf</span></span>
<span data-ttu-id="f5c07-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f5c07-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5c07-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f5c07-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5c07-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5c07-126">CommonParameters</span></span>
<span data-ttu-id="f5c07-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5c07-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5c07-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5c07-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5c07-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f5c07-129">INPUTS</span></span>

### <span data-ttu-id="f5c07-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f5c07-130">System.String</span></span>

## <span data-ttu-id="f5c07-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f5c07-131">OUTPUTS</span></span>

### <span data-ttu-id="f5c07-132">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="f5c07-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="f5c07-133">Note</span><span class="sxs-lookup"><span data-stu-id="f5c07-133">NOTES</span></span>

## <span data-ttu-id="f5c07-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f5c07-134">RELATED LINKS</span></span>

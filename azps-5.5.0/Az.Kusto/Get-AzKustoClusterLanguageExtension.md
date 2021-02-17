---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: 8ad074cf40074032fbab46cab6ee6c6c290eb2ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185278"
---
# <span data-ttu-id="c06f4-101">Get-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="c06f4-101">Get-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="c06f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c06f4-102">SYNOPSIS</span></span>
<span data-ttu-id="c06f4-103">Restituisce un elenco di estensioni delle lingue che possono essere eseguite all'interno di query KQL.</span><span class="sxs-lookup"><span data-stu-id="c06f4-103">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="c06f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c06f4-104">SYNTAX</span></span>

```
Get-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c06f4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c06f4-105">DESCRIPTION</span></span>
<span data-ttu-id="c06f4-106">Restituisce un elenco di estensioni delle lingue che possono essere eseguite all'interno di query KQL.</span><span class="sxs-lookup"><span data-stu-id="c06f4-106">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="c06f4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c06f4-107">EXAMPLES</span></span>

### <span data-ttu-id="c06f4-108">Esempio 1: Elencare tutte le estensioni delle lingue impostate per un cluster</span><span class="sxs-lookup"><span data-stu-id="c06f4-108">Example 1: List all language extensions set for a cluster</span></span>
```powershell
PS C:\> Get-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster

Name
----
R
PYTHON
```

<span data-ttu-id="c06f4-109">Il comando precedente restituisce un elenco di estensioni delle lingue che possono essere eseguite all'interno di query KQL.</span><span class="sxs-lookup"><span data-stu-id="c06f4-109">The above command returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="c06f4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c06f4-110">PARAMETERS</span></span>

### <span data-ttu-id="c06f4-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c06f4-111">-ClusterName</span></span>
<span data-ttu-id="c06f4-112">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c06f4-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="c06f4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c06f4-113">-DefaultProfile</span></span>
<span data-ttu-id="c06f4-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c06f4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c06f4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c06f4-115">-ResourceGroupName</span></span>
<span data-ttu-id="c06f4-116">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="c06f4-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="c06f4-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c06f4-117">-SubscriptionId</span></span>
<span data-ttu-id="c06f4-118">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c06f4-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c06f4-119">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c06f4-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c06f4-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c06f4-120">-Confirm</span></span>
<span data-ttu-id="c06f4-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c06f4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c06f4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c06f4-122">-WhatIf</span></span>
<span data-ttu-id="c06f4-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c06f4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c06f4-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c06f4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c06f4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c06f4-125">CommonParameters</span></span>
<span data-ttu-id="c06f4-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c06f4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c06f4-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c06f4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c06f4-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="c06f4-128">INPUTS</span></span>

## <span data-ttu-id="c06f4-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c06f4-129">OUTPUTS</span></span>

### <span data-ttu-id="c06f4-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.iLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="c06f4-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension</span></span>

## <span data-ttu-id="c06f4-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="c06f4-131">NOTES</span></span>

<span data-ttu-id="c06f4-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c06f4-132">ALIASES</span></span>

## <span data-ttu-id="c06f4-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c06f4-133">RELATED LINKS</span></span>


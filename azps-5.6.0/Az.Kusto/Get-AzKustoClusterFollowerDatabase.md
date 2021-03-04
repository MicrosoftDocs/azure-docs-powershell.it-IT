---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustoclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
ms.openlocfilehash: 5b53c9806fa541c28b7f318f464a26e9a88104e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964510"
---
# <span data-ttu-id="59666-101">Get-AzKustoClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="59666-101">Get-AzKustoClusterFollowerDatabase</span></span>

## <span data-ttu-id="59666-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59666-102">SYNOPSIS</span></span>
<span data-ttu-id="59666-103">Restituisce un elenco di database appartenenti al cluster e seguiti da un altro cluster.</span><span class="sxs-lookup"><span data-stu-id="59666-103">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="59666-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59666-104">SYNTAX</span></span>

```
Get-AzKustoClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="59666-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="59666-105">DESCRIPTION</span></span>
<span data-ttu-id="59666-106">Restituisce un elenco di database appartenenti al cluster e seguiti da un altro cluster.</span><span class="sxs-lookup"><span data-stu-id="59666-106">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="59666-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59666-107">EXAMPLES</span></span>

### <span data-ttu-id="59666-108">Esempio 1: Elencare tutti i database seguiti</span><span class="sxs-lookup"><span data-stu-id="59666-108">Example 1: List all followed databases</span></span>
```powershell
PS C:\>  Get-AzKustoClusterFollowerDatabase  -ResourceGroupName testrg -ClusterName testnewkustocluster

AttachedDatabaseConfigurationName ClusterResourceId                                                                                                                     DatabaseName
--------------------------------- -----------------                                                                                                                     ------------
myfollowerconfiguration             /subscriptions/xxxxxxxx-xxxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf mykustodatabase
```

<span data-ttu-id="59666-109">Il comando precedente elenca tutti i database che appartengono al cluster e sono stati seguiti da un altro cluster.</span><span class="sxs-lookup"><span data-stu-id="59666-109">The above command lists all the databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="59666-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59666-110">PARAMETERS</span></span>

### <span data-ttu-id="59666-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="59666-111">-ClusterName</span></span>
<span data-ttu-id="59666-112">Nome del cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="59666-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="59666-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59666-113">-DefaultProfile</span></span>
<span data-ttu-id="59666-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="59666-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59666-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59666-115">-ResourceGroupName</span></span>
<span data-ttu-id="59666-116">Nome del gruppo di risorse che contiene il cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="59666-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="59666-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="59666-117">-SubscriptionId</span></span>
<span data-ttu-id="59666-118">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="59666-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="59666-119">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="59666-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="59666-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59666-120">-Confirm</span></span>
<span data-ttu-id="59666-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59666-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59666-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59666-122">-WhatIf</span></span>
<span data-ttu-id="59666-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59666-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59666-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59666-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59666-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59666-125">CommonParameters</span></span>
<span data-ttu-id="59666-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59666-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59666-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="59666-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59666-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="59666-128">INPUTS</span></span>

## <span data-ttu-id="59666-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59666-129">OUTPUTS</span></span>

### <span data-ttu-id="59666-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IFollowerDatabaseDefinition</span><span class="sxs-lookup"><span data-stu-id="59666-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IFollowerDatabaseDefinition</span></span>

## <span data-ttu-id="59666-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="59666-131">NOTES</span></span>

<span data-ttu-id="59666-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="59666-132">ALIASES</span></span>

## <span data-ttu-id="59666-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59666-133">RELATED LINKS</span></span>


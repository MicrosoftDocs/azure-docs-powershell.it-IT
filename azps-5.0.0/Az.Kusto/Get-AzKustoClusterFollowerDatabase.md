---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
ms.openlocfilehash: e35e0731fb14cf8ca45b6e56d3957d13ccb88398
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202485"
---
# <span data-ttu-id="2c3a1-101">Get-AzKustoClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="2c3a1-101">Get-AzKustoClusterFollowerDatabase</span></span>

## <span data-ttu-id="2c3a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c3a1-102">SYNOPSIS</span></span>
<span data-ttu-id="2c3a1-103">Restituisce un elenco di database posseduti da questo cluster e seguiti da un altro cluster.</span><span class="sxs-lookup"><span data-stu-id="2c3a1-103">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="2c3a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c3a1-104">SYNTAX</span></span>

```
Get-AzKustoClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2c3a1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c3a1-105">DESCRIPTION</span></span>
<span data-ttu-id="2c3a1-106">Restituisce un elenco di database posseduti da questo cluster e seguiti da un altro cluster.</span><span class="sxs-lookup"><span data-stu-id="2c3a1-106">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="2c3a1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c3a1-107">EXAMPLES</span></span>

### <span data-ttu-id="2c3a1-108">Esempio 1: elenca tutti i database seguiti</span><span class="sxs-lookup"><span data-stu-id="2c3a1-108">Example 1: List all followed databases</span></span>
```powershell
PS C:\>  Get-AzKustoClusterFollowerDatabase  -ResourceGroupName testrg -ClusterName testnewkustocluster

AttachedDatabaseConfigurationName ClusterResourceId                                                                                                                     DatabaseName
--------------------------------- -----------------                                                                                                                     ------------
myfollowerconfiguration             /subscriptions/xxxxxxxx-xxxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf mykustodatabase
```

<span data-ttu-id="2c3a1-109">Il comando precedente elenca tutti i database di proprietà di questo cluster e seguiti da un altro cluster.</span><span class="sxs-lookup"><span data-stu-id="2c3a1-109">The above command lists all the databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="2c3a1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c3a1-110">PARAMETERS</span></span>

### <span data-ttu-id="2c3a1-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="2c3a1-111">-ClusterName</span></span>
<span data-ttu-id="2c3a1-112">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="2c3a1-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="2c3a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c3a1-113">-DefaultProfile</span></span>
<span data-ttu-id="2c3a1-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2c3a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c3a1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c3a1-115">-ResourceGroupName</span></span>
<span data-ttu-id="2c3a1-116">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="2c3a1-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="2c3a1-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2c3a1-117">-SubscriptionId</span></span>
<span data-ttu-id="2c3a1-118">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2c3a1-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2c3a1-119">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="2c3a1-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2c3a1-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2c3a1-120">-Confirm</span></span>
<span data-ttu-id="2c3a1-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c3a1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c3a1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c3a1-122">-WhatIf</span></span>
<span data-ttu-id="2c3a1-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2c3a1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c3a1-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2c3a1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c3a1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c3a1-125">CommonParameters</span></span>
<span data-ttu-id="2c3a1-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c3a1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c3a1-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c3a1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c3a1-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c3a1-128">INPUTS</span></span>

## <span data-ttu-id="2c3a1-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c3a1-129">OUTPUTS</span></span>

### <span data-ttu-id="2c3a1-130">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. IFollowerDatabaseDefinition</span><span class="sxs-lookup"><span data-stu-id="2c3a1-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IFollowerDatabaseDefinition</span></span>

## <span data-ttu-id="2c3a1-131">Note</span><span class="sxs-lookup"><span data-stu-id="2c3a1-131">NOTES</span></span>

<span data-ttu-id="2c3a1-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2c3a1-132">ALIASES</span></span>

## <span data-ttu-id="2c3a1-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c3a1-133">RELATED LINKS</span></span>


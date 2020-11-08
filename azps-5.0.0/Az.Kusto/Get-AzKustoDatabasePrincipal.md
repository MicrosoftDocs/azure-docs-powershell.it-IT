---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: c9b25327d170d05a4c2ad97b3cb7ce7626fbfec9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202474"
---
# <span data-ttu-id="ba978-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="ba978-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="ba978-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ba978-102">SYNOPSIS</span></span>
<span data-ttu-id="ba978-103">Restituisce un elenco di entità di database del cluster e del database kusto specificati.</span><span class="sxs-lookup"><span data-stu-id="ba978-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="ba978-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba978-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ba978-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba978-105">DESCRIPTION</span></span>
<span data-ttu-id="ba978-106">Restituisce un elenco di entità di database del cluster e del database kusto specificati.</span><span class="sxs-lookup"><span data-stu-id="ba978-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="ba978-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba978-107">EXAMPLES</span></span>

### <span data-ttu-id="ba978-108">Esempio 1: elenco delle entità di database del cluster e del database kusto specificati</span><span class="sxs-lookup"><span data-stu-id="ba978-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="ba978-109">Il comando precedente restituisce un elenco di entità di database del cluster e del database kusto specificati</span><span class="sxs-lookup"><span data-stu-id="ba978-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="ba978-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ba978-110">PARAMETERS</span></span>

### <span data-ttu-id="ba978-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="ba978-111">-ClusterName</span></span>
<span data-ttu-id="ba978-112">Il nome del cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="ba978-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ba978-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ba978-113">-DatabaseName</span></span>
<span data-ttu-id="ba978-114">Nome del database nel cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="ba978-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="ba978-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba978-115">-DefaultProfile</span></span>
<span data-ttu-id="ba978-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba978-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba978-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba978-117">-ResourceGroupName</span></span>
<span data-ttu-id="ba978-118">Nome del gruppo di risorse contenente il cluster kusto.</span><span class="sxs-lookup"><span data-stu-id="ba978-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ba978-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba978-119">-SubscriptionId</span></span>
<span data-ttu-id="ba978-120">Ottiene le credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ba978-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ba978-121">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="ba978-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ba978-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ba978-122">-Confirm</span></span>
<span data-ttu-id="ba978-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba978-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba978-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba978-124">-WhatIf</span></span>
<span data-ttu-id="ba978-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba978-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba978-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba978-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba978-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba978-127">CommonParameters</span></span>
<span data-ttu-id="ba978-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba978-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba978-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba978-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba978-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ba978-130">INPUTS</span></span>

## <span data-ttu-id="ba978-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba978-131">OUTPUTS</span></span>

### <span data-ttu-id="ba978-132">Microsoft. Azure. PowerShell. Cmdlets. kusto. Models. Api20200614. IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="ba978-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="ba978-133">Note</span><span class="sxs-lookup"><span data-stu-id="ba978-133">NOTES</span></span>

<span data-ttu-id="ba978-134">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ba978-134">ALIASES</span></span>

## <span data-ttu-id="ba978-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba978-135">RELATED LINKS</span></span>


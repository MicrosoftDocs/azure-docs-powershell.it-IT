---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
ms.openlocfilehash: e53857533770d6de0040d2d777020f1a2f9f320a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325763"
---
# <span data-ttu-id="e5806-101">Get-AzSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="e5806-101">Get-AzSqlServerServiceObjective</span></span>

## <span data-ttu-id="e5806-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e5806-102">SYNOPSIS</span></span>
<span data-ttu-id="e5806-103">Ottiene gli obiettivi di servizio per un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e5806-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="e5806-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5806-104">SYNTAX</span></span>

### <span data-ttu-id="e5806-105">ByLocation (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e5806-105">ByLocation (Default)</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5806-106">ByServer</span><span class="sxs-lookup"><span data-stu-id="e5806-106">ByServer</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ResourceGroupName] <String>
 [-ServerName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5806-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5806-107">DESCRIPTION</span></span>
<span data-ttu-id="e5806-108">Il cmdlet **Get-AzSqlServerServiceObjective** ottiene gli obiettivi di servizio disponibili per un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e5806-108">The **Get-AzSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="e5806-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5806-109">EXAMPLES</span></span>

### <span data-ttu-id="e5806-110">Esempio 1: ottenere gli obiettivi di servizio</span><span class="sxs-lookup"><span data-stu-id="e5806-110">Example 1: Get service objectives</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

<span data-ttu-id="e5806-111">Questo comando consente di ottenere gli obiettivi di servizio per il server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="e5806-111">This command gets the service objectives for the server named Server01.</span></span>

### <span data-ttu-id="e5806-112">Esempio 2: ottenere gli obiettivi di servizio tramite filtro</span><span class="sxs-lookup"><span data-stu-id="e5806-112">Example 2: Get service objectives using filtering</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServiceObjectiveName "P*"
ServiceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
```

<span data-ttu-id="e5806-113">Questo comando consente di ottenere gli obiettivi di servizio per il server denominato Server01 che iniziano con "System".</span><span class="sxs-lookup"><span data-stu-id="e5806-113">This command gets the service objectives for the server named Server01 that start with "System".</span></span>

### <span data-ttu-id="e5806-114">Esempio 3: ottenere gli obiettivi di servizio per una posizione</span><span class="sxs-lookup"><span data-stu-id="e5806-114">Example 3: Get service objectives for a location</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -Location "west us"
serviceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
System               System        System                  0        DTU          False
Free                 Free          Free                    5        DTU          True
Basic                Basic         Basic                   5        DTU          True
S0                   Standard      Standard                10       DTU          True
S1                   Standard      Standard                20       DTU          True
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
DW100c               DataWarehouse DataWarehouse           900      DTU          False
GP_Gen4_1            GP_Gen4       GeneralPurpose   Gen4   1        VCores       True
GP_Gen5_2            GP_Gen5       GeneralPurpose   Gen5   2        VCores       True
BC_Gen4_1            BC_Gen4       BusinessCritical Gen4   1        VCores       True
BC_Gen5_4            BC_Gen5       BusinessCritical Gen5   4        VCores       True
```

<span data-ttu-id="e5806-115">Questo comando ottiene gli obiettivi di servizio per un'area di Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="e5806-115">This command gets the service objectives for a specified Azure region.</span></span>

## <span data-ttu-id="e5806-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e5806-116">PARAMETERS</span></span>

### <span data-ttu-id="e5806-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5806-117">-DefaultProfile</span></span>
<span data-ttu-id="e5806-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e5806-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5806-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e5806-119">-Location</span></span>
<span data-ttu-id="e5806-120">Nome della posizione per cui ottenere gli obiettivi di servizio.</span><span class="sxs-lookup"><span data-stu-id="e5806-120">The name of the Location for which to get the service objectives.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5806-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5806-121">-ResourceGroupName</span></span>
<span data-ttu-id="e5806-122">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e5806-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="e5806-123">Questo cmdlet ottiene gli obiettivi di servizio per un server di database SQL assegnato alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="e5806-123">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5806-124">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="e5806-124">-ServerName</span></span>
<span data-ttu-id="e5806-125">Specifica il nome di un server di database SQL di database SQL.</span><span class="sxs-lookup"><span data-stu-id="e5806-125">Specifies the name of a SQL Database SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5806-126">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="e5806-126">-ServiceObjectiveName</span></span>
<span data-ttu-id="e5806-127">Specifica il nome di un obiettivo di servizio per un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="e5806-127">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="e5806-128">I valori accettabili per questo parametro sono: Basic, S0, S1, S2, P1, P2 e P3.</span><span class="sxs-lookup"><span data-stu-id="e5806-128">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5806-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e5806-129">-Confirm</span></span>
<span data-ttu-id="e5806-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5806-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5806-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5806-131">-WhatIf</span></span>
<span data-ttu-id="e5806-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5806-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5806-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e5806-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5806-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5806-134">CommonParameters</span></span>
<span data-ttu-id="e5806-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5806-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5806-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5806-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5806-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e5806-137">INPUTS</span></span>

### <span data-ttu-id="e5806-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e5806-138">System.String</span></span>

## <span data-ttu-id="e5806-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5806-139">OUTPUTS</span></span>

### <span data-ttu-id="e5806-140">Microsoft. Azure. Commands. SQL. ServiceObjective. Model. AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="e5806-140">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="e5806-141">Note</span><span class="sxs-lookup"><span data-stu-id="e5806-141">NOTES</span></span>

## <span data-ttu-id="e5806-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5806-142">RELATED LINKS</span></span>

[<span data-ttu-id="e5806-143">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="e5806-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



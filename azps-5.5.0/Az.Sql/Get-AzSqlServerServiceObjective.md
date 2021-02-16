---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerServiceObjective.md
ms.openlocfilehash: e53857533770d6de0040d2d777020f1a2f9f320a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201479"
---
# <span data-ttu-id="beafd-101">Get-AzSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="beafd-101">Get-AzSqlServerServiceObjective</span></span>

## <span data-ttu-id="beafd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="beafd-102">SYNOPSIS</span></span>
<span data-ttu-id="beafd-103">Ottiene gli obiettivi del servizio per un server di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="beafd-103">Gets service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="beafd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="beafd-104">SYNTAX</span></span>

### <span data-ttu-id="beafd-105">ByLocation (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="beafd-105">ByLocation (Default)</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="beafd-106">ByServer</span><span class="sxs-lookup"><span data-stu-id="beafd-106">ByServer</span></span>
```
Get-AzSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ResourceGroupName] <String>
 [-ServerName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="beafd-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="beafd-107">DESCRIPTION</span></span>
<span data-ttu-id="beafd-108">Il cmdlet **Get-AzSqlServerServiceObjective** ottiene gli obiettivi di servizio disponibili per un server di database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="beafd-108">The **Get-AzSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="beafd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="beafd-109">EXAMPLES</span></span>

### <span data-ttu-id="beafd-110">Esempio 1: Ottenere gli obiettivi del servizio</span><span class="sxs-lookup"><span data-stu-id="beafd-110">Example 1: Get service objectives</span></span>
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

<span data-ttu-id="beafd-111">Questo comando ottiene gli obiettivi del servizio per il server denominato Server01.</span><span class="sxs-lookup"><span data-stu-id="beafd-111">This command gets the service objectives for the server named Server01.</span></span>

### <span data-ttu-id="beafd-112">Esempio 2: Ottenere gli obiettivi del servizio con i filtri</span><span class="sxs-lookup"><span data-stu-id="beafd-112">Example 2: Get service objectives using filtering</span></span>
```
PS C:\>Get-AzSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServiceObjectiveName "P*"
ServiceObjectiveName SkuName       Edition          Family Capacity CapacityUnit Enabled
-------------------- -------       -------          ------ -------- ------------ -------
P1                   Premium       Premium                 125      DTU          True
P2                   Premium       Premium                 250      DTU          True
```

<span data-ttu-id="beafd-113">Questo comando ottiene gli obiettivi del servizio per il server denominato Server01 che inizia con "Sistema".</span><span class="sxs-lookup"><span data-stu-id="beafd-113">This command gets the service objectives for the server named Server01 that start with "System".</span></span>

### <span data-ttu-id="beafd-114">Esempio 3: Ottenere gli obiettivi del servizio per una località</span><span class="sxs-lookup"><span data-stu-id="beafd-114">Example 3: Get service objectives for a location</span></span>
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

<span data-ttu-id="beafd-115">Questo comando ottiene gli obiettivi del servizio per un'area geografica di Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="beafd-115">This command gets the service objectives for a specified Azure region.</span></span>

## <span data-ttu-id="beafd-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="beafd-116">PARAMETERS</span></span>

### <span data-ttu-id="beafd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beafd-117">-DefaultProfile</span></span>
<span data-ttu-id="beafd-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="beafd-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="beafd-119">-Location</span><span class="sxs-lookup"><span data-stu-id="beafd-119">-Location</span></span>
<span data-ttu-id="beafd-120">Nome della posizione per cui ottenere gli obiettivi del servizio.</span><span class="sxs-lookup"><span data-stu-id="beafd-120">The name of the Location for which to get the service objectives.</span></span>

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

### <span data-ttu-id="beafd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beafd-121">-ResourceGroupName</span></span>
<span data-ttu-id="beafd-122">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="beafd-122">Specifies the name of a resource group.</span></span>
<span data-ttu-id="beafd-123">Questo cmdlet ottiene gli obiettivi del servizio per un server SQL database assegnato alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="beafd-123">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

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

### <span data-ttu-id="beafd-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="beafd-124">-ServerName</span></span>
<span data-ttu-id="beafd-125">Specifica il nome di un server di SQL database SQL server di database.</span><span class="sxs-lookup"><span data-stu-id="beafd-125">Specifies the name of a SQL Database SQL Database server.</span></span>

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

### <span data-ttu-id="beafd-126">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="beafd-126">-ServiceObjectiveName</span></span>
<span data-ttu-id="beafd-127">Specifica il nome di un obiettivo del servizio per un server di database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="beafd-127">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="beafd-128">I valori accettabili per questo parametro sono: Base, S0, S1, S2, P1, P2 e P3.</span><span class="sxs-lookup"><span data-stu-id="beafd-128">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

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

### <span data-ttu-id="beafd-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="beafd-129">-Confirm</span></span>
<span data-ttu-id="beafd-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="beafd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="beafd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beafd-131">-WhatIf</span></span>
<span data-ttu-id="beafd-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="beafd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="beafd-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="beafd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="beafd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beafd-134">CommonParameters</span></span>
<span data-ttu-id="beafd-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beafd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beafd-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="beafd-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beafd-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="beafd-137">INPUTS</span></span>

### <span data-ttu-id="beafd-138">System.String</span><span class="sxs-lookup"><span data-stu-id="beafd-138">System.String</span></span>

## <span data-ttu-id="beafd-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="beafd-139">OUTPUTS</span></span>

### <span data-ttu-id="beafd-140">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="beafd-140">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="beafd-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="beafd-141">NOTES</span></span>

## <span data-ttu-id="beafd-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="beafd-142">RELATED LINKS</span></span>

[<span data-ttu-id="beafd-143">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="beafd-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



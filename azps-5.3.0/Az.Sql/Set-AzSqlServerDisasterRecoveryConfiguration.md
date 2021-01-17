---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: c49eb386265dff2650ba9bdb0882d25be98fca0c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475430"
---
# <span data-ttu-id="44eda-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="44eda-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="44eda-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="44eda-102">SYNOPSIS</span></span>
<span data-ttu-id="44eda-103">Modifica una configurazione di ripristino del server di database.</span><span class="sxs-lookup"><span data-stu-id="44eda-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="44eda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="44eda-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44eda-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44eda-105">DESCRIPTION</span></span>
<span data-ttu-id="44eda-106">Il cmdlet **set-AzSqlServerDisasterRecoveryConfiguration** modifica una configurazione di ripristino di database di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="44eda-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="44eda-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="44eda-107">EXAMPLES</span></span>

## <span data-ttu-id="44eda-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="44eda-108">PARAMETERS</span></span>

### <span data-ttu-id="44eda-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="44eda-109">-AllowDataLoss</span></span>
<span data-ttu-id="44eda-110">Indica che l'operazione di failover consente la perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="44eda-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="44eda-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44eda-111">-AsJob</span></span>
<span data-ttu-id="44eda-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="44eda-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44eda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44eda-113">-DefaultProfile</span></span>
<span data-ttu-id="44eda-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="44eda-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44eda-115">-Failover</span><span class="sxs-lookup"><span data-stu-id="44eda-115">-Failover</span></span>
<span data-ttu-id="44eda-116">Indica che questa operazione è un failover.</span><span class="sxs-lookup"><span data-stu-id="44eda-116">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44eda-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44eda-117">-ResourceGroupName</span></span>
<span data-ttu-id="44eda-118">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="44eda-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="44eda-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="44eda-119">-ServerName</span></span>
<span data-ttu-id="44eda-120">Specifica il nome di un server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="44eda-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="44eda-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="44eda-121">-VirtualEndpointName</span></span>
<span data-ttu-id="44eda-122">Specifica il nome di un punto finale virtuale.</span><span class="sxs-lookup"><span data-stu-id="44eda-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="44eda-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="44eda-123">-Confirm</span></span>
<span data-ttu-id="44eda-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44eda-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44eda-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44eda-125">-WhatIf</span></span>
<span data-ttu-id="44eda-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44eda-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44eda-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="44eda-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44eda-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44eda-128">CommonParameters</span></span>
<span data-ttu-id="44eda-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44eda-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44eda-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44eda-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44eda-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="44eda-131">INPUTS</span></span>

### <span data-ttu-id="44eda-132">System. String</span><span class="sxs-lookup"><span data-stu-id="44eda-132">System.String</span></span>

## <span data-ttu-id="44eda-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="44eda-133">OUTPUTS</span></span>

### <span data-ttu-id="44eda-134">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="44eda-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="44eda-135">Note</span><span class="sxs-lookup"><span data-stu-id="44eda-135">NOTES</span></span>

## <span data-ttu-id="44eda-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="44eda-136">RELATED LINKS</span></span>

[<span data-ttu-id="44eda-137">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="44eda-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="44eda-138">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="44eda-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="44eda-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="44eda-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="44eda-140">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="44eda-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

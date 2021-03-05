---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a1f91c01d3183551cbabf58754fbe628e1feea32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992388"
---
# <span data-ttu-id="31f06-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="31f06-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="31f06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31f06-102">SYNOPSIS</span></span>
<span data-ttu-id="31f06-103">Modifica una configurazione di ripristino del server di database.</span><span class="sxs-lookup"><span data-stu-id="31f06-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="31f06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31f06-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31f06-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="31f06-105">DESCRIPTION</span></span>
<span data-ttu-id="31f06-106">Il cmdlet **Set-AzSqlServerDisasterRecoveryConfiguration** modifica una configurazione SQL ripristino del server di database.</span><span class="sxs-lookup"><span data-stu-id="31f06-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="31f06-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31f06-107">EXAMPLES</span></span>

## <span data-ttu-id="31f06-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31f06-108">PARAMETERS</span></span>

### <span data-ttu-id="31f06-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="31f06-109">-AllowDataLoss</span></span>
<span data-ttu-id="31f06-110">Indica che l'operazione di failover consente la perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="31f06-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="31f06-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31f06-111">-AsJob</span></span>
<span data-ttu-id="31f06-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="31f06-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="31f06-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f06-113">-DefaultProfile</span></span>
<span data-ttu-id="31f06-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="31f06-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31f06-115">-Failover</span><span class="sxs-lookup"><span data-stu-id="31f06-115">-Failover</span></span>
<span data-ttu-id="31f06-116">Indica che l'operazione è un failover.</span><span class="sxs-lookup"><span data-stu-id="31f06-116">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="31f06-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31f06-117">-ResourceGroupName</span></span>
<span data-ttu-id="31f06-118">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="31f06-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="31f06-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="31f06-119">-ServerName</span></span>
<span data-ttu-id="31f06-120">Specifica il nome di un server di SQL database.</span><span class="sxs-lookup"><span data-stu-id="31f06-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="31f06-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="31f06-121">-VirtualEndpointName</span></span>
<span data-ttu-id="31f06-122">Specifica il nome di un punto finale virtuale.</span><span class="sxs-lookup"><span data-stu-id="31f06-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="31f06-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31f06-123">-Confirm</span></span>
<span data-ttu-id="31f06-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31f06-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31f06-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31f06-125">-WhatIf</span></span>
<span data-ttu-id="31f06-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31f06-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31f06-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31f06-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31f06-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f06-128">CommonParameters</span></span>
<span data-ttu-id="31f06-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31f06-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f06-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="31f06-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f06-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="31f06-131">INPUTS</span></span>

### <span data-ttu-id="31f06-132">System.String</span><span class="sxs-lookup"><span data-stu-id="31f06-132">System.String</span></span>

## <span data-ttu-id="31f06-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31f06-133">OUTPUTS</span></span>

### <span data-ttu-id="31f06-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="31f06-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="31f06-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="31f06-135">NOTES</span></span>

## <span data-ttu-id="31f06-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31f06-136">RELATED LINKS</span></span>

[<span data-ttu-id="31f06-137">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="31f06-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="31f06-138">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="31f06-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="31f06-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="31f06-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="31f06-140">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="31f06-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

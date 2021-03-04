---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
ms.openlocfilehash: 565d22bc2860acc69f5d919bf000a564d9295ce5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955165"
---
# <span data-ttu-id="987d3-101">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="987d3-101">Remove-AzSqlElasticPool</span></span>

## <span data-ttu-id="987d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="987d3-102">SYNOPSIS</span></span>
<span data-ttu-id="987d3-103">Elimina un pool di database flessibile.</span><span class="sxs-lookup"><span data-stu-id="987d3-103">Deletes an elastic database pool.</span></span>

## <span data-ttu-id="987d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="987d3-104">SYNTAX</span></span>

```
Remove-AzSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="987d3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="987d3-105">DESCRIPTION</span></span>
<span data-ttu-id="987d3-106">Il cmdlet **Remove-AzSqlElasticPool** elimina un pool di SQL database flessibile di Azure.</span><span class="sxs-lookup"><span data-stu-id="987d3-106">The **Remove-AzSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="987d3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="987d3-107">EXAMPLES</span></span>

### <span data-ttu-id="987d3-108">Esempio 1: Eliminare un pool flessibile</span><span class="sxs-lookup"><span data-stu-id="987d3-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="987d3-109">Questo comando elimina un pool elastico denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="987d3-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="987d3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="987d3-110">PARAMETERS</span></span>

### <span data-ttu-id="987d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="987d3-111">-DefaultProfile</span></span>
<span data-ttu-id="987d3-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="987d3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="987d3-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="987d3-113">-ElasticPoolName</span></span>
<span data-ttu-id="987d3-114">Specifica il nome del pool flessibile eliminato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="987d3-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="987d3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="987d3-115">-Force</span></span>
<span data-ttu-id="987d3-116">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="987d3-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="987d3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="987d3-117">-ResourceGroupName</span></span>
<span data-ttu-id="987d3-118">Specifica il nome del gruppo di risorse a cui è assegnato il pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="987d3-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="987d3-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="987d3-119">-ServerName</span></span>
<span data-ttu-id="987d3-120">Specifica il nome del server che ospita il pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="987d3-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="987d3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="987d3-121">-Confirm</span></span>
<span data-ttu-id="987d3-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="987d3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="987d3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="987d3-123">-WhatIf</span></span>
<span data-ttu-id="987d3-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="987d3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="987d3-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="987d3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="987d3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="987d3-126">CommonParameters</span></span>
<span data-ttu-id="987d3-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="987d3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="987d3-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="987d3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="987d3-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="987d3-129">INPUTS</span></span>

### <span data-ttu-id="987d3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="987d3-130">System.String</span></span>

## <span data-ttu-id="987d3-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="987d3-131">OUTPUTS</span></span>

### <span data-ttu-id="987d3-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="987d3-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="987d3-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="987d3-133">NOTES</span></span>

## <span data-ttu-id="987d3-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="987d3-134">RELATED LINKS</span></span>

[<span data-ttu-id="987d3-135">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="987d3-135">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="987d3-136">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="987d3-136">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="987d3-137">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="987d3-137">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="987d3-138">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="987d3-138">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="987d3-139">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="987d3-139">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="987d3-140">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="987d3-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



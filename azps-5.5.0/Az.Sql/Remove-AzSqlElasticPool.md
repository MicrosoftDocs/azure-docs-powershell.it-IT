---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
ms.openlocfilehash: d751954a5c66d9220513017aa62b6797f8f1ea6f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197679"
---
# <span data-ttu-id="34e23-101">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="34e23-101">Remove-AzSqlElasticPool</span></span>

## <span data-ttu-id="34e23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34e23-102">SYNOPSIS</span></span>
<span data-ttu-id="34e23-103">Elimina un pool di database flessibile.</span><span class="sxs-lookup"><span data-stu-id="34e23-103">Deletes an elastic database pool.</span></span>

## <span data-ttu-id="34e23-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34e23-104">SYNTAX</span></span>

```
Remove-AzSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34e23-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="34e23-105">DESCRIPTION</span></span>
<span data-ttu-id="34e23-106">Il cmdlet **Remove-AzSqlElasticPool** elimina un pool di SQL database flessibile di Azure.</span><span class="sxs-lookup"><span data-stu-id="34e23-106">The **Remove-AzSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="34e23-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34e23-107">EXAMPLES</span></span>

### <span data-ttu-id="34e23-108">Esempio 1: Eliminare un pool flessibile</span><span class="sxs-lookup"><span data-stu-id="34e23-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="34e23-109">Questo comando elimina un pool elastico denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="34e23-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="34e23-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34e23-110">PARAMETERS</span></span>

### <span data-ttu-id="34e23-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34e23-111">-DefaultProfile</span></span>
<span data-ttu-id="34e23-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="34e23-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34e23-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="34e23-113">-ElasticPoolName</span></span>
<span data-ttu-id="34e23-114">Specifica il nome del pool flessibile eliminato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34e23-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="34e23-115">-Force</span><span class="sxs-lookup"><span data-stu-id="34e23-115">-Force</span></span>
<span data-ttu-id="34e23-116">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="34e23-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="34e23-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34e23-117">-ResourceGroupName</span></span>
<span data-ttu-id="34e23-118">Specifica il nome del gruppo di risorse a cui è assegnato il pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="34e23-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="34e23-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="34e23-119">-ServerName</span></span>
<span data-ttu-id="34e23-120">Specifica il nome del server che ospita il pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="34e23-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="34e23-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34e23-121">-Confirm</span></span>
<span data-ttu-id="34e23-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34e23-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34e23-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34e23-123">-WhatIf</span></span>
<span data-ttu-id="34e23-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34e23-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34e23-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34e23-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34e23-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e23-126">CommonParameters</span></span>
<span data-ttu-id="34e23-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34e23-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e23-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34e23-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e23-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="34e23-129">INPUTS</span></span>

### <span data-ttu-id="34e23-130">System.String</span><span class="sxs-lookup"><span data-stu-id="34e23-130">System.String</span></span>

## <span data-ttu-id="34e23-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34e23-131">OUTPUTS</span></span>

### <span data-ttu-id="34e23-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="34e23-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="34e23-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="34e23-133">NOTES</span></span>

## <span data-ttu-id="34e23-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34e23-134">RELATED LINKS</span></span>

[<span data-ttu-id="34e23-135">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="34e23-135">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="34e23-136">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="34e23-136">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="34e23-137">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="34e23-137">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="34e23-138">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="34e23-138">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="34e23-139">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="34e23-139">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="34e23-140">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="34e23-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)



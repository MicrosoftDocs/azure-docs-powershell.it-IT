---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
ms.openlocfilehash: caca08a5a9390d3e80fdef8309244a8a4d29aec0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200107"
---
# <span data-ttu-id="6a3bc-101">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="6a3bc-101">Remove-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="6a3bc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a3bc-102">SYNOPSIS</span></span>
<span data-ttu-id="6a3bc-103">Rimuove le impostazioni di controllo di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="6a3bc-103">Removes the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="6a3bc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a3bc-104">SYNTAX</span></span>

### <span data-ttu-id="6a3bc-105">DatabaseParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6a3bc-105">DatabaseParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a3bc-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a3bc-106">DatabaseObjectParameterSet</span></span>
```
Remove-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a3bc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a3bc-107">DESCRIPTION</span></span>
<span data-ttu-id="6a3bc-108">Il cmdlet **Remove-AzSqlDatabaseAudit** rimuove le impostazioni di controllo di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="6a3bc-108">The **Remove-AzSqlDatabaseAudit** cmdlet removes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="6a3bc-109">Per usare il cmdlet, usare i parametri *ResourceGroupName* , *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="6a3bc-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="6a3bc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a3bc-110">EXAMPLES</span></span>

### <span data-ttu-id="6a3bc-111">Esempio 1: rimuovere le impostazioni di controllo di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="6a3bc-111">Example 1: Remove the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Remove-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="6a3bc-112">Esempio 2: rimuovere, tramite pipeline, le impostazioni di controllo di un database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="6a3bc-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Remove-AzSqlDatabaseAudit
```

## <span data-ttu-id="6a3bc-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a3bc-113">PARAMETERS</span></span>

### <span data-ttu-id="6a3bc-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6a3bc-114">-DatabaseName</span></span>
<span data-ttu-id="6a3bc-115">Nome database SQL.</span><span class="sxs-lookup"><span data-stu-id="6a3bc-115">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a3bc-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="6a3bc-116">-DatabaseObject</span></span>
<span data-ttu-id="6a3bc-117">Oggetto database per gestire i criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="6a3bc-117">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a3bc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a3bc-118">-DefaultProfile</span></span>
<span data-ttu-id="6a3bc-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a3bc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a3bc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a3bc-120">-ResourceGroupName</span></span>
<span data-ttu-id="6a3bc-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6a3bc-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a3bc-122">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="6a3bc-122">-ServerName</span></span>
<span data-ttu-id="6a3bc-123">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6a3bc-123">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a3bc-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6a3bc-124">-Confirm</span></span>
<span data-ttu-id="6a3bc-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a3bc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a3bc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a3bc-126">-WhatIf</span></span>
<span data-ttu-id="6a3bc-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a3bc-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a3bc-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a3bc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a3bc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a3bc-129">CommonParameters</span></span>
<span data-ttu-id="6a3bc-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a3bc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a3bc-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a3bc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a3bc-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a3bc-132">INPUTS</span></span>

### <span data-ttu-id="6a3bc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6a3bc-133">System.String</span></span>

### <span data-ttu-id="6a3bc-134">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="6a3bc-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="6a3bc-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a3bc-135">OUTPUTS</span></span>

### <span data-ttu-id="6a3bc-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6a3bc-136">System.Boolean</span></span>

## <span data-ttu-id="6a3bc-137">Note</span><span class="sxs-lookup"><span data-stu-id="6a3bc-137">NOTES</span></span>

## <span data-ttu-id="6a3bc-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a3bc-138">RELATED LINKS</span></span>

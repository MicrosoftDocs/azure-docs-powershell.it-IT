---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Remove-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseAudit.md
ms.openlocfilehash: 9688475a1d8bae19b10bc5626dca643ac947156d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961406"
---
# <span data-ttu-id="e9ca5-101">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e9ca5-101">Remove-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="e9ca5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9ca5-102">SYNOPSIS</span></span>
<span data-ttu-id="e9ca5-103">Rimuove le impostazioni di controllo di un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e9ca5-103">Removes the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="e9ca5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9ca5-104">SYNTAX</span></span>

### <span data-ttu-id="e9ca5-105">DatabaseParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e9ca5-105">DatabaseParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9ca5-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9ca5-106">DatabaseObjectParameterSet</span></span>
```
Remove-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9ca5-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e9ca5-107">DESCRIPTION</span></span>
<span data-ttu-id="e9ca5-108">Il cmdlet **Remove-AzSqlDatabaseAudit** rimuove le impostazioni di controllo di un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e9ca5-108">The **Remove-AzSqlDatabaseAudit** cmdlet removes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="e9ca5-109">Per usare il cmdlet, usare i *parametri ResourceGroupName,* *ServerName* e *DatabaseName* per identificare il database.</span><span class="sxs-lookup"><span data-stu-id="e9ca5-109">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="e9ca5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9ca5-110">EXAMPLES</span></span>

### <span data-ttu-id="e9ca5-111">Esempio 1: Rimuovere le impostazioni di controllo di un database di SQL Azure</span><span class="sxs-lookup"><span data-stu-id="e9ca5-111">Example 1: Remove the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Remove-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="e9ca5-112">Esempio 2: Rimuovere tramite pipeline le impostazioni di controllo di un database SQL Azure</span><span class="sxs-lookup"><span data-stu-id="e9ca5-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Remove-AzSqlDatabaseAudit
```

## <span data-ttu-id="e9ca5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9ca5-113">PARAMETERS</span></span>

### <span data-ttu-id="e9ca5-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e9ca5-114">-DatabaseName</span></span>
<span data-ttu-id="e9ca5-115">SQL nome del database.</span><span class="sxs-lookup"><span data-stu-id="e9ca5-115">SQL Database name.</span></span>

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

### <span data-ttu-id="e9ca5-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="e9ca5-116">-DatabaseObject</span></span>
<span data-ttu-id="e9ca5-117">Oggetto di database per la gestione dei criteri di controllo.</span><span class="sxs-lookup"><span data-stu-id="e9ca5-117">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="e9ca5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9ca5-118">-DefaultProfile</span></span>
<span data-ttu-id="e9ca5-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e9ca5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9ca5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9ca5-120">-ResourceGroupName</span></span>
<span data-ttu-id="e9ca5-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e9ca5-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="e9ca5-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e9ca5-122">-ServerName</span></span>
<span data-ttu-id="e9ca5-123">SQL del server.</span><span class="sxs-lookup"><span data-stu-id="e9ca5-123">SQL server name.</span></span>

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

### <span data-ttu-id="e9ca5-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9ca5-124">-Confirm</span></span>
<span data-ttu-id="e9ca5-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9ca5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9ca5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9ca5-126">-WhatIf</span></span>
<span data-ttu-id="e9ca5-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e9ca5-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9ca5-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e9ca5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9ca5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9ca5-129">CommonParameters</span></span>
<span data-ttu-id="e9ca5-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9ca5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9ca5-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e9ca5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9ca5-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="e9ca5-132">INPUTS</span></span>

### <span data-ttu-id="e9ca5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e9ca5-133">System.String</span></span>

### <span data-ttu-id="e9ca5-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e9ca5-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="e9ca5-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9ca5-135">OUTPUTS</span></span>

### <span data-ttu-id="e9ca5-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e9ca5-136">System.Boolean</span></span>

## <span data-ttu-id="e9ca5-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="e9ca5-137">NOTES</span></span>

## <span data-ttu-id="e9ca5-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9ca5-138">RELATED LINKS</span></span>

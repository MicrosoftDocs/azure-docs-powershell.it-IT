---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 0e3bfc112ee8c80d08b0b5a87eb574a4c5bdb29e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957934"
---
# <span data-ttu-id="d9ad3-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d9ad3-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="d9ad3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9ad3-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ad3-103">Rimuove un gruppo di failover delle istanze.</span><span class="sxs-lookup"><span data-stu-id="d9ad3-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="d9ad3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9ad3-104">SYNTAX</span></span>

### <span data-ttu-id="d9ad3-105">RemoveIFGDefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d9ad3-105">RemoveIFGDefaultSet (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ad3-106">RemoveInstanceFailoverGroupByResourceId</span><span class="sxs-lookup"><span data-stu-id="d9ad3-106">RemoveInstanceFailoverGroupByResourceId</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ad3-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="d9ad3-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9ad3-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d9ad3-108">DESCRIPTION</span></span>
<span data-ttu-id="d9ad3-109">Questo comando rimuove il gruppo di failover delle istanze con il nome specificato, lasciando inalterati tutti i database.</span><span class="sxs-lookup"><span data-stu-id="d9ad3-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="d9ad3-110">L'endpoint del listener verrà ne verrà annullata la registrazione dal DNS.</span><span class="sxs-lookup"><span data-stu-id="d9ad3-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="d9ad3-111">L'area principale del gruppo di failover dell'istanza deve essere usata per eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="d9ad3-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="d9ad3-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9ad3-112">EXAMPLES</span></span>

### <span data-ttu-id="d9ad3-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d9ad3-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="d9ad3-114">Rimuovere un gruppo di failover delle istanze.</span><span class="sxs-lookup"><span data-stu-id="d9ad3-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="d9ad3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9ad3-115">PARAMETERS</span></span>

### <span data-ttu-id="d9ad3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ad3-116">-DefaultProfile</span></span>
<span data-ttu-id="d9ad3-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9ad3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9ad3-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d9ad3-118">-Force</span></span>
<span data-ttu-id="d9ad3-119">Ignorare il messaggio di conferma per l'esecuzione dell'azione.</span><span class="sxs-lookup"><span data-stu-id="d9ad3-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="d9ad3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9ad3-120">-InputObject</span></span>
<span data-ttu-id="d9ad3-121">Oggetto Gruppo di failover dell'istanza da rimuovere</span><span class="sxs-lookup"><span data-stu-id="d9ad3-121">The Instance Failover Group object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ad3-122">-Location</span><span class="sxs-lookup"><span data-stu-id="d9ad3-122">-Location</span></span>
<span data-ttu-id="d9ad3-123">Nome dell'area locale da cui recuperare il gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="d9ad3-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet, RemoveInstanceFailoverGroupByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ad3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d9ad3-124">-Name</span></span>
<span data-ttu-id="d9ad3-125">Nome del gruppo di failover delle istanze da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="d9ad3-125">The name of the Instance Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ad3-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9ad3-126">-PassThru</span></span>
<span data-ttu-id="d9ad3-127">Specifica se passare attraverso l'output di esecuzione del cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9ad3-127">Specifies whether to pass through cmdlet execution output.</span></span>

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

### <span data-ttu-id="d9ad3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9ad3-128">-ResourceGroupName</span></span>
<span data-ttu-id="d9ad3-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d9ad3-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ad3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9ad3-130">-ResourceId</span></span>
<span data-ttu-id="d9ad3-131">ID risorsa del gruppo di failover dell'istanza da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="d9ad3-131">The Resource ID of the Instance Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFailoverGroupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ad3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d9ad3-132">-Confirm</span></span>
<span data-ttu-id="d9ad3-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9ad3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9ad3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9ad3-134">-WhatIf</span></span>
<span data-ttu-id="d9ad3-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9ad3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9ad3-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9ad3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9ad3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ad3-137">CommonParameters</span></span>
<span data-ttu-id="d9ad3-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9ad3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ad3-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d9ad3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ad3-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="d9ad3-140">INPUTS</span></span>

### <span data-ttu-id="d9ad3-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="d9ad3-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="d9ad3-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d9ad3-142">System.String</span></span>

## <span data-ttu-id="d9ad3-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9ad3-143">OUTPUTS</span></span>

### <span data-ttu-id="d9ad3-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="d9ad3-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="d9ad3-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="d9ad3-145">NOTES</span></span>

## <span data-ttu-id="d9ad3-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9ad3-146">RELATED LINKS</span></span>

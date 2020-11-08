---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 12bc26177a249995f748a879a9ae8d2f73900c99
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021155"
---
# <span data-ttu-id="c853a-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c853a-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="c853a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c853a-102">SYNOPSIS</span></span>
<span data-ttu-id="c853a-103">Rimuove un gruppo di failover delle istanze.</span><span class="sxs-lookup"><span data-stu-id="c853a-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="c853a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c853a-104">SYNTAX</span></span>

### <span data-ttu-id="c853a-105">RemoveIFGDefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c853a-105">RemoveIFGDefaultSet (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c853a-106">RemoveInstanceFailoverGroupByResourceId</span><span class="sxs-lookup"><span data-stu-id="c853a-106">RemoveInstanceFailoverGroupByResourceId</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c853a-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="c853a-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c853a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c853a-108">DESCRIPTION</span></span>
<span data-ttu-id="c853a-109">Questo comando rimuove il gruppo di failover dell'istanza con il nome specificato, lasciando intatti tutti i database.</span><span class="sxs-lookup"><span data-stu-id="c853a-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="c853a-110">L'endpoint del listener verrà annullata la registrazione dal DNS.</span><span class="sxs-lookup"><span data-stu-id="c853a-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="c853a-111">L'area principale del gruppo di failover dell'istanza deve essere usata per eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="c853a-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="c853a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c853a-112">EXAMPLES</span></span>

### <span data-ttu-id="c853a-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c853a-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="c853a-114">Rimuovere un gruppo di failover delle istanze.</span><span class="sxs-lookup"><span data-stu-id="c853a-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="c853a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c853a-115">PARAMETERS</span></span>

### <span data-ttu-id="c853a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c853a-116">-DefaultProfile</span></span>
<span data-ttu-id="c853a-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c853a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c853a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c853a-118">-Force</span></span>
<span data-ttu-id="c853a-119">Ignorare il messaggio di conferma per l'esecuzione dell'azione.</span><span class="sxs-lookup"><span data-stu-id="c853a-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="c853a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c853a-120">-InputObject</span></span>
<span data-ttu-id="c853a-121">Oggetto gruppo di failover dell'istanza da rimuovere</span><span class="sxs-lookup"><span data-stu-id="c853a-121">The Instance Failover Group object to remove</span></span>

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

### <span data-ttu-id="c853a-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c853a-122">-Location</span></span>
<span data-ttu-id="c853a-123">Nome dell'area geografica locale da cui recuperare il gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="c853a-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="c853a-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c853a-124">-Name</span></span>
<span data-ttu-id="c853a-125">Nome del gruppo di failover dell'istanza da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c853a-125">The name of the Instance Failover Group to remove.</span></span>

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

### <span data-ttu-id="c853a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c853a-126">-PassThru</span></span>
<span data-ttu-id="c853a-127">Specifica se passare all'output di esecuzione del cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c853a-127">Specifies whether to pass through cmdlet execution output.</span></span>

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

### <span data-ttu-id="c853a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c853a-128">-ResourceGroupName</span></span>
<span data-ttu-id="c853a-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c853a-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="c853a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c853a-130">-ResourceId</span></span>
<span data-ttu-id="c853a-131">ID risorsa del gruppo di failover delle istanze da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c853a-131">The Resource ID of the Instance Failover Group to remove.</span></span>

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

### <span data-ttu-id="c853a-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c853a-132">-Confirm</span></span>
<span data-ttu-id="c853a-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c853a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c853a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c853a-134">-WhatIf</span></span>
<span data-ttu-id="c853a-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c853a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c853a-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c853a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c853a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c853a-137">CommonParameters</span></span>
<span data-ttu-id="c853a-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c853a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c853a-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c853a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c853a-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c853a-140">INPUTS</span></span>

### <span data-ttu-id="c853a-141">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="c853a-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="c853a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c853a-142">System.String</span></span>

## <span data-ttu-id="c853a-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c853a-143">OUTPUTS</span></span>

### <span data-ttu-id="c853a-144">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="c853a-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="c853a-145">Note</span><span class="sxs-lookup"><span data-stu-id="c853a-145">NOTES</span></span>

## <span data-ttu-id="c853a-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c853a-146">RELATED LINKS</span></span>

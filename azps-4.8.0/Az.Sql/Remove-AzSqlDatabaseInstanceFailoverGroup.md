---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 12bc26177a249995f748a879a9ae8d2f73900c99
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189291"
---
# <span data-ttu-id="5def5-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5def5-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="5def5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5def5-102">SYNOPSIS</span></span>
<span data-ttu-id="5def5-103">Rimuove un gruppo di failover delle istanze.</span><span class="sxs-lookup"><span data-stu-id="5def5-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="5def5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5def5-104">SYNTAX</span></span>

### <span data-ttu-id="5def5-105">RemoveIFGDefaultSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5def5-105">RemoveIFGDefaultSet (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5def5-106">RemoveInstanceFailoverGroupByResourceId</span><span class="sxs-lookup"><span data-stu-id="5def5-106">RemoveInstanceFailoverGroupByResourceId</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5def5-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="5def5-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5def5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5def5-108">DESCRIPTION</span></span>
<span data-ttu-id="5def5-109">Questo comando rimuove il gruppo di failover dell'istanza con il nome specificato, lasciando intatti tutti i database.</span><span class="sxs-lookup"><span data-stu-id="5def5-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="5def5-110">L'endpoint del listener verrà annullata la registrazione dal DNS.</span><span class="sxs-lookup"><span data-stu-id="5def5-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="5def5-111">L'area principale del gruppo di failover dell'istanza deve essere usata per eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="5def5-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="5def5-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5def5-112">EXAMPLES</span></span>

### <span data-ttu-id="5def5-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5def5-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="5def5-114">Rimuovere un gruppo di failover delle istanze.</span><span class="sxs-lookup"><span data-stu-id="5def5-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="5def5-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5def5-115">PARAMETERS</span></span>

### <span data-ttu-id="5def5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5def5-116">-DefaultProfile</span></span>
<span data-ttu-id="5def5-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5def5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5def5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5def5-118">-Force</span></span>
<span data-ttu-id="5def5-119">Ignorare il messaggio di conferma per l'esecuzione dell'azione.</span><span class="sxs-lookup"><span data-stu-id="5def5-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="5def5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5def5-120">-InputObject</span></span>
<span data-ttu-id="5def5-121">Oggetto gruppo di failover dell'istanza da rimuovere</span><span class="sxs-lookup"><span data-stu-id="5def5-121">The Instance Failover Group object to remove</span></span>

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

### <span data-ttu-id="5def5-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5def5-122">-Location</span></span>
<span data-ttu-id="5def5-123">Nome dell'area geografica locale da cui recuperare il gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="5def5-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="5def5-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="5def5-124">-Name</span></span>
<span data-ttu-id="5def5-125">Nome del gruppo di failover dell'istanza da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="5def5-125">The name of the Instance Failover Group to remove.</span></span>

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

### <span data-ttu-id="5def5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5def5-126">-PassThru</span></span>
<span data-ttu-id="5def5-127">Specifica se passare all'output di esecuzione del cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5def5-127">Specifies whether to pass through cmdlet execution output.</span></span>

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

### <span data-ttu-id="5def5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5def5-128">-ResourceGroupName</span></span>
<span data-ttu-id="5def5-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5def5-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="5def5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5def5-130">-ResourceId</span></span>
<span data-ttu-id="5def5-131">ID risorsa del gruppo di failover delle istanze da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="5def5-131">The Resource ID of the Instance Failover Group to remove.</span></span>

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

### <span data-ttu-id="5def5-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5def5-132">-Confirm</span></span>
<span data-ttu-id="5def5-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5def5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5def5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5def5-134">-WhatIf</span></span>
<span data-ttu-id="5def5-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5def5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5def5-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5def5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5def5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5def5-137">CommonParameters</span></span>
<span data-ttu-id="5def5-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5def5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5def5-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5def5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5def5-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5def5-140">INPUTS</span></span>

### <span data-ttu-id="5def5-141">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="5def5-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="5def5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5def5-142">System.String</span></span>

## <span data-ttu-id="5def5-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5def5-143">OUTPUTS</span></span>

### <span data-ttu-id="5def5-144">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="5def5-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="5def5-145">Note</span><span class="sxs-lookup"><span data-stu-id="5def5-145">NOTES</span></span>

## <span data-ttu-id="5def5-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5def5-146">RELATED LINKS</span></span>

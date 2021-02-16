---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
ms.openlocfilehash: c57b704f54eacbd9b5cac808e69f9bbf289dc0cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195902"
---
# <span data-ttu-id="3de1f-101">Stop-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="3de1f-101">Stop-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="3de1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3de1f-102">SYNOPSIS</span></span>
<span data-ttu-id="3de1f-103">Interrompe le SQL di un'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="3de1f-103">Stops a SQL managed instance's operations.</span></span>

## <span data-ttu-id="3de1f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3de1f-104">SYNTAX</span></span>

### <span data-ttu-id="3de1f-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3de1f-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (Default)</span></span>
```
Stop-AzSqlInstanceOperation [-Name] <String> [-ManagedInstanceName] <String> [-ResourceGroupName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3de1f-106">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3de1f-106">StopByResourceIdParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3de1f-107">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3de1f-107">StopByInputObjectParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-InputObject] <AzureSqlManagedInstanceOperationModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3de1f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3de1f-108">DESCRIPTION</span></span>
<span data-ttu-id="3de1f-109">Il cmdlet Stop-AzSqlInstanceOperation interrompe l'operazione con il nome dell'operazione fornito in un'SQL gestita.</span><span class="sxs-lookup"><span data-stu-id="3de1f-109">The Stop-AzSqlInstanceOperation cmdlet stops operation with provided operation name on a SQL managed instance.</span></span>

## <span data-ttu-id="3de1f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3de1f-110">EXAMPLES</span></span>

### <span data-ttu-id="3de1f-111">Esempio 1: Ottenere un'operazione specifica</span><span class="sxs-lookup"><span data-stu-id="3de1f-111">Example 1: Get a specific operation</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name d0f5bef5-e2b1-4ef8-bb42-2e54073874f9

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:49:53 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="3de1f-112">Questo comando interrompe l'operazione con il nome 'd0f5bef5-e2b1-4ef8-bb42-2e54073874f9' in un'istanza SQL gestita.</span><span class="sxs-lookup"><span data-stu-id="3de1f-112">This command stops operation with name 'd0f5bef5-e2b1-4ef8-bb42-2e54073874f9' on a SQL managed instance.</span></span>

### <span data-ttu-id="3de1f-113">Esempio 2: Uso dell'ID risorsa dell'operazione</span><span class="sxs-lookup"><span data-stu-id="3de1f-113">Example 2: Using operation resource id</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 4253bf58-34f1-4499-80c6-198d94c659f7
PS C:\> Get-AzSqlInstanceOperation -ResourceId $managedInstanceOperation.Id

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/4253bf58-34f1-4499-80c6-198d94c659f7
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 4253bf58-34f1-4499-80c6-198d94c659f7
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:47:32 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="3de1f-114">Questo comando interrompe l'operazione con ID risorsa $managedInstanceOperation.Id.</span><span class="sxs-lookup"><span data-stu-id="3de1f-114">This command stops operation with resource id $managedInstanceOperation.Id.</span></span>

### <span data-ttu-id="3de1f-115">Esempio 3: Uso dell'oggetto operazione</span><span class="sxs-lookup"><span data-stu-id="3de1f-115">Example 3: Using operation object</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name b15a2b78-c42c-4e00-bf87-7ef4737552dc
PS C:\> Stop-AzSqlInstanceOperation -InputObject $managedInstanceOperation

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/b15a2b78-c42c-4e00-bf87-7ef4737552dc
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : b15a2b78-c42c-4e00-bf87-7ef4737552dc
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:44:57 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="3de1f-116">Questo comando interrompe l'operazione con gli oggetti $managedInstanceOperation.</span><span class="sxs-lookup"><span data-stu-id="3de1f-116">This command stops operation with object $managedInstanceOperation.</span></span>

## <span data-ttu-id="3de1f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3de1f-117">PARAMETERS</span></span>

### <span data-ttu-id="3de1f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3de1f-118">-DefaultProfile</span></span>
<span data-ttu-id="3de1f-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3de1f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3de1f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3de1f-120">-Force</span></span>
<span data-ttu-id="3de1f-121">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="3de1f-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="3de1f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3de1f-122">-InputObject</span></span>
<span data-ttu-id="3de1f-123">Operazione da annullare</span><span class="sxs-lookup"><span data-stu-id="3de1f-123">The operation to cancel</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel
Parameter Sets: StopByInputObjectParameterSet
Aliases: SqlInstanceOperation

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3de1f-124">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="3de1f-124">-ManagedInstanceName</span></span>
<span data-ttu-id="3de1f-125">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="3de1f-125">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de1f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="3de1f-126">-Name</span></span>
<span data-ttu-id="3de1f-127">Nome dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="3de1f-127">The name of the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases: OperationName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de1f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3de1f-128">-ResourceGroupName</span></span>
<span data-ttu-id="3de1f-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3de1f-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3de1f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3de1f-130">-ResourceId</span></span>
<span data-ttu-id="3de1f-131">ID risorsa dell'oggetto operazione da interrompere</span><span class="sxs-lookup"><span data-stu-id="3de1f-131">The resource id of operation object to stop</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3de1f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3de1f-132">-Confirm</span></span>
<span data-ttu-id="3de1f-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3de1f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3de1f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3de1f-134">-WhatIf</span></span>
<span data-ttu-id="3de1f-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3de1f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3de1f-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3de1f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3de1f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3de1f-137">CommonParameters</span></span>
<span data-ttu-id="3de1f-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3de1f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3de1f-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3de1f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3de1f-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="3de1f-140">INPUTS</span></span>

### <span data-ttu-id="3de1f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3de1f-141">System.String</span></span>

### <span data-ttu-id="3de1f-142">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="3de1f-142">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="3de1f-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3de1f-143">OUTPUTS</span></span>

### <span data-ttu-id="3de1f-144">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="3de1f-144">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="3de1f-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="3de1f-145">NOTES</span></span>

## <span data-ttu-id="3de1f-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3de1f-146">RELATED LINKS</span></span>

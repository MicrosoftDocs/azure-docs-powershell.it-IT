---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
ms.openlocfilehash: c57b704f54eacbd9b5cac808e69f9bbf289dc0cc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201747"
---
# <span data-ttu-id="7053b-101">Stop-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="7053b-101">Stop-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="7053b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7053b-102">SYNOPSIS</span></span>
<span data-ttu-id="7053b-103">Interrompe le operazioni di un'istanza di SQL Managed.</span><span class="sxs-lookup"><span data-stu-id="7053b-103">Stops a SQL managed instance's operations.</span></span>

## <span data-ttu-id="7053b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7053b-104">SYNTAX</span></span>

### <span data-ttu-id="7053b-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7053b-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (Default)</span></span>
```
Stop-AzSqlInstanceOperation [-Name] <String> [-ManagedInstanceName] <String> [-ResourceGroupName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7053b-106">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7053b-106">StopByResourceIdParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7053b-107">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7053b-107">StopByInputObjectParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-InputObject] <AzureSqlManagedInstanceOperationModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7053b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7053b-108">DESCRIPTION</span></span>
<span data-ttu-id="7053b-109">Il cmdlet Stop-AzSqlInstanceOperation interrompe l'operazione con il nome dell'operazione specificata in un'istanza di SQL Managed.</span><span class="sxs-lookup"><span data-stu-id="7053b-109">The Stop-AzSqlInstanceOperation cmdlet stops operation with provided operation name on a SQL managed instance.</span></span>

## <span data-ttu-id="7053b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7053b-110">EXAMPLES</span></span>

### <span data-ttu-id="7053b-111">Esempio 1: ottenere un'operazione specifica</span><span class="sxs-lookup"><span data-stu-id="7053b-111">Example 1: Get a specific operation</span></span>
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

<span data-ttu-id="7053b-112">Questo comando interrompe l'operazione con il nome "d0f5bef5-e2b1-4ef8-BB42-2e54073874f9" in un'istanza di SQL Managed.</span><span class="sxs-lookup"><span data-stu-id="7053b-112">This command stops operation with name 'd0f5bef5-e2b1-4ef8-bb42-2e54073874f9' on a SQL managed instance.</span></span>

### <span data-ttu-id="7053b-113">Esempio 2: uso dell'ID risorsa operazione</span><span class="sxs-lookup"><span data-stu-id="7053b-113">Example 2: Using operation resource id</span></span>
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

<span data-ttu-id="7053b-114">Questo comando interrompe l'operazione con ID risorsa $managedInstanceOperation. ID.</span><span class="sxs-lookup"><span data-stu-id="7053b-114">This command stops operation with resource id $managedInstanceOperation.Id.</span></span>

### <span data-ttu-id="7053b-115">Esempio 3: uso dell'oggetto Operation</span><span class="sxs-lookup"><span data-stu-id="7053b-115">Example 3: Using operation object</span></span>
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

<span data-ttu-id="7053b-116">Questo comando interrompe l'operazione con l'oggetto $managedInstanceOperation.</span><span class="sxs-lookup"><span data-stu-id="7053b-116">This command stops operation with object $managedInstanceOperation.</span></span>

## <span data-ttu-id="7053b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7053b-117">PARAMETERS</span></span>

### <span data-ttu-id="7053b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7053b-118">-DefaultProfile</span></span>
<span data-ttu-id="7053b-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7053b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7053b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7053b-120">-Force</span></span>
<span data-ttu-id="7053b-121">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="7053b-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="7053b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7053b-122">-InputObject</span></span>
<span data-ttu-id="7053b-123">Operazione da annullare</span><span class="sxs-lookup"><span data-stu-id="7053b-123">The operation to cancel</span></span>

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

### <span data-ttu-id="7053b-124">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="7053b-124">-ManagedInstanceName</span></span>
<span data-ttu-id="7053b-125">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="7053b-125">The name of the instance.</span></span>

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

### <span data-ttu-id="7053b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="7053b-126">-Name</span></span>
<span data-ttu-id="7053b-127">Nome dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7053b-127">The name of the operation.</span></span>

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

### <span data-ttu-id="7053b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7053b-128">-ResourceGroupName</span></span>
<span data-ttu-id="7053b-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7053b-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="7053b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7053b-130">-ResourceId</span></span>
<span data-ttu-id="7053b-131">ID risorsa dell'oggetto Operation da interrompere</span><span class="sxs-lookup"><span data-stu-id="7053b-131">The resource id of operation object to stop</span></span>

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

### <span data-ttu-id="7053b-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7053b-132">-Confirm</span></span>
<span data-ttu-id="7053b-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7053b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7053b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7053b-134">-WhatIf</span></span>
<span data-ttu-id="7053b-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7053b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7053b-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7053b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7053b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7053b-137">CommonParameters</span></span>
<span data-ttu-id="7053b-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7053b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7053b-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7053b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7053b-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7053b-140">INPUTS</span></span>

### <span data-ttu-id="7053b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7053b-141">System.String</span></span>

### <span data-ttu-id="7053b-142">Microsoft. Azure. Commands. SQL. ManagedInstanceOperation. Model. AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="7053b-142">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="7053b-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7053b-143">OUTPUTS</span></span>

### <span data-ttu-id="7053b-144">Microsoft. Azure. Commands. SQL. ManagedInstanceOperation. Model. AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="7053b-144">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="7053b-145">Note</span><span class="sxs-lookup"><span data-stu-id="7053b-145">NOTES</span></span>

## <span data-ttu-id="7053b-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7053b-146">RELATED LINKS</span></span>

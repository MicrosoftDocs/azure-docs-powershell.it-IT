---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
ms.openlocfilehash: c51ee87ccde0a6be22612033a2fb4c0a4ea3ad2f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999326"
---
# <span data-ttu-id="83412-101">Get-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="83412-101">Get-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="83412-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83412-102">SYNOPSIS</span></span>
<span data-ttu-id="83412-103">Ottiene un SQL le operazioni dell'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="83412-103">Gets a SQL managed instance's operations.</span></span>

## <span data-ttu-id="83412-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83412-104">SYNTAX</span></span>

### <span data-ttu-id="83412-105">DefaultParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="83412-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceOperation [-Name <String>] -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83412-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="83412-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstanceOperation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83412-107">ListByManagedInstanceParameterSet</span><span class="sxs-lookup"><span data-stu-id="83412-107">ListByManagedInstanceParameterSet</span></span>
```
Get-AzSqlInstanceOperation -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83412-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="83412-108">DESCRIPTION</span></span>
<span data-ttu-id="83412-109">Il Get-AzSqlInstanceOperation cmdlet riceve informazioni sulle operazioni in un'SQL gestita.</span><span class="sxs-lookup"><span data-stu-id="83412-109">The Get-AzSqlInstanceOperation cmdlet gets information about the operations on a SQL managed instance.</span></span> <span data-ttu-id="83412-110">È possibile visualizzare tutte le operazioni su un'istanza gestita o un'operazione specifica fornendo il nome dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="83412-110">You can view all operations on a managed instance or view a specific operation by providing the operation name.</span></span>

## <span data-ttu-id="83412-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83412-111">EXAMPLES</span></span>

### <span data-ttu-id="83412-112">Esempio 1: Ottenere tutte le operazioni dell'istanza</span><span class="sxs-lookup"><span data-stu-id="83412-112">Example 1: Get all instance's operations</span></span>
```powershell
PS C:\> Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/79f2c91b-0080-4c14-b9b4-d9991c6e82dd
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 79f2c91b-0080-4c14-b9b4-d9991c6e82dd
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:19:53 AM
State                   : Cancelled
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="83412-113">Questo comando recupera tutte le operazioni come SQL'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="83412-113">This command gets all operations a SQL managed instance.</span></span>

### <span data-ttu-id="83412-114">Esempio 2: Ottenere un'operazione specifica</span><span class="sxs-lookup"><span data-stu-id="83412-114">Example 2: Get a specific operation</span></span>
```powershell
PS C:\> Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 5870c6d8-6703-4b27-8ae4-687b4ca7caea

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="83412-115">Questo comando ottiene l'operazione con il nome '5870c6d8-6703-4b27-8ae4-687b4ca7caea' in un'istanza gestita di SQL.</span><span class="sxs-lookup"><span data-stu-id="83412-115">This command gets operation with name '5870c6d8-6703-4b27-8ae4-687b4ca7caea' on a SQL managed instance.</span></span>

### <span data-ttu-id="83412-116">Esempio 3: Uso dell'ID risorsa dell'operazione</span><span class="sxs-lookup"><span data-stu-id="83412-116">Example 3: Using operation resource id</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 5870c6d8-6703-4b27-8ae4-687b4ca7caea
PS C:\> Get-AzSqlInstanceOperation -ResourceId $managedInstanceOperation.Id

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="83412-117">Questo comando ottiene l'operazione con id '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea'.</span><span class="sxs-lookup"><span data-stu-id="83412-117">This command gets operation with id '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea'.</span></span>

## <span data-ttu-id="83412-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83412-118">PARAMETERS</span></span>

### <span data-ttu-id="83412-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83412-119">-DefaultProfile</span></span>
<span data-ttu-id="83412-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83412-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83412-121">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="83412-121">-ManagedInstanceName</span></span>
<span data-ttu-id="83412-122">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="83412-122">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, ListByManagedInstanceParameterSet
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83412-123">-Name</span><span class="sxs-lookup"><span data-stu-id="83412-123">-Name</span></span>
<span data-ttu-id="83412-124">Nome dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="83412-124">The name of the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: OperationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83412-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83412-125">-ResourceGroupName</span></span>
<span data-ttu-id="83412-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="83412-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, ListByManagedInstanceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83412-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83412-127">-ResourceId</span></span>
<span data-ttu-id="83412-128">Identificatore di risorsa dell'operazione dell'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="83412-128">The managed instance operation resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByManagedInstanceOperationResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83412-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83412-129">CommonParameters</span></span>
<span data-ttu-id="83412-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83412-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83412-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="83412-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83412-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="83412-132">INPUTS</span></span>

### <span data-ttu-id="83412-133">System.String</span><span class="sxs-lookup"><span data-stu-id="83412-133">System.String</span></span>

## <span data-ttu-id="83412-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83412-134">OUTPUTS</span></span>

### <span data-ttu-id="83412-135">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="83412-135">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="83412-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="83412-136">NOTES</span></span>

## <span data-ttu-id="83412-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83412-137">RELATED LINKS</span></span>

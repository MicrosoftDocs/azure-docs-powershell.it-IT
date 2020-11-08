---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
ms.openlocfilehash: a190e6a47c0a3027505c471be870c10ac80593cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191200"
---
# <span data-ttu-id="86f85-101">Get-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="86f85-101">Get-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="86f85-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86f85-102">SYNOPSIS</span></span>
<span data-ttu-id="86f85-103">Ottiene le operazioni di un'istanza di SQL Managed.</span><span class="sxs-lookup"><span data-stu-id="86f85-103">Gets a SQL managed instance's operations.</span></span>

## <span data-ttu-id="86f85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86f85-104">SYNTAX</span></span>

### <span data-ttu-id="86f85-105">DefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="86f85-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceOperation [-Name <String>] -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86f85-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="86f85-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstanceOperation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86f85-107">ListByManagedInstanceParameterSet</span><span class="sxs-lookup"><span data-stu-id="86f85-107">ListByManagedInstanceParameterSet</span></span>
```
Get-AzSqlInstanceOperation -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86f85-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86f85-108">DESCRIPTION</span></span>
<span data-ttu-id="86f85-109">Il cmdlet Get-AzSqlInstanceOperation ottiene informazioni sulle operazioni in un'istanza di SQL Managed.</span><span class="sxs-lookup"><span data-stu-id="86f85-109">The Get-AzSqlInstanceOperation cmdlet gets information about the operations on a SQL managed instance.</span></span> <span data-ttu-id="86f85-110">Puoi visualizzare tutte le operazioni in un'istanza gestita o visualizzare un'operazione specifica fornendo il nome dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="86f85-110">You can view all operations on a managed instance or view a specific operation by providing the operation name.</span></span>

## <span data-ttu-id="86f85-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86f85-111">EXAMPLES</span></span>

### <span data-ttu-id="86f85-112">Esempio 1: ottenere tutte le operazioni dell'istanza</span><span class="sxs-lookup"><span data-stu-id="86f85-112">Example 1: Get all instance's operations</span></span>
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

<span data-ttu-id="86f85-113">Questo comando consente di ottenere tutte le operazioni un'istanza di SQL Managed.</span><span class="sxs-lookup"><span data-stu-id="86f85-113">This command gets all operations a SQL managed instance.</span></span>

### <span data-ttu-id="86f85-114">Esempio 2: ottenere un'operazione specifica</span><span class="sxs-lookup"><span data-stu-id="86f85-114">Example 2: Get a specific operation</span></span>
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

<span data-ttu-id="86f85-115">Questo comando ottiene l'operazione con il nome "5870c6d8-6703-4b27-8ae4-687b4ca7caea" in un'istanza di SQL Managed.</span><span class="sxs-lookup"><span data-stu-id="86f85-115">This command gets operation with name '5870c6d8-6703-4b27-8ae4-687b4ca7caea' on a SQL managed instance.</span></span>

### <span data-ttu-id="86f85-116">Esempio 3: uso dell'ID risorsa operazione</span><span class="sxs-lookup"><span data-stu-id="86f85-116">Example 3: Using operation resource id</span></span>
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

<span data-ttu-id="86f85-117">Questo comando ottiene l'operazione con l'ID '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea '.</span><span class="sxs-lookup"><span data-stu-id="86f85-117">This command gets operation with id '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea'.</span></span>

## <span data-ttu-id="86f85-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86f85-118">PARAMETERS</span></span>

### <span data-ttu-id="86f85-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86f85-119">-DefaultProfile</span></span>
<span data-ttu-id="86f85-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86f85-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86f85-121">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="86f85-121">-ManagedInstanceName</span></span>
<span data-ttu-id="86f85-122">Nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="86f85-122">The name of the instance.</span></span>

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

### <span data-ttu-id="86f85-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="86f85-123">-Name</span></span>
<span data-ttu-id="86f85-124">Nome dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="86f85-124">The name of the operation.</span></span>

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

### <span data-ttu-id="86f85-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86f85-125">-ResourceGroupName</span></span>
<span data-ttu-id="86f85-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="86f85-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="86f85-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86f85-127">-ResourceId</span></span>
<span data-ttu-id="86f85-128">Identificatore della risorsa operazione dell'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="86f85-128">The managed instance operation resource identifier.</span></span>

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

### <span data-ttu-id="86f85-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86f85-129">CommonParameters</span></span>
<span data-ttu-id="86f85-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86f85-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86f85-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86f85-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86f85-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86f85-132">INPUTS</span></span>

### <span data-ttu-id="86f85-133">System. String</span><span class="sxs-lookup"><span data-stu-id="86f85-133">System.String</span></span>

## <span data-ttu-id="86f85-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86f85-134">OUTPUTS</span></span>

### <span data-ttu-id="86f85-135">Microsoft. Azure. Commands. SQL. ManagedInstanceOperation. Model. AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="86f85-135">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="86f85-136">Note</span><span class="sxs-lookup"><span data-stu-id="86f85-136">NOTES</span></span>

## <span data-ttu-id="86f85-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86f85-137">RELATED LINKS</span></span>
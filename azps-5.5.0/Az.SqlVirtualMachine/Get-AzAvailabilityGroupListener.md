---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
ms.openlocfilehash: f1ba6e50c03fffbd4eb6407e90e2a50957806539
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195870"
---
# <span data-ttu-id="e68ad-101">Get-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="e68ad-101">Get-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="e68ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e68ad-102">SYNOPSIS</span></span>
<span data-ttu-id="e68ad-103">Ottenere uno o più ascoltatori del gruppo di disponibilità in un gruppo SQL di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e68ad-103">Get one or more Availability Group Listeners in a SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="e68ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e68ad-104">SYNTAX</span></span>

### <span data-ttu-id="e68ad-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e68ad-105">Name (Default)</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-ResourceGroupName] <String> [-SqlVMGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e68ad-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="e68ad-106">SqlVmGroupObject</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e68ad-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e68ad-107">ResourceId</span></span>
```
Get-AzAvailabilityGroupListener [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e68ad-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e68ad-108">DESCRIPTION</span></span>
<span data-ttu-id="e68ad-109">LGet-AzAvailabilityGroupListener ottiene uno o più listener del gruppo di disponibilità dal SQL di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e68ad-109">The Get-AzAvailabilityGroupListener gets one or more Availability Group Listener from the SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="e68ad-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e68ad-110">EXAMPLES</span></span>

### <span data-ttu-id="e68ad-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e68ad-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="e68ad-112">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="e68ad-112">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="e68ad-113">AgSql01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="e68ad-113">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="e68ad-114">Questo comando ottiene informazioni sull'ascoltatore del gruppo di disponibilità Ag Ag Listener01 nel gruppo di SQL di macchina virtuale SqlVmGroup01 e ResourceGroup01 del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e68ad-114">This command gets information about the Availability Group Listener AgListener01 in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="e68ad-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e68ad-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
```

<span data-ttu-id="e68ad-116">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="e68ad-116">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="e68ad-117">AgSql01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01 AgSql02 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="e68ad-117">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="e68ad-118">Questo comando ottiene informazioni su tutti SQL i listener del gruppo di disponibilità nel gruppo di macchine virtuali SqlVmGroup01 e ResourceGroup01 del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e68ad-118">This command gets information about all Availability Group Listeners in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="e68ad-119">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="e68ad-119">Example 3</span></span>
```powershell
PS C:\> $SqlVmGroupObject = Get-AzSqlVMGroup -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
PS C:\> Get-AzAvailabilityGroupListener -Name AgListener01 -SqlVMGroupObject $SqlVmGroupObject
```

<span data-ttu-id="e68ad-120">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="e68ad-120">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="e68ad-121">AgSql01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="e68ad-121">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

## <span data-ttu-id="e68ad-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e68ad-122">PARAMETERS</span></span>

### <span data-ttu-id="e68ad-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e68ad-123">-DefaultProfile</span></span>
<span data-ttu-id="e68ad-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e68ad-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e68ad-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e68ad-125">-Name</span></span>
<span data-ttu-id="e68ad-126">Nome del listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="e68ad-126">Availability Group Listener name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, SqlVmGroupObject
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e68ad-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e68ad-127">-ResourceGroupName</span></span>
<span data-ttu-id="e68ad-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e68ad-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e68ad-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e68ad-129">-ResourceId</span></span>
<span data-ttu-id="e68ad-130">ID risorsa listener del gruppo di disponibilità</span><span class="sxs-lookup"><span data-stu-id="e68ad-130">Availability Group Listener Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e68ad-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="e68ad-131">-SqlVMGroupName</span></span>
<span data-ttu-id="e68ad-132">SQL del gruppo di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="e68ad-132">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e68ad-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="e68ad-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="e68ad-134">SQL di gruppo di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="e68ad-134">SQL virtual machine Group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: SqlVmGroupObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e68ad-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e68ad-135">CommonParameters</span></span>
<span data-ttu-id="e68ad-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e68ad-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e68ad-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e68ad-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e68ad-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="e68ad-138">INPUTS</span></span>

### <span data-ttu-id="e68ad-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e68ad-139">System.String</span></span>

### <span data-ttu-id="e68ad-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="e68ad-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="e68ad-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e68ad-141">OUTPUTS</span></span>

### <span data-ttu-id="e68ad-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupAmaModel</span><span class="sxs-lookup"><span data-stu-id="e68ad-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="e68ad-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="e68ad-143">NOTES</span></span>

## <span data-ttu-id="e68ad-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e68ad-144">RELATED LINKS</span></span>

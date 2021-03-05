---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/get-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
ms.openlocfilehash: be20b280dccccae6f6afcc1a18514ad3dfb89ba2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008334"
---
# <span data-ttu-id="56ad4-101">Get-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="56ad4-101">Get-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="56ad4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56ad4-102">SYNOPSIS</span></span>
<span data-ttu-id="56ad4-103">Ottenere uno o più ascoltatori del gruppo di disponibilità in un gruppo SQL di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="56ad4-103">Get one or more Availability Group Listeners in a SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="56ad4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56ad4-104">SYNTAX</span></span>

### <span data-ttu-id="56ad4-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="56ad4-105">Name (Default)</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-ResourceGroupName] <String> [-SqlVMGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56ad4-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="56ad4-106">SqlVmGroupObject</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56ad4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="56ad4-107">ResourceId</span></span>
```
Get-AzAvailabilityGroupListener [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56ad4-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="56ad4-108">DESCRIPTION</span></span>
<span data-ttu-id="56ad4-109">LGet-AzAvailabilityGroupListener ottiene uno o più listener del gruppo di disponibilità dal SQL di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="56ad4-109">The Get-AzAvailabilityGroupListener gets one or more Availability Group Listener from the SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="56ad4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56ad4-110">EXAMPLES</span></span>

### <span data-ttu-id="56ad4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="56ad4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="56ad4-112">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="56ad4-112">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="56ad4-113">AgSql01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="56ad4-113">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="56ad4-114">Questo comando ottiene informazioni sull'ascoltatore del gruppo di disponibilità AgNtassi01 nel gruppo di macchine virtuali SqlVmGroup01 e ResourceGroup01 del gruppo di risorse di SQL.</span><span class="sxs-lookup"><span data-stu-id="56ad4-114">This command gets information about the Availability Group Listener AgListener01 in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="56ad4-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="56ad4-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
```

<span data-ttu-id="56ad4-116">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="56ad4-116">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="56ad4-117">AgSql01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01 AgSql02 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="56ad4-117">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="56ad4-118">Questo comando ottiene informazioni su tutti i listener del gruppo di SQL disponibilità nel gruppo di macchine virtuali SqlVmGroup01 e ResourceGroup01 del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="56ad4-118">This command gets information about all Availability Group Listeners in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="56ad4-119">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="56ad4-119">Example 3</span></span>
```powershell
PS C:\> $SqlVmGroupObject = Get-AzSqlVMGroup -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
PS C:\> Get-AzAvailabilityGroupListener -Name AgListener01 -SqlVMGroupObject $SqlVmGroupObject
```

<span data-ttu-id="56ad4-120">Name ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="56ad4-120">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="56ad4-121">AgSql01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="56ad4-121">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

## <span data-ttu-id="56ad4-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56ad4-122">PARAMETERS</span></span>

### <span data-ttu-id="56ad4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56ad4-123">-DefaultProfile</span></span>
<span data-ttu-id="56ad4-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56ad4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56ad4-125">-Name</span><span class="sxs-lookup"><span data-stu-id="56ad4-125">-Name</span></span>
<span data-ttu-id="56ad4-126">Nome del listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="56ad4-126">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="56ad4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56ad4-127">-ResourceGroupName</span></span>
<span data-ttu-id="56ad4-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="56ad4-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="56ad4-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56ad4-129">-ResourceId</span></span>
<span data-ttu-id="56ad4-130">ID risorsa listener del gruppo di disponibilità</span><span class="sxs-lookup"><span data-stu-id="56ad4-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="56ad4-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="56ad4-131">-SqlVMGroupName</span></span>
<span data-ttu-id="56ad4-132">SQL del gruppo di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="56ad4-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="56ad4-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="56ad4-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="56ad4-134">SQL di gruppo di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="56ad4-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="56ad4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56ad4-135">CommonParameters</span></span>
<span data-ttu-id="56ad4-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56ad4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56ad4-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="56ad4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56ad4-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="56ad4-138">INPUTS</span></span>

### <span data-ttu-id="56ad4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="56ad4-139">System.String</span></span>

### <span data-ttu-id="56ad4-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="56ad4-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="56ad4-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56ad4-141">OUTPUTS</span></span>

### <span data-ttu-id="56ad4-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupFalse</span><span class="sxs-lookup"><span data-stu-id="56ad4-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="56ad4-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="56ad4-143">NOTES</span></span>

## <span data-ttu-id="56ad4-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56ad4-144">RELATED LINKS</span></span>

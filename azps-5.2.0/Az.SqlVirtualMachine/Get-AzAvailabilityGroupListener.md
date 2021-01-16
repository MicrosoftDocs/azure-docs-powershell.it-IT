---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azavailabilitygrouplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzAvailabilityGroupListener.md
ms.openlocfilehash: f1ba6e50c03fffbd4eb6407e90e2a50957806539
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364671"
---
# <span data-ttu-id="a4b1e-101">Get-AzAvailabilityGroupListener</span><span class="sxs-lookup"><span data-stu-id="a4b1e-101">Get-AzAvailabilityGroupListener</span></span>

## <span data-ttu-id="a4b1e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4b1e-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b1e-103">Ottenere uno o più listener di gruppi di disponibilità in un gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="a4b1e-103">Get one or more Availability Group Listeners in a SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="a4b1e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4b1e-104">SYNTAX</span></span>

### <span data-ttu-id="a4b1e-105">Nome (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a4b1e-105">Name (Default)</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-ResourceGroupName] <String> [-SqlVMGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4b1e-106">SqlVmGroupObject</span><span class="sxs-lookup"><span data-stu-id="a4b1e-106">SqlVmGroupObject</span></span>
```
Get-AzAvailabilityGroupListener [[-Name] <String>] [-SqlVMGroupObject] <AzureSqlVMGroupModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4b1e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4b1e-107">ResourceId</span></span>
```
Get-AzAvailabilityGroupListener [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4b1e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4b1e-108">DESCRIPTION</span></span>
<span data-ttu-id="a4b1e-109">Il Get-AzAvailabilityGroupListener ottiene uno o più listener del gruppo di disponibilità dal gruppo SQL Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="a4b1e-109">The Get-AzAvailabilityGroupListener gets one or more Availability Group Listener from the SQL Virtual Machine Group.</span></span>

## <span data-ttu-id="a4b1e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4b1e-110">EXAMPLES</span></span>

### <span data-ttu-id="a4b1e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a4b1e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01 -Name AgListener01
```

<span data-ttu-id="a4b1e-112">Nome ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="a4b1e-112">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="a4b1e-113">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="a4b1e-113">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="a4b1e-114">Questo comando consente di ottenere informazioni sul listener del gruppo di disponibilità AgListener01 nel gruppo SqlVmGroup01 e nel gruppo di risorse ResourceGroup01 di SQL Virtual Machine.</span><span class="sxs-lookup"><span data-stu-id="a4b1e-114">This command gets information about the Availability Group Listener AgListener01 in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="a4b1e-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a4b1e-115">Example 2</span></span>
```powershell
PS C:\> Get-AzAvailabilityGroupListener -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
```

<span data-ttu-id="a4b1e-116">Nome ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="a4b1e-116">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="a4b1e-117">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="a4b1e-117">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01 AgListener02 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

<span data-ttu-id="a4b1e-118">Questo comando consente di ottenere informazioni su tutti i listener del gruppo di disponibilità nel gruppo SqlVmGroup01 e nel gruppo di risorse di SQL Virtual Machine ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="a4b1e-118">This command gets information about all Availability Group Listeners in the SQL Virtual Machine Group SqlVmGroup01 and Resource Group ResourceGroup01.</span></span>

### <span data-ttu-id="a4b1e-119">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a4b1e-119">Example 3</span></span>
```powershell
PS C:\> $SqlVmGroupObject = Get-AzSqlVMGroup -ResourceGroupName ResourceGroup01 -SqlVMGroupName SqlVmGroup01
PS C:\> Get-AzAvailabilityGroupListener -Name AgListener01 -SqlVMGroupObject $SqlVmGroupObject
```

<span data-ttu-id="a4b1e-120">Nome ResourceGroupName GroupName AvailabilityGroupName</span><span class="sxs-lookup"><span data-stu-id="a4b1e-120">Name         ResourceGroupName GroupName    AvailabilityGroupName</span></span>
----         ----------------- ---------    ---------------------
<span data-ttu-id="a4b1e-121">AgListener01 ResourceGroup01 SqlVmGroup01 AvailabilityGroup01</span><span class="sxs-lookup"><span data-stu-id="a4b1e-121">AgListener01 ResourceGroup01   SqlVmGroup01 AvailabilityGroup01</span></span>

## <span data-ttu-id="a4b1e-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4b1e-122">PARAMETERS</span></span>

### <span data-ttu-id="a4b1e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b1e-123">-DefaultProfile</span></span>
<span data-ttu-id="a4b1e-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4b1e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4b1e-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4b1e-125">-Name</span></span>
<span data-ttu-id="a4b1e-126">Nome del listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="a4b1e-126">Availability Group Listener name.</span></span>

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

### <span data-ttu-id="a4b1e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4b1e-127">-ResourceGroupName</span></span>
<span data-ttu-id="a4b1e-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a4b1e-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="a4b1e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4b1e-129">-ResourceId</span></span>
<span data-ttu-id="a4b1e-130">ID risorsa listener del gruppo di disponibilità</span><span class="sxs-lookup"><span data-stu-id="a4b1e-130">Availability Group Listener Resource Id</span></span>

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

### <span data-ttu-id="a4b1e-131">-SqlVMGroupName</span><span class="sxs-lookup"><span data-stu-id="a4b1e-131">-SqlVMGroupName</span></span>
<span data-ttu-id="a4b1e-132">Nome del gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="a4b1e-132">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="a4b1e-133">-SqlVMGroupObject</span><span class="sxs-lookup"><span data-stu-id="a4b1e-133">-SqlVMGroupObject</span></span>
<span data-ttu-id="a4b1e-134">Oggetto gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="a4b1e-134">SQL virtual machine Group object.</span></span>

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

### <span data-ttu-id="a4b1e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b1e-135">CommonParameters</span></span>
<span data-ttu-id="a4b1e-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4b1e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b1e-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4b1e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b1e-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4b1e-138">INPUTS</span></span>

### <span data-ttu-id="a4b1e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a4b1e-139">System.String</span></span>

### <span data-ttu-id="a4b1e-140">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="a4b1e-140">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="a4b1e-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4b1e-141">OUTPUTS</span></span>

### <span data-ttu-id="a4b1e-142">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureAvailabilityGroupListenerModel</span><span class="sxs-lookup"><span data-stu-id="a4b1e-142">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureAvailabilityGroupListenerModel</span></span>

## <span data-ttu-id="a4b1e-143">Note</span><span class="sxs-lookup"><span data-stu-id="a4b1e-143">NOTES</span></span>

## <span data-ttu-id="a4b1e-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4b1e-144">RELATED LINKS</span></span>

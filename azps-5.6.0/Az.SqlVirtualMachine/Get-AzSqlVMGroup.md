---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: a7ff8df963f7d1d58256ab40cf5788e81b49a23c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992192"
---
# <span data-ttu-id="9eeb5-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="9eeb5-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="9eeb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9eeb5-102">SYNOPSIS</span></span>
<span data-ttu-id="9eeb5-103">Ottiene uno o più gruppi di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="9eeb5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9eeb5-104">SYNTAX</span></span>

### <span data-ttu-id="9eeb5-105">ResourceGroupOnly (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9eeb5-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9eeb5-106">Nome</span><span class="sxs-lookup"><span data-stu-id="9eeb5-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9eeb5-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9eeb5-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9eeb5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9eeb5-108">DESCRIPTION</span></span>
<span data-ttu-id="9eeb5-109">Il Get-AzSqlVMGroup cmdlet di configurazione ottiene uno o più gruppi di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="9eeb5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9eeb5-110">EXAMPLES</span></span>

### <span data-ttu-id="9eeb5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9eeb5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="9eeb5-112">Questo comando ottiene informazioni su tutti i gruppi di SQL virtuali di Azure nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="9eeb5-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9eeb5-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="9eeb5-114">Questo comando ottiene informazioni su tutti i gruppi di SQL virtuali di Azure nella sottoscrizione corrente assegnata al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="9eeb5-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9eeb5-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="9eeb5-116">Questo comando ottiene informazioni sul gruppo SQL di macchina virtuale "test-group" assegnato al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="9eeb5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9eeb5-117">PARAMETERS</span></span>

### <span data-ttu-id="9eeb5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eeb5-118">-DefaultProfile</span></span>
<span data-ttu-id="9eeb5-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9eeb5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9eeb5-120">-Name</span></span>
<span data-ttu-id="9eeb5-121">SQL del gruppo di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-121">SQL virtual machine group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eeb5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eeb5-122">-ResourceGroupName</span></span>
<span data-ttu-id="9eeb5-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupOnly
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="9eeb5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9eeb5-124">-ResourceId</span></span>
<span data-ttu-id="9eeb5-125">SQL ID risorsa gruppo di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-125">SQL virtual machine group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eeb5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eeb5-126">CommonParameters</span></span>
<span data-ttu-id="9eeb5-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eeb5-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eeb5-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="9eeb5-129">INPUTS</span></span>

### <span data-ttu-id="9eeb5-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9eeb5-130">System.String</span></span>

## <span data-ttu-id="9eeb5-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9eeb5-131">OUTPUTS</span></span>

### <span data-ttu-id="9eeb5-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="9eeb5-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="9eeb5-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="9eeb5-133">NOTES</span></span>

## <span data-ttu-id="9eeb5-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9eeb5-134">RELATED LINKS</span></span>

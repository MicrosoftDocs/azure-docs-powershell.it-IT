---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: fc4a0624b6e5702c0ef0c836f0b6ac593c25dafe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476647"
---
# <span data-ttu-id="6aec3-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="6aec3-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="6aec3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6aec3-102">SYNOPSIS</span></span>
<span data-ttu-id="6aec3-103">Ottiene uno o più gruppi di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="6aec3-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="6aec3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6aec3-104">SYNTAX</span></span>

### <span data-ttu-id="6aec3-105">ResourceGroupOnly (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6aec3-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6aec3-106">Nome</span><span class="sxs-lookup"><span data-stu-id="6aec3-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6aec3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6aec3-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6aec3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6aec3-108">DESCRIPTION</span></span>
<span data-ttu-id="6aec3-109">Il cmdlet Get-AzSqlVMGroup ottiene uno o più gruppi di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="6aec3-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="6aec3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6aec3-110">EXAMPLES</span></span>

### <span data-ttu-id="6aec3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6aec3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="6aec3-112">Questo comando consente di ottenere informazioni su tutti i gruppi di macchine virtuali di Azure SQL nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="6aec3-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="6aec3-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6aec3-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="6aec3-114">Questo comando consente di ottenere informazioni su tutti i gruppi di macchine virtuali di Azure SQL nella sottoscrizione corrente assegnata al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="6aec3-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="6aec3-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6aec3-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="6aec3-116">Questo comando consente di ottenere informazioni sul gruppo "test-Group" della macchina virtuale SQL assegnato al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="6aec3-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="6aec3-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6aec3-117">PARAMETERS</span></span>

### <span data-ttu-id="6aec3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aec3-118">-DefaultProfile</span></span>
<span data-ttu-id="6aec3-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6aec3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aec3-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6aec3-120">-Name</span></span>
<span data-ttu-id="6aec3-121">Nome del gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="6aec3-121">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="6aec3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aec3-122">-ResourceGroupName</span></span>
<span data-ttu-id="6aec3-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6aec3-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="6aec3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6aec3-124">-ResourceId</span></span>
<span data-ttu-id="6aec3-125">ID risorsa di gruppo della macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="6aec3-125">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="6aec3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aec3-126">CommonParameters</span></span>
<span data-ttu-id="6aec3-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aec3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aec3-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6aec3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aec3-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6aec3-129">INPUTS</span></span>

### <span data-ttu-id="6aec3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6aec3-130">System.String</span></span>

## <span data-ttu-id="6aec3-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6aec3-131">OUTPUTS</span></span>

### <span data-ttu-id="6aec3-132">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="6aec3-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="6aec3-133">Note</span><span class="sxs-lookup"><span data-stu-id="6aec3-133">NOTES</span></span>

## <span data-ttu-id="6aec3-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6aec3-134">RELATED LINKS</span></span>

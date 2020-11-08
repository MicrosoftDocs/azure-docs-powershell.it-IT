---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvmgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVMGroup.md
ms.openlocfilehash: fc4a0624b6e5702c0ef0c836f0b6ac593c25dafe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191801"
---
# <span data-ttu-id="8ba09-101">Get-AzSqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="8ba09-101">Get-AzSqlVMGroup</span></span>

## <span data-ttu-id="8ba09-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8ba09-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba09-103">Ottiene uno o più gruppi di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="8ba09-103">Gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="8ba09-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ba09-104">SYNTAX</span></span>

### <span data-ttu-id="8ba09-105">ResourceGroupOnly (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8ba09-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVMGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ba09-106">Nome</span><span class="sxs-lookup"><span data-stu-id="8ba09-106">Name</span></span>
```
Get-AzSqlVMGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ba09-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ba09-107">ResourceId</span></span>
```
Get-AzSqlVMGroup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ba09-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ba09-108">DESCRIPTION</span></span>
<span data-ttu-id="8ba09-109">Il cmdlet Get-AzSqlVMGroup ottiene uno o più gruppi di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="8ba09-109">The Get-AzSqlVMGroup cmdlet gets one or more sql virtual machine groups.</span></span>

## <span data-ttu-id="8ba09-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ba09-110">EXAMPLES</span></span>

### <span data-ttu-id="8ba09-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8ba09-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup

Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
group1     ResourceGroup02    Developer SQL2017-WS2016
```

<span data-ttu-id="8ba09-112">Questo comando consente di ottenere informazioni su tutti i gruppi di macchine virtuali di Azure SQL nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="8ba09-112">This command gets information about all the Azure SQL virtual machine groups in the current subscription.</span></span>

### <span data-ttu-id="8ba09-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8ba09-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="8ba09-114">Questo comando consente di ottenere informazioni su tutti i gruppi di macchine virtuali di Azure SQL nella sottoscrizione corrente assegnata al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="8ba09-114">This command gets information about all the Azure SQL virtual machine groups in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="8ba09-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="8ba09-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVMGroup -ResourceGroupName "ResourceGroup01" -Name "test-group"
Name       ResourceGroupName  Sku       Offer
----       -----------------  ---       -----
test-group ResourceGroup01    Developer SQL2017-WS2016
```

<span data-ttu-id="8ba09-116">Questo comando consente di ottenere informazioni sul gruppo "test-Group" della macchina virtuale SQL assegnato al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="8ba09-116">This command gets information about the SQL virtual machine group "test-group" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="8ba09-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8ba09-117">PARAMETERS</span></span>

### <span data-ttu-id="8ba09-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba09-118">-DefaultProfile</span></span>
<span data-ttu-id="8ba09-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8ba09-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ba09-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ba09-120">-Name</span></span>
<span data-ttu-id="8ba09-121">Nome del gruppo di macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="8ba09-121">SQL virtual machine group name.</span></span>

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

### <span data-ttu-id="8ba09-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ba09-122">-ResourceGroupName</span></span>
<span data-ttu-id="8ba09-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8ba09-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="8ba09-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ba09-124">-ResourceId</span></span>
<span data-ttu-id="8ba09-125">ID risorsa di gruppo della macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="8ba09-125">SQL virtual machine group resource id.</span></span>

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

### <span data-ttu-id="8ba09-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba09-126">CommonParameters</span></span>
<span data-ttu-id="8ba09-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ba09-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba09-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ba09-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba09-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8ba09-129">INPUTS</span></span>

### <span data-ttu-id="8ba09-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8ba09-130">System.String</span></span>

## <span data-ttu-id="8ba09-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ba09-131">OUTPUTS</span></span>

### <span data-ttu-id="8ba09-132">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMGroupModel</span><span class="sxs-lookup"><span data-stu-id="8ba09-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel</span></span>

## <span data-ttu-id="8ba09-133">Note</span><span class="sxs-lookup"><span data-stu-id="8ba09-133">NOTES</span></span>

## <span data-ttu-id="8ba09-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ba09-134">RELATED LINKS</span></span>
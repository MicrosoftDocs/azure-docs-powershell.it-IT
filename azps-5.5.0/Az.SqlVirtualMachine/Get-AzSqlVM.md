---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
ms.openlocfilehash: b6f5b885e2cb65c8cf4775f8bb37742b8d98b6a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209147"
---
# <span data-ttu-id="379a2-101">Get-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="379a2-101">Get-AzSqlVM</span></span>

## <span data-ttu-id="379a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="379a2-102">SYNOPSIS</span></span>
<span data-ttu-id="379a2-103">Ottiene una o più macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="379a2-103">Gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="379a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="379a2-104">SYNTAX</span></span>

### <span data-ttu-id="379a2-105">ResourceGroupOnly (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="379a2-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVM [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="379a2-106">Nome</span><span class="sxs-lookup"><span data-stu-id="379a2-106">Name</span></span>
```
Get-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="379a2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="379a2-107">ResourceId</span></span>
```
Get-AzSqlVM [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="379a2-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="379a2-108">DESCRIPTION</span></span>
<span data-ttu-id="379a2-109">Il cmdlet Get-AzSqlVM cmdlet ottiene una o più macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="379a2-109">The Get-AzSqlVM cmdlet gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="379a2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="379a2-110">EXAMPLES</span></span>

### <span data-ttu-id="379a2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="379a2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVM

Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
vm2  ResourceGroup02    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="379a2-112">Questo comando ottiene informazioni su tutte le macchine SQL azure SQL nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="379a2-112">This command gets information about all the Azure SQL virtual machines in the current subscription.</span></span>

### <span data-ttu-id="379a2-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="379a2-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="379a2-114">Questo comando ottiene informazioni su tutte le macchine virtuali SQL azure nella sottoscrizione corrente assegnata al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="379a2-114">This command gets information about all the Azure SQL virtual machines in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="379a2-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="379a2-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="379a2-116">Questo comando ottiene informazioni sulla macchina SQL "vm" assegnata al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="379a2-116">This command gets information about the SQL virtual machine "vm" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="379a2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="379a2-117">PARAMETERS</span></span>

### <span data-ttu-id="379a2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="379a2-118">-DefaultProfile</span></span>
<span data-ttu-id="379a2-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="379a2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="379a2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="379a2-120">-Name</span></span>
<span data-ttu-id="379a2-121">SQL nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="379a2-121">SQL virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: SqlVMName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="379a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="379a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="379a2-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="379a2-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="379a2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="379a2-124">-ResourceId</span></span>
<span data-ttu-id="379a2-125">SQL ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="379a2-125">SQL virtual machine resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: SqlVMId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="379a2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="379a2-126">CommonParameters</span></span>
<span data-ttu-id="379a2-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="379a2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="379a2-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="379a2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="379a2-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="379a2-129">INPUTS</span></span>

### <span data-ttu-id="379a2-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="379a2-130">None</span></span>

## <span data-ttu-id="379a2-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="379a2-131">OUTPUTS</span></span>

### <span data-ttu-id="379a2-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="379a2-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="379a2-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="379a2-133">NOTES</span></span>

## <span data-ttu-id="379a2-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="379a2-134">RELATED LINKS</span></span>

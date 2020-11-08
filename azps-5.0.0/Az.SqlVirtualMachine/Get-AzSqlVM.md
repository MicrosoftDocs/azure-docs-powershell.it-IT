---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/get-azsqlvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Get-AzSqlVM.md
ms.openlocfilehash: b6f5b885e2cb65c8cf4775f8bb37742b8d98b6a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202240"
---
# <span data-ttu-id="4c316-101">Get-AzSqlVM</span><span class="sxs-lookup"><span data-stu-id="4c316-101">Get-AzSqlVM</span></span>

## <span data-ttu-id="4c316-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4c316-102">SYNOPSIS</span></span>
<span data-ttu-id="4c316-103">Ottiene una o più macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="4c316-103">Gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="4c316-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c316-104">SYNTAX</span></span>

### <span data-ttu-id="4c316-105">ResourceGroupOnly (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4c316-105">ResourceGroupOnly (Default)</span></span>
```
Get-AzSqlVM [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c316-106">Nome</span><span class="sxs-lookup"><span data-stu-id="4c316-106">Name</span></span>
```
Get-AzSqlVM [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c316-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c316-107">ResourceId</span></span>
```
Get-AzSqlVM [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c316-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c316-108">DESCRIPTION</span></span>
<span data-ttu-id="4c316-109">Il cmdlet Get-AzSqlVM ottiene una o più macchine virtuali SQL.</span><span class="sxs-lookup"><span data-stu-id="4c316-109">The Get-AzSqlVM cmdlet gets one or more sql virtual machines.</span></span>

## <span data-ttu-id="4c316-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c316-110">EXAMPLES</span></span>

### <span data-ttu-id="4c316-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4c316-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlVM

Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
vm2  ResourceGroup02    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="4c316-112">Questo comando consente di ottenere informazioni su tutte le macchine virtuali di Azure SQL nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="4c316-112">This command gets information about all the Azure SQL virtual machines in the current subscription.</span></span>

### <span data-ttu-id="4c316-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4c316-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="4c316-114">Questo comando consente di ottenere informazioni su tutte le macchine virtuali di Azure SQL nella sottoscrizione corrente assegnata al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="4c316-114">This command gets information about all the Azure SQL virtual machines in the current subscription assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="4c316-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="4c316-115">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm"
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="4c316-116">Questo comando consente di ottenere informazioni sulla macchina virtuale SQL "VM" assegnata al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="4c316-116">This command gets information about the SQL virtual machine "vm" assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="4c316-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4c316-117">PARAMETERS</span></span>

### <span data-ttu-id="4c316-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c316-118">-DefaultProfile</span></span>
<span data-ttu-id="4c316-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c316-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c316-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c316-120">-Name</span></span>
<span data-ttu-id="4c316-121">Nome macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="4c316-121">SQL virtual machine name.</span></span>

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

### <span data-ttu-id="4c316-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c316-122">-ResourceGroupName</span></span>
<span data-ttu-id="4c316-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4c316-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="4c316-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c316-124">-ResourceId</span></span>
<span data-ttu-id="4c316-125">ID risorsa macchina virtuale SQL.</span><span class="sxs-lookup"><span data-stu-id="4c316-125">SQL virtual machine resource id.</span></span>

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

### <span data-ttu-id="4c316-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c316-126">CommonParameters</span></span>
<span data-ttu-id="4c316-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c316-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c316-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c316-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c316-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4c316-129">INPUTS</span></span>

### <span data-ttu-id="4c316-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4c316-130">None</span></span>

## <span data-ttu-id="4c316-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c316-131">OUTPUTS</span></span>

### <span data-ttu-id="4c316-132">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. Model. AzureSqlVMModel</span><span class="sxs-lookup"><span data-stu-id="4c316-132">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="4c316-133">Note</span><span class="sxs-lookup"><span data-stu-id="4c316-133">NOTES</span></span>

## <span data-ttu-id="4c316-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c316-134">RELATED LINKS</span></span>

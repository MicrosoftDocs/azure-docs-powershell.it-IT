---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
ms.openlocfilehash: 7903e13abf7e924898910ad007eefcf6800dcc61
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195038"
---
# <span data-ttu-id="efe7e-101">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="efe7e-101">Get-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="efe7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efe7e-102">SYNOPSIS</span></span>
<span data-ttu-id="efe7e-103">Ottiene le impostazioni per un'estensione SQL Server in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="efe7e-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="efe7e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="efe7e-104">SYNTAX</span></span>

```
Get-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efe7e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="efe7e-105">DESCRIPTION</span></span>
<span data-ttu-id="efe7e-106">Il cmdlet **Get-AzVMSqlServerExtension** ottiene le impostazioni dell'infrastruttura di SQL Server come agente di servizio (IaaS) in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="efe7e-106">The **Get-AzVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="efe7e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="efe7e-107">EXAMPLES</span></span>

### <span data-ttu-id="efe7e-108">Esempio 1: Ottenere le impostazioni di un'estensione SQL Server in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="efe7e-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="efe7e-109">Questo comando recupera le impostazioni dell'estensione SQL Server in una macchina virtuale denominata ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="efe7e-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="efe7e-110">Esempio 2: Ottenere le impostazioni usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="efe7e-110">Example 2: Get the settings by using the pipeline</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service08" -Name "ContosoVM22" | Get-AzVMSqlServerExtension
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="efe7e-111">Questo comando recupera la macchina virtuale denominata ContosoVM22 nel servizio Service08 usando il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="efe7e-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="efe7e-112">Il comando passa i risultati al cmdlet corrente usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="efe7e-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="efe7e-113">Il comando corrente ottiene le impostazioni dell'SQL Server'agente IaaS nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="efe7e-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="efe7e-114">Esempio 3: Ottenere le impostazioni di una versione SQL Server specifica</span><span class="sxs-lookup"><span data-stu-id="efe7e-114">Example 3: Get the settings of specific SQL Server version</span></span>
```
PS C:\> Get-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07" -Version "1.0"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="efe7e-115">Questo comando recupera le impostazioni della versione 1.0 dell'estensione SQL Server in una macchina virtuale denominata ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="efe7e-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="efe7e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efe7e-116">PARAMETERS</span></span>

### <span data-ttu-id="efe7e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efe7e-117">-DefaultProfile</span></span>
<span data-ttu-id="efe7e-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="efe7e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efe7e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="efe7e-119">-Name</span></span>
<span data-ttu-id="efe7e-120">Specifica il nome della SQL Server'estensione.</span><span class="sxs-lookup"><span data-stu-id="efe7e-120">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efe7e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efe7e-121">-ResourceGroupName</span></span>
<span data-ttu-id="efe7e-122">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="efe7e-122">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efe7e-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="efe7e-123">-VMName</span></span>
<span data-ttu-id="efe7e-124">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="efe7e-124">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efe7e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efe7e-125">CommonParameters</span></span>
<span data-ttu-id="efe7e-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efe7e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efe7e-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="efe7e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efe7e-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="efe7e-128">INPUTS</span></span>

### <span data-ttu-id="efe7e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="efe7e-129">System.String</span></span>

## <span data-ttu-id="efe7e-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="efe7e-130">OUTPUTS</span></span>

### <span data-ttu-id="efe7e-131">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span><span class="sxs-lookup"><span data-stu-id="efe7e-131">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="efe7e-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="efe7e-132">NOTES</span></span>

## <span data-ttu-id="efe7e-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="efe7e-133">RELATED LINKS</span></span>

[<span data-ttu-id="efe7e-134">Get-AZVM</span><span class="sxs-lookup"><span data-stu-id="efe7e-134">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="efe7e-135">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="efe7e-135">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="efe7e-136">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="efe7e-136">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)



---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsqlserverextension
schema: 2.0.0
ms.openlocfilehash: 6b02a83c7664fa460cd4ebd25a1754a8bc57e784
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867157"
---
# <span data-ttu-id="81303-101">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="81303-101">Get-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="81303-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="81303-102">SYNOPSIS</span></span>
<span data-ttu-id="81303-103">Ottiene le impostazioni per un'estensione di SQL Server in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="81303-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81303-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81303-104">SYNTAX</span></span>

```
Get-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81303-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81303-105">DESCRIPTION</span></span>
<span data-ttu-id="81303-106">Il cmdlet **Get-AzureRmVMSqlServerExtension** ottiene le impostazioni dell'agente di SQL Server come servizio (IaaS) in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="81303-106">The **Get-AzureRmVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="81303-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81303-107">EXAMPLES</span></span>

### <span data-ttu-id="81303-108">Esempio 1: ottenere le impostazioni di un'estensione di SQL Server in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="81303-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="81303-109">Questo comando consente di ottenere le impostazioni dell'estensione di SQL Server in una macchina virtuale denominata ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="81303-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="81303-110">Esempio 2: ottenere le impostazioni usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="81303-110">Example 2: Get the settings by using the pipeline</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service08" -Name "ContosoVM22" | Get-AzureRmVMSqlServerExtension
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="81303-111">Questo comando consente di ottenere la macchina virtuale denominata ContosoVM22 nel servizio Service08 usando il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="81303-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="81303-112">Il comando passa i risultati al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="81303-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="81303-113">Il comando corrente ottiene le impostazioni dell'agente IaaS di SQL Server nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="81303-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="81303-114">Esempio 3: ottenere le impostazioni di una versione specifica di SQL Server</span><span class="sxs-lookup"><span data-stu-id="81303-114">Example 3: Get the settings of specific SQL Server version</span></span>
```
PS C:\> Get-AzureRmVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07" -Version "1.0"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="81303-115">Questo comando consente di ottenere le impostazioni della versione 1,0 dell'estensione di SQL Server in una macchina virtuale denominata ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="81303-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="81303-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81303-116">PARAMETERS</span></span>

### <span data-ttu-id="81303-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81303-117">-DefaultProfile</span></span>
<span data-ttu-id="81303-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81303-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81303-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="81303-119">-Name</span></span>
<span data-ttu-id="81303-120">Specifica il nome dell'estensione di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="81303-120">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81303-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81303-121">-ResourceGroupName</span></span>
<span data-ttu-id="81303-122">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="81303-122">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81303-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="81303-123">-VMName</span></span>
<span data-ttu-id="81303-124">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="81303-124">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81303-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81303-125">CommonParameters</span></span>
<span data-ttu-id="81303-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81303-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81303-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81303-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81303-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="81303-128">INPUTS</span></span>

### <span data-ttu-id="81303-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="81303-129">None</span></span>
<span data-ttu-id="81303-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="81303-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="81303-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81303-131">OUTPUTS</span></span>

### <span data-ttu-id="81303-132">Microsoft. Azure. Commands. Compute. VirtualMachineSqlServerExtensionContext</span><span class="sxs-lookup"><span data-stu-id="81303-132">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="81303-133">Note</span><span class="sxs-lookup"><span data-stu-id="81303-133">NOTES</span></span>

## <span data-ttu-id="81303-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81303-134">RELATED LINKS</span></span>

[<span data-ttu-id="81303-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="81303-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="81303-136">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="81303-136">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="81303-137">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="81303-137">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)



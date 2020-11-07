---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
ms.openlocfilehash: a3570a65e5c4f6aa305c4123188d094d9bd4545c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863718"
---
# <span data-ttu-id="26aa9-101">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="26aa9-101">Get-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="26aa9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26aa9-102">SYNOPSIS</span></span>
<span data-ttu-id="26aa9-103">Ottiene le impostazioni per un'estensione di SQL Server in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="26aa9-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="26aa9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26aa9-104">SYNTAX</span></span>

```
Get-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26aa9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26aa9-105">DESCRIPTION</span></span>
<span data-ttu-id="26aa9-106">Il cmdlet **Get-AzVMSqlServerExtension** ottiene le impostazioni dell'agente di SQL Server come servizio (IaaS) in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="26aa9-106">The **Get-AzVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="26aa9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26aa9-107">EXAMPLES</span></span>

### <span data-ttu-id="26aa9-108">Esempio 1: ottenere le impostazioni di un'estensione di SQL Server in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="26aa9-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
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

<span data-ttu-id="26aa9-109">Questo comando consente di ottenere le impostazioni dell'estensione di SQL Server in una macchina virtuale denominata ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="26aa9-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="26aa9-110">Esempio 2: ottenere le impostazioni usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="26aa9-110">Example 2: Get the settings by using the pipeline</span></span>
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

<span data-ttu-id="26aa9-111">Questo comando consente di ottenere la macchina virtuale denominata ContosoVM22 nel servizio Service08 usando il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="26aa9-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="26aa9-112">Il comando passa i risultati al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="26aa9-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="26aa9-113">Il comando corrente ottiene le impostazioni dell'agente IaaS di SQL Server nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="26aa9-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="26aa9-114">Esempio 3: ottenere le impostazioni di una versione specifica di SQL Server</span><span class="sxs-lookup"><span data-stu-id="26aa9-114">Example 3: Get the settings of specific SQL Server version</span></span>
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

<span data-ttu-id="26aa9-115">Questo comando consente di ottenere le impostazioni della versione 1,0 dell'estensione di SQL Server in una macchina virtuale denominata ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="26aa9-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="26aa9-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26aa9-116">PARAMETERS</span></span>

### <span data-ttu-id="26aa9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26aa9-117">-DefaultProfile</span></span>
<span data-ttu-id="26aa9-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26aa9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26aa9-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="26aa9-119">-Name</span></span>
<span data-ttu-id="26aa9-120">Specifica il nome dell'estensione di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="26aa9-120">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="26aa9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26aa9-121">-ResourceGroupName</span></span>
<span data-ttu-id="26aa9-122">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="26aa9-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="26aa9-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="26aa9-123">-VMName</span></span>
<span data-ttu-id="26aa9-124">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="26aa9-124">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="26aa9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26aa9-125">CommonParameters</span></span>
<span data-ttu-id="26aa9-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26aa9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26aa9-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26aa9-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26aa9-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26aa9-128">INPUTS</span></span>

### <span data-ttu-id="26aa9-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="26aa9-129">None</span></span>
<span data-ttu-id="26aa9-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="26aa9-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="26aa9-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26aa9-131">OUTPUTS</span></span>

### <span data-ttu-id="26aa9-132">Microsoft. Azure. Commands. Compute. VirtualMachineSqlServerExtensionContext</span><span class="sxs-lookup"><span data-stu-id="26aa9-132">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="26aa9-133">Note</span><span class="sxs-lookup"><span data-stu-id="26aa9-133">NOTES</span></span>

## <span data-ttu-id="26aa9-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26aa9-134">RELATED LINKS</span></span>

[<span data-ttu-id="26aa9-135">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="26aa9-135">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="26aa9-136">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="26aa9-136">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="26aa9-137">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="26aa9-137">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)



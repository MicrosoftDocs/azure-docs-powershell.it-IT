---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: a6f2ed82835cca252f905cb53c5ddd9c8530900a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521091"
---
# <span data-ttu-id="b8510-101">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b8510-101">Get-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="b8510-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b8510-102">SYNOPSIS</span></span>
<span data-ttu-id="b8510-103">Ottiene le impostazioni per un'estensione di SQL Server in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b8510-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8510-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b8510-104">SYNTAX</span></span>

```
Get-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8510-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8510-105">DESCRIPTION</span></span>
<span data-ttu-id="b8510-106">Il cmdlet **Get-AzureRmVMSqlServerExtension** ottiene le impostazioni dell'agente di SQL Server come servizio (IaaS) in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b8510-106">The **Get-AzureRmVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="b8510-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b8510-107">EXAMPLES</span></span>

### <span data-ttu-id="b8510-108">Esempio 1: ottenere le impostazioni di un'estensione di SQL Server in una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="b8510-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
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

<span data-ttu-id="b8510-109">Questo comando consente di ottenere le impostazioni dell'estensione di SQL Server in una macchina virtuale denominata ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="b8510-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="b8510-110">Esempio 2: ottenere le impostazioni usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="b8510-110">Example 2: Get the settings by using the pipeline</span></span>
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

<span data-ttu-id="b8510-111">Questo comando consente di ottenere la macchina virtuale denominata ContosoVM22 nel servizio Service08 usando il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="b8510-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="b8510-112">Il comando passa i risultati al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="b8510-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="b8510-113">Il comando corrente ottiene le impostazioni dell'agente IaaS di SQL Server nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b8510-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="b8510-114">Esempio 3: ottenere le impostazioni di una versione specifica di SQL Server</span><span class="sxs-lookup"><span data-stu-id="b8510-114">Example 3: Get the settings of specific SQL Server version</span></span>
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

<span data-ttu-id="b8510-115">Questo comando consente di ottenere le impostazioni della versione 1,0 dell'estensione di SQL Server in una macchina virtuale denominata ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="b8510-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="b8510-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b8510-116">PARAMETERS</span></span>

### <span data-ttu-id="b8510-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8510-117">-Name</span></span>
<span data-ttu-id="b8510-118">Specifica il nome dell'estensione di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b8510-118">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="b8510-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8510-119">-ResourceGroupName</span></span>
<span data-ttu-id="b8510-120">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b8510-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b8510-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="b8510-121">-VMName</span></span>
<span data-ttu-id="b8510-122">Specifica il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b8510-122">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="b8510-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8510-123">CommonParameters</span></span>
<span data-ttu-id="b8510-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8510-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8510-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8510-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8510-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b8510-126">INPUTS</span></span>

### <span data-ttu-id="b8510-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b8510-127">None</span></span>
<span data-ttu-id="b8510-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b8510-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b8510-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b8510-129">OUTPUTS</span></span>

## <span data-ttu-id="b8510-130">Note</span><span class="sxs-lookup"><span data-stu-id="b8510-130">NOTES</span></span>

## <span data-ttu-id="b8510-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b8510-131">RELATED LINKS</span></span>

[<span data-ttu-id="b8510-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b8510-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="b8510-133">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b8510-133">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="b8510-134">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b8510-134">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: ee210b5b9408f3de2b9e92213fafe4846ea8c3e1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407098"
---
# <span data-ttu-id="506d5-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="506d5-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="506d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="506d5-102">SYNOPSIS</span></span>
<span data-ttu-id="506d5-103">Recupera i dati di diagnostica di avvio per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="506d5-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="506d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="506d5-104">SYNTAX</span></span>

### <span data-ttu-id="506d5-105">WindowsParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="506d5-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows] [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="506d5-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="506d5-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux] [[-LocalPath] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="506d5-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="506d5-107">DESCRIPTION</span></span>
<span data-ttu-id="506d5-108">Il cmdlet **Get-AzVMBootDiagnosticsData** ottiene i dati di diagnostica di avvio per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="506d5-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="506d5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="506d5-109">EXAMPLES</span></span>

### <span data-ttu-id="506d5-110">Esempio 1: Ottenere i dati di diagnostica di avvio</span><span class="sxs-lookup"><span data-stu-id="506d5-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="506d5-111">Questo comando recupera i dati di diagnostica di avvio per la macchina virtuale ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="506d5-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="506d5-112">Questa macchina virtuale esegue il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="506d5-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="506d5-113">Il comando archivia i dati nel percorso locale specificato.</span><span class="sxs-lookup"><span data-stu-id="506d5-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="506d5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="506d5-114">PARAMETERS</span></span>

### <span data-ttu-id="506d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="506d5-115">-DefaultProfile</span></span>
<span data-ttu-id="506d5-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="506d5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="506d5-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="506d5-117">-Linux</span></span>
<span data-ttu-id="506d5-118">Indica che la macchina virtuale esegue il sistema operativo Linux.</span><span class="sxs-lookup"><span data-stu-id="506d5-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="506d5-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="506d5-119">-LocalPath</span></span>
<span data-ttu-id="506d5-120">Specifica il percorso locale per i dati di diagnostica di avvio.</span><span class="sxs-lookup"><span data-stu-id="506d5-120">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsParamSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: LinuxParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="506d5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="506d5-121">-Name</span></span>
<span data-ttu-id="506d5-122">Specifica il nome della macchina virtuale per cui il cmdlet riceve i dati di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="506d5-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="506d5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="506d5-123">-ResourceGroupName</span></span>
<span data-ttu-id="506d5-124">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="506d5-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="506d5-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="506d5-125">-Windows</span></span>
<span data-ttu-id="506d5-126">Indica che la macchina virtuale esegue il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="506d5-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="506d5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="506d5-127">CommonParameters</span></span>
<span data-ttu-id="506d5-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="506d5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="506d5-129">Per altre informazioni, [vedere](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="506d5-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="506d5-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="506d5-130">INPUTS</span></span>

### <span data-ttu-id="506d5-131">System.String</span><span class="sxs-lookup"><span data-stu-id="506d5-131">System.String</span></span>

## <span data-ttu-id="506d5-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="506d5-132">OUTPUTS</span></span>

### <span data-ttu-id="506d5-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="506d5-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="506d5-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="506d5-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="506d5-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="506d5-135">NOTES</span></span>

## <span data-ttu-id="506d5-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="506d5-136">RELATED LINKS</span></span>

[<span data-ttu-id="506d5-137">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="506d5-137">Set-AzVMBootDiagnostic</span></span>](./Set-AzVMBootDiagnostic.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: 96248492feac9997d1afdba83fdda943c75fa363
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031895"
---
# <span data-ttu-id="00bb2-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="00bb2-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="00bb2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="00bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="00bb2-103">Ottiene i dati di diagnostica di avvio per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="00bb2-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="00bb2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00bb2-104">SYNTAX</span></span>

### <span data-ttu-id="00bb2-105">WindowsParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="00bb2-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows] [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00bb2-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="00bb2-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux] [[-LocalPath] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00bb2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00bb2-107">DESCRIPTION</span></span>
<span data-ttu-id="00bb2-108">Il cmdlet **Get-AzVMBootDiagnosticsData** ottiene i dati di diagnostica di avvio per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="00bb2-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="00bb2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00bb2-109">EXAMPLES</span></span>

### <span data-ttu-id="00bb2-110">Esempio 1: ottenere i dati di diagnostica di avvio</span><span class="sxs-lookup"><span data-stu-id="00bb2-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="00bb2-111">Questo comando consente di ottenere i dati di diagnostica di avvio per la macchina virtuale denominata ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="00bb2-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="00bb2-112">Questa macchina virtuale esegue il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="00bb2-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="00bb2-113">Il comando Archivia i dati in un percorso locale specificato.</span><span class="sxs-lookup"><span data-stu-id="00bb2-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="00bb2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="00bb2-114">PARAMETERS</span></span>

### <span data-ttu-id="00bb2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00bb2-115">-DefaultProfile</span></span>
<span data-ttu-id="00bb2-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="00bb2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00bb2-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="00bb2-117">-Linux</span></span>
<span data-ttu-id="00bb2-118">Indica che la macchina virtuale esegue il sistema operativo Linux.</span><span class="sxs-lookup"><span data-stu-id="00bb2-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="00bb2-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="00bb2-119">-LocalPath</span></span>
<span data-ttu-id="00bb2-120">Specifica il percorso locale per i dati di diagnostica di avvio.</span><span class="sxs-lookup"><span data-stu-id="00bb2-120">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="00bb2-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="00bb2-121">-Name</span></span>
<span data-ttu-id="00bb2-122">Specifica il nome della macchina virtuale per cui questo cmdlet ottiene i dati di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="00bb2-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="00bb2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00bb2-123">-ResourceGroupName</span></span>
<span data-ttu-id="00bb2-124">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="00bb2-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="00bb2-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="00bb2-125">-Windows</span></span>
<span data-ttu-id="00bb2-126">Indica che la macchina virtuale esegue il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="00bb2-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="00bb2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00bb2-127">CommonParameters</span></span>
<span data-ttu-id="00bb2-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00bb2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00bb2-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00bb2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00bb2-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="00bb2-130">INPUTS</span></span>

### <span data-ttu-id="00bb2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="00bb2-131">System.String</span></span>

## <span data-ttu-id="00bb2-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00bb2-132">OUTPUTS</span></span>

### <span data-ttu-id="00bb2-133">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="00bb2-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="00bb2-134">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="00bb2-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="00bb2-135">Note</span><span class="sxs-lookup"><span data-stu-id="00bb2-135">NOTES</span></span>

## <span data-ttu-id="00bb2-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00bb2-136">RELATED LINKS</span></span>

[<span data-ttu-id="00bb2-137">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="00bb2-137">Set-AzVMBootDiagnostic</span></span>](./Set-AzVMBootDiagnostic.md)



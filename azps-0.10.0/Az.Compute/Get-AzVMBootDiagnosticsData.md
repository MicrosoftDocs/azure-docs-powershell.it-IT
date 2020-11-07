---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: ab7bae5430bf2b588997d57e92a18a4408ca4334
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863781"
---
# <span data-ttu-id="ba6aa-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="ba6aa-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="ba6aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ba6aa-102">SYNOPSIS</span></span>
<span data-ttu-id="ba6aa-103">Ottiene i dati di diagnostica di avvio per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ba6aa-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="ba6aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba6aa-104">SYNTAX</span></span>

### <span data-ttu-id="ba6aa-105">WindowsParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ba6aa-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba6aa-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="ba6aa-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba6aa-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba6aa-107">DESCRIPTION</span></span>
<span data-ttu-id="ba6aa-108">Il cmdlet **Get-AzVMBootDiagnosticsData** ottiene i dati di diagnostica di avvio per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ba6aa-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="ba6aa-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba6aa-109">EXAMPLES</span></span>

### <span data-ttu-id="ba6aa-110">Esempio 1: ottenere i dati di diagnostica di avvio</span><span class="sxs-lookup"><span data-stu-id="ba6aa-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="ba6aa-111">Questo comando consente di ottenere i dati di diagnostica di avvio per la macchina virtuale denominata ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="ba6aa-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="ba6aa-112">Questa macchina virtuale esegue il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="ba6aa-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="ba6aa-113">Il comando Archivia i dati in un percorso locale specificato.</span><span class="sxs-lookup"><span data-stu-id="ba6aa-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="ba6aa-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ba6aa-114">PARAMETERS</span></span>

### <span data-ttu-id="ba6aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba6aa-115">-DefaultProfile</span></span>
<span data-ttu-id="ba6aa-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba6aa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba6aa-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="ba6aa-117">-Linux</span></span>
<span data-ttu-id="ba6aa-118">Indica che la macchina virtuale esegue il sistema operativo Linux.</span><span class="sxs-lookup"><span data-stu-id="ba6aa-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba6aa-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="ba6aa-119">-LocalPath</span></span>
<span data-ttu-id="ba6aa-120">Specifica il percorso locale per i dati di diagnostica di avvio.</span><span class="sxs-lookup"><span data-stu-id="ba6aa-120">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: LinuxParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba6aa-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ba6aa-121">-Name</span></span>
<span data-ttu-id="ba6aa-122">Specifica il nome della macchina virtuale per cui questo cmdlet ottiene i dati di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="ba6aa-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba6aa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba6aa-123">-ResourceGroupName</span></span>
<span data-ttu-id="ba6aa-124">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ba6aa-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ba6aa-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="ba6aa-125">-Windows</span></span>
<span data-ttu-id="ba6aa-126">Indica che la macchina virtuale esegue il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="ba6aa-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba6aa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba6aa-127">CommonParameters</span></span>
<span data-ttu-id="ba6aa-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba6aa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba6aa-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba6aa-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba6aa-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ba6aa-130">INPUTS</span></span>

### <span data-ttu-id="ba6aa-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ba6aa-131">None</span></span>
<span data-ttu-id="ba6aa-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="ba6aa-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ba6aa-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba6aa-133">OUTPUTS</span></span>

### <span data-ttu-id="ba6aa-134">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ba6aa-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="ba6aa-135">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="ba6aa-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="ba6aa-136">Note</span><span class="sxs-lookup"><span data-stu-id="ba6aa-136">NOTES</span></span>

## <span data-ttu-id="ba6aa-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba6aa-137">RELATED LINKS</span></span>

[<span data-ttu-id="ba6aa-138">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ba6aa-138">Set-AzVMBootDiagnostic</span></span>](./Set-AzVMBootDiagnostic.md)



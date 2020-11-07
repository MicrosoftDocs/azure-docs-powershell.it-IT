---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmbootdiagnosticsdata
schema: 2.0.0
ms.openlocfilehash: 867f2c14e90eddd9649e0720d41f56aa896c61ff
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866132"
---
# <span data-ttu-id="683ec-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="683ec-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="683ec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="683ec-102">SYNOPSIS</span></span>
<span data-ttu-id="683ec-103">Ottiene i dati di diagnostica di avvio per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="683ec-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="683ec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="683ec-104">SYNTAX</span></span>

### <span data-ttu-id="683ec-105">WindowsParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="683ec-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="683ec-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="683ec-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="683ec-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="683ec-107">DESCRIPTION</span></span>
<span data-ttu-id="683ec-108">Il cmdlet **Get-AzureRmVMBootDiagnosticsData** ottiene i dati di diagnostica di avvio per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="683ec-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="683ec-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="683ec-109">EXAMPLES</span></span>

### <span data-ttu-id="683ec-110">Esempio 1: ottenere i dati di diagnostica di avvio</span><span class="sxs-lookup"><span data-stu-id="683ec-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="683ec-111">Questo comando consente di ottenere i dati di diagnostica di avvio per la macchina virtuale denominata ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="683ec-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="683ec-112">Questa macchina virtuale esegue il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="683ec-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="683ec-113">Il comando Archivia i dati in un percorso locale specificato.</span><span class="sxs-lookup"><span data-stu-id="683ec-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="683ec-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="683ec-114">PARAMETERS</span></span>

### <span data-ttu-id="683ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="683ec-115">-DefaultProfile</span></span>
<span data-ttu-id="683ec-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="683ec-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="683ec-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="683ec-117">-Linux</span></span>
<span data-ttu-id="683ec-118">Indica che la macchina virtuale esegue il sistema operativo Linux.</span><span class="sxs-lookup"><span data-stu-id="683ec-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="683ec-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="683ec-119">-LocalPath</span></span>
<span data-ttu-id="683ec-120">Specifica il percorso locale per i dati di diagnostica di avvio.</span><span class="sxs-lookup"><span data-stu-id="683ec-120">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="683ec-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="683ec-121">-Name</span></span>
<span data-ttu-id="683ec-122">Specifica il nome della macchina virtuale per cui questo cmdlet ottiene i dati di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="683ec-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="683ec-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="683ec-123">-ResourceGroupName</span></span>
<span data-ttu-id="683ec-124">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="683ec-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="683ec-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="683ec-125">-Windows</span></span>
<span data-ttu-id="683ec-126">Indica che la macchina virtuale esegue il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="683ec-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="683ec-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="683ec-127">CommonParameters</span></span>
<span data-ttu-id="683ec-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="683ec-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="683ec-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="683ec-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="683ec-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="683ec-130">INPUTS</span></span>

### <span data-ttu-id="683ec-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="683ec-131">None</span></span>
<span data-ttu-id="683ec-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="683ec-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="683ec-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="683ec-133">OUTPUTS</span></span>

### <span data-ttu-id="683ec-134">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="683ec-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="683ec-135">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="683ec-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="683ec-136">Note</span><span class="sxs-lookup"><span data-stu-id="683ec-136">NOTES</span></span>

## <span data-ttu-id="683ec-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="683ec-137">RELATED LINKS</span></span>

[<span data-ttu-id="683ec-138">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="683ec-138">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)



---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
ms.openlocfilehash: 5ae237c21c78f206188f23153bdf35c6bea10b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685848"
---
# <span data-ttu-id="43766-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="43766-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="43766-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43766-102">SYNOPSIS</span></span>
<span data-ttu-id="43766-103">Ottiene i dati di diagnostica di avvio per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="43766-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43766-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43766-104">SYNTAX</span></span>

### <span data-ttu-id="43766-105">WindowsParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="43766-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [<CommonParameters>]
```

### <span data-ttu-id="43766-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="43766-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [<CommonParameters>]
```

## <span data-ttu-id="43766-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43766-107">DESCRIPTION</span></span>
<span data-ttu-id="43766-108">Il cmdlet **Get-AzureRmVMBootDiagnosticsData** ottiene i dati di diagnostica di avvio per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="43766-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="43766-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43766-109">EXAMPLES</span></span>

### <span data-ttu-id="43766-110">Esempio 1: ottenere i dati di diagnostica di avvio</span><span class="sxs-lookup"><span data-stu-id="43766-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="43766-111">Questo comando consente di ottenere i dati di diagnostica di avvio per la macchina virtuale denominata ContosoVM07.</span><span class="sxs-lookup"><span data-stu-id="43766-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="43766-112">Questa macchina virtuale esegue il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="43766-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="43766-113">Il comando Archivia i dati in un percorso locale specificato.</span><span class="sxs-lookup"><span data-stu-id="43766-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="43766-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43766-114">PARAMETERS</span></span>

### <span data-ttu-id="43766-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="43766-115">-Linux</span></span>
<span data-ttu-id="43766-116">Indica che la macchina virtuale esegue il sistema operativo Linux.</span><span class="sxs-lookup"><span data-stu-id="43766-116">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="43766-117">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="43766-117">-LocalPath</span></span>
<span data-ttu-id="43766-118">Specifica il percorso locale per i dati di diagnostica di avvio.</span><span class="sxs-lookup"><span data-stu-id="43766-118">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="43766-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="43766-119">-Name</span></span>
<span data-ttu-id="43766-120">Specifica il nome della macchina virtuale per cui questo cmdlet ottiene i dati di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="43766-120">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="43766-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43766-121">-ResourceGroupName</span></span>
<span data-ttu-id="43766-122">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="43766-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="43766-123">-Windows</span><span class="sxs-lookup"><span data-stu-id="43766-123">-Windows</span></span>
<span data-ttu-id="43766-124">Indica che la macchina virtuale esegue il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="43766-124">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="43766-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43766-125">CommonParameters</span></span>
<span data-ttu-id="43766-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43766-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43766-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43766-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43766-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43766-128">INPUTS</span></span>

### <span data-ttu-id="43766-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="43766-129">None</span></span>
<span data-ttu-id="43766-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="43766-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="43766-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43766-131">OUTPUTS</span></span>

## <span data-ttu-id="43766-132">Note</span><span class="sxs-lookup"><span data-stu-id="43766-132">NOTES</span></span>

## <span data-ttu-id="43766-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43766-133">RELATED LINKS</span></span>

[<span data-ttu-id="43766-134">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="43766-134">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)



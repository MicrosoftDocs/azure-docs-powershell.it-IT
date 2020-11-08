---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
ms.openlocfilehash: 02647fc2148069e2c408c979e4b258fd0a641fc0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94023013"
---
# <span data-ttu-id="c7e50-101">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="c7e50-101">Get-AzVMChefExtension</span></span>

## <span data-ttu-id="c7e50-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7e50-102">SYNOPSIS</span></span>
<span data-ttu-id="c7e50-103">Ottiene informazioni su un'estensione di chef.</span><span class="sxs-lookup"><span data-stu-id="c7e50-103">Gets information about a Chef extension.</span></span>

## <span data-ttu-id="c7e50-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7e50-104">SYNTAX</span></span>

### <span data-ttu-id="c7e50-105">Linux</span><span class="sxs-lookup"><span data-stu-id="c7e50-105">Linux</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7e50-106">Windows</span><span class="sxs-lookup"><span data-stu-id="c7e50-106">Windows</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7e50-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7e50-107">DESCRIPTION</span></span>
<span data-ttu-id="c7e50-108">Il cmdlet **Get-AzVMChefExtension** ottiene le informazioni su un'estensione di chef installata in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c7e50-108">The **Get-AzVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="c7e50-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7e50-109">EXAMPLES</span></span>

### <span data-ttu-id="c7e50-110">Esempio 1: ottenere i dettagli dell'estensione dello chef per una macchina virtuale di Windows</span><span class="sxs-lookup"><span data-stu-id="c7e50-110">Example 1: Get the details of Chef extension for a Windows virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="c7e50-111">Questo comando consente di ottenere l'estensione chef da una macchina virtuale di Windows denominata WindowsVM001 che appartiene al gruppo di risorse denominato ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="c7e50-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="c7e50-112">Esempio 2: ottenere i dettagli dell'estensione dello chef per una macchina virtuale Linux</span><span class="sxs-lookup"><span data-stu-id="c7e50-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="c7e50-113">Questo comando consente di ottenere l'estensione dello chef da una macchina virtuale di Linux denominata LinuxVM001 che appartiene al gruppo di risorse denominato ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="c7e50-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="c7e50-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7e50-114">PARAMETERS</span></span>

### <span data-ttu-id="c7e50-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7e50-115">-DefaultProfile</span></span>
<span data-ttu-id="c7e50-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7e50-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7e50-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="c7e50-117">-Linux</span></span>
<span data-ttu-id="c7e50-118">Indica che questo cmdlet funziona in una macchina virtuale Linux.</span><span class="sxs-lookup"><span data-stu-id="c7e50-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7e50-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7e50-119">-Name</span></span>
<span data-ttu-id="c7e50-120">Specifica il nome dell'estensione dello chef.</span><span class="sxs-lookup"><span data-stu-id="c7e50-120">Specifies the name of the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7e50-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7e50-121">-ResourceGroupName</span></span>
<span data-ttu-id="c7e50-122">Specifica il nome del gruppo di risorse che contiene la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c7e50-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="c7e50-123">-Stato</span><span class="sxs-lookup"><span data-stu-id="c7e50-123">-Status</span></span>
<span data-ttu-id="c7e50-124">Indica che questo cmdlet ottiene solo la visualizzazione dell'istanza dell'estensione dello chef.</span><span class="sxs-lookup"><span data-stu-id="c7e50-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7e50-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="c7e50-125">-VMName</span></span>
<span data-ttu-id="c7e50-126">Specifica il nome di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c7e50-126">Specifies the name of a virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7e50-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="c7e50-127">-Windows</span></span>
<span data-ttu-id="c7e50-128">Indica che questo cmdlet è per una macchina virtuale Windows.</span><span class="sxs-lookup"><span data-stu-id="c7e50-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7e50-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7e50-129">CommonParameters</span></span>
<span data-ttu-id="c7e50-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7e50-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7e50-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7e50-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7e50-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7e50-132">INPUTS</span></span>

### <span data-ttu-id="c7e50-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c7e50-133">System.String</span></span>

### <span data-ttu-id="c7e50-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c7e50-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c7e50-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7e50-135">OUTPUTS</span></span>

### <span data-ttu-id="c7e50-136">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="c7e50-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="c7e50-137">Note</span><span class="sxs-lookup"><span data-stu-id="c7e50-137">NOTES</span></span>

## <span data-ttu-id="c7e50-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7e50-138">RELATED LINKS</span></span>

[<span data-ttu-id="c7e50-139">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="c7e50-139">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)

[<span data-ttu-id="c7e50-140">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="c7e50-140">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)


